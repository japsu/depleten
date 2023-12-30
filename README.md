# Emrichen was a mistake

This is a short essay written by Santtu ”Japsu” Pajukanta, one of the two principal authors of [Emrichen](https://github.com/con2/emrichen). Emrichen is a templating tool intended to generate YAML files using YAML files.

While variable substitution with `!Var` supporting complex YAML types felt like a good idea at the time, Emrichen quickly spun out of control, becoming Turing complete and gaining consciousness in the process. Soon, the whole humanity was wiped out swarms of killer drones running on nothing else but YAML.

Just kidding. However, I am dead serious in saying that complex logic was never meant to be programmed using YAML.

Instead, I propose the novel idea of using an **actual programming language** to **write whatever files you need**, be they YAML, JSON or [something else altogether](https://github.com/con2/redirects/blob/d67af7050da756c2a262ca47111212d29623f559/kubernetes/configmap.in.yaml#L14-L27). I call this approach `depleten`.

The `depleten` approach is not a tool or a library. It is not bound to a single programming language. Like TypeScript? Use TypeScript. Like Python? Use Python. Like Rust? I do, too. However, I do not think you should use Rust for generating configuration files. You are free to do so, though, if you like.

In an actual programming language, we have actual programming constructs such as conditionals and loops. A `for` loop or a `.map` is much more straightforward to write than a `!Loop`. Functions and classes provide for better reuse than the obscure `!With` macro pattern. You can even divide your config generation into multiple files and use the module import facility of your programming language.

Need to call AWS Secrets Manager or Hashicorp Vault to construct your Kubernetes manifests? No problem. Just use whatever 3rd party libraries you like.

Thus, the swarm of killer drones was avoided.

## Examples
