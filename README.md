![Bloom](/priv/images/bloom.png)

# Bloom

The opinionated extention to Phoenix core_components.

Inspired by shad-cn.

## Installation

Can be installed by adding `bloom` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:bloom, "~> 0.0.2"}
  ]
end
```

Relies on Phoenix being installed.

## Installing components

#### All components can be installed by running the following mix command in your project root

```
mix bloom.install <component_name>
```

Some components require Tailwind Config changes - refer to the component doc for more information.

#### View all components by running:

```
mix bloom.install help
```

## Frequently Asked Questions

### Why are the components manually installed?

So you can customise them to your hearts content and make them your own easily. The source code of the components will live in your project so you can tweak them as you see fit.

### The colours aren't showing up!

Tailwind treeshakes colours that aren't in use at compile time - this means dynamic ones set by Phoenix Components won't show if the colours aren't already part of the page. You can circumvent this by safelisting colours in your `tailwind.config.js` or ensuring the colours are already in use (not recommended).

See the [Tailwind website](https://tailwindcss.com/docs/content-configuration) for more information.

You can safelist by Regex or manually.

Recommended safelist:

```
  safelist: [
    {
      pattern: /bg-+/,
    },
    {
      pattern: /text-+/,
    },
    {
      pattern: /from-+/,
    },
    {
      pattern: /to-+/,
    },
  ],
```

### There aren't many components

I'm gonna be adding components slowly but this repo welcomes contributions for beautiful, useful components not already covered by the excellent core_components that ship with Phoenix.

### How do I preview these components?

I'm going to be adding a Storybook and website soon.
