# XGBoost Interactive Algorithm Visualizer

## Run locally

No installation or build step is required. From the `XGBoost` directory, start a local web server:

```bash
python3 -m http.server 8000
```

Then open [http://localhost:8000/](http://localhost:8000/) in a modern web browser.

To stop the server, return to the terminal and press `Ctrl+C`.

## How to use

1. Create a dataset in the **Shape the Problem** panel:
   - Select **Add Points**, then click the canvas to add a small group of points or drag to spray points continuously.
   - Adjust **Brush Size** to change the spray and eraser radius.
   - Adjust **Spray Density** to choose how many points are created per burst, from 1 to 10.
   - Select **Delete Points**, then click near a point to remove one point or drag to erase multiple points within the red brush.
   - Select **Random Data** to generate a new dataset, or **Clear** to remove all points.
   - The canvas supports up to 240 points. A red warning appears above the canvas when the limit is reached.

2. Adjust the hyperparameters in the **Tune the Learner** panel. Changing a value resets the current model so training can restart with the new settings.

3. Select **Next Step** to move through the XGBoost process one stage at a time. The right side explains the current calculation and updates the model structure.

4. Select **Train Until Convergence** to run the steps automatically. Use **Pause** to stop the animation or **Reset Model** to restart training while keeping the current dataset.

5. Observe the results:
   - The data canvas shows the current prediction, residuals, and latest split.
   - The model panels show gradients, Hessians, split gain, leaf weights, tree contributions, and the additive ensemble.
   - The Training Ledger displays up to 12 representative points when the dataset is large, while the model still calculates every point.
   - The Loss Graph shows how MSE, RMSE, and MAE change after each boosting round.
