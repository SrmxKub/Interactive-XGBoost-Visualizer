# XGBoost Interactive Algorithm Visualizer

A dependency-free, single-page teaching application that demonstrates how XGBoost regression builds decision trees from gradients, Hessians, regularized split gain, and leaf weights.

## Run locally

You can open `index.html` directly in a modern browser. For the most reliable local behavior, serve the folder:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000/`.

## Deploy to GitHub Pages

1. Push `index.html` and this README to the repository's default branch.
2. Open **Settings → Pages** in the GitHub repository.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the default branch, choose the root (`/`) folder, and save.
5. Open the GitHub Pages URL shown after deployment completes.

No package installation, compilation, or external runtime assets are required.

## How to use

- Click the data canvas to add points, or switch to delete mode and click near a point.
- Generate a random dataset or adjust the seven experiment controls, including convergence tolerance.
- Select **Next Step** to move through the exact eight teaching stages: Input Dataset, Initial Prediction, Calculate Gradients & Hessians, Find the Best Split, Calculate Leaf Weights, Calculate Tree Contribution, Update Prediction & Loss, and Add Tree & Repeat.
- Select **Train until Convergence** to advance through the same teaching steps automatically, or pause at any time.
- Follow the residuals and prediction line on the left; inspect the mathematical flow, pending tree, completed additive ensemble, point ledger, boosting loop, and primary MSE loss curve on the right.

The visualizer is a simplified educational XGBoost-style implementation for one-dimensional regression. It teaches the causal boosting flow rather than reproducing every feature of a production XGBoost library.
