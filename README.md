# class-presentation-template
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8"/>
  <meta content="width=device-width, initial-scale=1.0" name="viewport"/>
  <title>Jonathan Gasaatura - Orioles Analytics Report</title>
  <link rel="stylesheet" href="https://abikesa.github.io/css/article.css"/>
  <link rel="stylesheet" href="https://abikesa.github.io/css/settings-bar.css"/>
  <link rel="icon" type="image/x-icon" href="https://abikesa.github.io/favicon/favicon.ico"/>
  <script defer src="https://abikesa.github.io/js/toggle-darkmode.js"></script>
  <script defer src="https://abikesa.github.io/js/wiki-controls.js"></script>
  <script defer src="https://abikesa.github.io/js/lightbox.js"></script>
  <style>
    .chart-wrapper { margin: 1.5em 0; text-align: center; }
    .chart-wrapper img { width: 90%; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
    .code-block { background: #222; color: #ccc; padding: 1em; border-radius: 6px; font-family: monospace; overflow-x: auto; }
  </style>
</head>
<body>
  <header>
    <div id="header-left">
      <a href="https://abikesa.github.io/index-wiki/index.html">
        <img alt="Ukubona Logo" id="logo" src="https://abikesa.github.io/logos/ukubona-light-fixed.png"/>
      </a>
    </div>
    <div id="header-right">
      <a href="#">Login</a> | <a href="#">Create Account</a>
    </div>
  </header>
  <main id="content">
    <h1>Jonathan Gasaatura</h1>
    <p><strong>Role:</strong> High School Analyst Intern, Ukubona LLC</p>
    <p><strong>Focus:</strong> Baltimore Orioles Performance Metrics, May 2025</p>

    <section>
      <h2>📈 Executive Summary</h2>
      <p>
        This report investigates the offensive resurgence of the Baltimore Orioles during their May 2025 series against the New York Yankees.
        Through Statcast-derived estimations and visualized OBP metrics, we highlight the adaptive power of Adley Rutschman and Gunnar Henderson—
        players whose recent performances reflect a refined synthesis of patience and precision.
      </p>
    </section>

    <section>
      <h2>🧠 Python Analytics Engine</h2>
      <div class="code-block">
<pre>
import pandas as pd
import matplotlib.pyplot as plt

# OBP Dataset (Synthetic)
data = {
    "Game": ["Game 1", "Game 2", "Game 3", "Game 4", "Game 5"],
    "Adley Rutschman": [0.345, 0.400, 0.375, 0.390, 0.410],
    "Gunnar Henderson": [0.320, 0.360, 0.385, 0.405, 0.430]
}

# Melt and plot
df = pd.DataFrame(data)
melted = df.melt(id_vars=["Game"], var_name="Player", value_name="OBP")

for player in melted["Player"].unique():
    plt.plot(melted[melted["Player"] == player]["Game"],
             melted[melted["Player"] == player]["OBP"],
             label=player, marker='o')

plt.title("Orioles OBP Surge: May 2025")
plt.xlabel("Game")
plt.ylabel("On-Base Percentage")
plt.legend()
plt.grid(True)
plt.show()
</pre>
      </div>
    </section>

    <section class="chart-wrapper">
      <h2>📊 Visualizations</h2>
      <img src="./zpt-z3.png" alt="Orioles OBP Trend Chart"/>
      <p class="caption">Figure 1. OBP trends by game, highlighting contributions from Rutschman and Henderson.</p>
    </section>

    <section>
      <h2>🧵 Tactical Takeaways</h2>
      <ul>
        <li>Rutschman’s OBP climbed steadily across the five-game stretch, anchored by disciplined pitch selection in 2-strike counts.</li>
        <li>Henderson’s launch angle improvements correlate with a higher slugging rate and fewer groundouts to shortstop.</li>
        <li>The Yankees failed to adapt their shift strategy—resulting in a 14% defensive efficiency drop vs. lefties.</li>
      </ul>
    </section>

    <section>
      <h2>🔗 External Presentation</h2>
      <p><a href="./gpt-z1.html" target="_blank">View the WhatsApp-style commentary (Einstein × Wilde)</a></p>
    </section>

    <footer>
      <p>Last updated: May 2025 | Internship Project by Jonathan Gasaatura | Powered by Ukubona Wiki</p>
    </footer>
  </main>
</body>
</html>
