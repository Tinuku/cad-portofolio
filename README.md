# CAD portfolio

## Getting a model from Fusion 360 onto the site
Fusion can't save GLB, the 3D format web pages use, so the model goes through one converter.

1. In Fusion, select the body or component, then go to **File → Export → OBJ** (or right-click the body → Save as Mesh → OBJ, refinement Medium).
   OBJ keeps the colours/appearances. STL works too, but it has no colour.
2. Convert the OBJ to GLB. Pick one:
   - **Blender (free):** File → Import → Wavefront (.obj), then File → Export → glTF 2.0, Format: **glTF Binary (.glb)**.
   - **Online, quicker:** a converter such as 3dviewer.net. Drop the .obj and .mtl files in, then Export → GLB.
3. Put the `.glb` file in `models/`. In `index.html`, change the project's `model:` line to `model: "models/your-file.glb"`.
4. Keep each file under about 5 MB. If it's bigger, export from Fusion at a lower refinement.

## Text
Each project has Romanian (`ro`) and English (`en`) text in `index.html`. The site opens in Romanian, and the EN button switches it.

## Publish
Push this folder to a GitHub repo named `yourname.github.io`, then go to Settings → Pages → Deploy from branch → main.
To preview locally, run `python3 -m http.server` and open http://localhost:8000.
