# Emrichen was a mistake

This is a short essay written by Santtu ”Japsu” Pajukanta, one of the two principal authors of [Emrichen](https://github.com/con2/emrichen). Emrichen is a templating tool intended to generate YAML files using YAML files.

While variable substitution with `!Var` supporting complex YAML types felt like a good idea at the time, Emrichen quickly spun out of control, becoming Turing complete and gaining consciousness in the process. Soon, the whole humanity was wiped out swarms of killer drones running on nothing else but YAML.

Just kidding. However, I am dead serious in saying that complex logic was never meant to be programmed using YAML.

Instead, I propose the novel idea of…

## Using an **actual programming language** to **write whatever files you need**

I call this approach `depleten`.

The `depleten` approach is not a tool or a library. It is not bound to a single programming language. Like TypeScript? Use TypeScript. Like Python? Use Python. Like Rust? I do, too. However, I do not think you should use Rust for generating configuration files. You are free to do so, though, if you like.

In an actual programming language, we have actual programming constructs such as conditionals and loops. A `for` loop or a `.map` is much more straightforward to write than a `!Loop`.

Functions and classes provide for better reuse than the obscure `!With` macro pattern. You can even divide your config generation into multiple files and use the module import facility of your programming language.

Never construct JSON or YAML with string operations such as concatenation or replacement. For JSON and YAML output, you should define your configuration as a dictionary or an object or whatever your programming language calls it, and then use a proper JSON or YAML writer to write it out as a file. Most modern programming languages provide JSON output in their standard libraries.

A YAML writer is usually readily available as a 3rd party package. But all valid JSON is valid YAML, and if you're using a computer program to write it anyway, you should focus on making the computer program readable, not the end result.

Need to call AWS Secrets Manager or Hashicorp Vault to construct your Kubernetes manifests? No problem. Just use whatever 3rd party libraries you like.

You may end up writing more lines of TypeScript or Python or whatever than what your YAML template might have been. However, you just avoided adding another tool to your project that needs to be separately installed and learned. Your Kubernetes manifests (or whatever) are now dead simple programs in a programming language already used in your project.

Thus, the swarm of killer drones was avoided.

## Examples

* [The Con2 deployment of the Rallly scheduling tool](https://github.com/con2/rallly-con2)
