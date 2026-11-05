<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/OpenJUIZ/juiz/main/assets/logo-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/OpenJUIZ/juiz/main/assets/logo-light.svg">
    <img src="https://raw.githubusercontent.com/OpenJUIZ/juiz/main/assets/logo-light.svg" alt="juiz" width="280">
  </picture>
</p>
<p align="center"><b>juiz — the robot middleware</b></p>

juiz is middleware for building robots and IoT devices as networked, distributed systems.
You write small units of software for cameras, robots, motors and sensors in Rust, Python, C++ or Haskell, then combine them so they run together as one service.

	•	Process — an idempotent function with inputs (arguments) and an output.
	•	Container — holds state; ContainerProcesses read and write it.
	•	Two ways to use it — connect Processes into a data flow (like ROS-style robot middleware), or call a Process from outside and get the result (like a server/client app).
	•	Brokers — HTTP+JSON, QUIC and IPC brokers link Processes across processes and machines.
	•	Web UI — a built-in browser view of the processes and connections in a running system.

📖 Documentation: https://openjuiz.github.io/ (日本語)

Repositories

Repository	What's in it
juiz	The middleware itself: core, SDK, juiz command, brokers, Python / C++ / Haskell bindings
juiz_examples_rust	Examples in Rust
juiz_examples_python	Examples in Python
juiz_examples_cpp	Examples in C++
openjuiz.github.io	Source of the official site (tutorial, guides, concepts)

Install

Python 3.10+ only, no Rust toolchain needed (Linux / macOS / Windows):

pip install juiz-cli     # the juiz command + pyjuiz for writing Processes in Python

To write Processes in Rust or C++ (Rust 1.88+):

cargo install juiz_app   # the juiz command
pip install pyjuiz       # only if you also write Processes in Python

Then follow the tutorial.

Packages: juiz-cli (PyPI) · pyjuiz (PyPI) · juiz_app (crates.io) · juiz_sdk (docs.rs)

日本語

juiz（ジュイス） は、ロボットや IoT 機器をネットワーク分散システムとして開発するためのミドルウェアです。
カメラやロボット、モータやセンサなどを動かすソフトウェアを Rust・Python・C++・Haskell で書き、それらをつないで一つのサービスのように動かせます。
入出力を持つ冪等な関数 Process と、状態を持つ Container を単位に開発し、Process を connect してデータフローで動かすことも、外から call して結果を受け取ることもできます。

	•	公式サイト: https://openjuiz.github.io/ja/
	•	インストール: pip install juiz-cli（Python だけで試す場合）、または cargo install juiz_app（Rust・C++ で書く場合）

License

All repositories are dual-licensed under MIT OR Apache-2.0, at your option.

[!NOTE]
juiz is developed by a single developer (@sugarsweetrobotics). Please avoid using it for mission-critical tasks.
