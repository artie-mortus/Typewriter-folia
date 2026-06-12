![TypeWriter Logo](https://github.com/gabber235/TypeWriter/blob/develop/design/Banner/TW_Banner_Transparant.png?raw=true)

> **Folia fork** — drop-in Typewriter for [Folia](https://github.com/PaperMC/Folia) threaded-region servers. Upstream: [gabber235/TypeWriter](https://github.com/gabber235/Typewriter).

Typewriter is a plugin for Minecraft servers that enables you to create immersive and interactive gameplay experiences, such as custom quests, NPC dialogues, and cinematic events, all while maintaining a simple and powerful interface.

## Folia Support

This fork patches Typewriter to run on **Folia** (threaded region scheduling). Key changes:

- MCCoroutine replaced with `mccoroutine-folia` artifacts
- Async dispatchers replaced with region-aware dispatchers (`globalRegionDispatcher`, `entityDispatcher`, `regionDispatcher`)
- Scheduler calls updated to use Folia's `RegionScheduler` / `GlobalRegionScheduler` APIs
- All entity/block operations dispatched to the owning region

### Compatibility

| Typewriter | Folia |
|---|---|
| develop | 1.21.x |

## Features

- **Custom Player Interactions**: Create quests, NPC dialogues, branching storylines, and more.
- **Cinematic Sequences**: Build dynamic camera paths, animated NPC interactions, and immersive cutscenes.
- **Intelligent NPCs**: Customize NPC behavior, including walking, changing appearance, and interacting with the environment.
- **Visual Configuration**: Manage quests, NPCs, and interactions using a visual web panel designed for ease of use.
- **Extensions**: Extend Typewriter's functionality with modular components called **extensions**. Extensions allow you to integrate custom plugins and create unique in-game content.

## Getting Started

For detailed setup instructions, visit the original [Installation Guide](https://docs.typewritermc.com/docs/getting-started/installation). Use this fork's jar in place of the upstream release.

> **Note:** This fork is community-maintained. For upstream features/bugs unrelated to Folia, report to [gabber235/TypeWriter](https://github.com/gabber235/Typewriter/issues).

## Building

```bash
./gradlew :engine:engine-paper:shadowJar
```

Output: `engine/engine-paper/build/libs/`

## For Administrators

Typewriter makes it simple for server admins to create and manage custom content. Through the web panel, you can easily configure complex interactions, NPCs, and quests, even without prior coding knowledge. If your server has specific requirements, the extension system allows for easy customization and the addition of new features.

## For Developers

Typewriter is built to be highly extensible. The **extensions** system lets developers build modular, reusable components that seamlessly integrate with the plugin. To learn more about creating extensions, or any other development related questions, visit the [Development Documentation](https://docs.typewritermc.com/develop).

---

## License

Typewriter is licensed under its own [LICENSE](LICENSE).

The basic of it is that you can use the software for free, but you can't sell/redistribute/modify it.
The only exception is if you want to contribute to the project and make it better.

See [LICENSE](LICENSE) to see the full text.

## Credits

- [gabber235](https://github.com/gabber235) — original Typewriter plugin
- [Aarthificial](https://www.youtube.com/@aarthificial) — inspiration for the base logic
