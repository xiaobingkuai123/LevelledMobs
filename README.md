<td style="text-align: center;">

<img src="https://i.ibb.co/ySgMPd0/Levelled-Mobs-Banner-v2-0.png" width="600" height="300" alt="LevelledMobs Banner" />

# LevelledMobs 4

*An ArcanePlugins Resource • by PenalBuffalo, UltimaOath, and lokka30*

<a href="https://discord.gg/arcaneplugins-752310043214479462">
<img src="https://img.shields.io/badge/Chat%20%2F%20Support-on%20Discord-skyblue?style=for-the-badge&logo=discord&logoColor=white" alt="Support available on Discord">
</a>
<a href="https://www.spigotmc.org/threads/levelledmobs.412953/">
<img src="https://img.shields.io/badge/Chat%20%2F%20Support-Spigot%20PM-skyblue?style=for-the-badge&logo=googlemessages" alt="Support available through Spigot PMs">
</a>

<br />

<a href="https://arcaneplugins.gitbook.io/levelledmobs-the-ultimate-mob-levelling-solution">
<img src="https://img.shields.io/badge/Documentation-on%20Wiki-skyblue?style=for-the-badge&logo=github" alt="Documentation available on the Wiki">
</a>

<a href="https://arcaneplugins.gitbook.io/levelledmobs-the-ultimate-mob-levelling-solution/credits-and-misc/developers-and-contributors">
    <img src="https://img.shields.io/badge/Contributors-View%20Credits-skyblue?style=for-the-badge" alt="Contributors listed in Credits Page">
</a>

<br /><hr />

## ⚠️ This fork: Folia support restored / 本分支：已恢复 Folia 支持

This fork is based on the official **LevelledMobs 4.5.3.2** and manually restores Folia support,
which was dropped by the upstream project after 4.5.2.

本分支基于官方 **LevelledMobs 4.5.3.2**，手动加回了官方在 4.5.2 之后移除的 Folia 支持。

| | |
|---|---|
| **Server / 服务端** | Folia 26.2 |
| **Build JDK / 编译 JDK** | 21 |
| **Tested MC / 测试版本** | 26.2 |
| **Branch / 分支** | [`folia-4.5.3.2`](https://github.com/xiaobingkuai123/LevelledMobs/tree/folia-4.5.3.2) |
| **Release / 发布** | [Releases](https://github.com/xiaobingkuai123/LevelledMobs/releases) |

### What was changed / 改动内容

- Restored `folia-supported: true` in `plugin.yml`
- Restored the `folia-api` dependency in `build.gradle.kts`
- `NmsNametagSender.sendNametag` — on Folia, route through `SchedulerWrapper` instead of a direct synchronous call
- `NmsNametagSender.sendNametagNonAsync` — added entity validity checks and reflection null-safety
- `NmsNametagSender.cloneEntityData` — changed `as Array<Any>` to `as? Array<Any> ?: return null`
- `NametagQueueManager` — on Folia, also use the queue + `EntityScheduler`, no longer bypassing the queue

- 恢复 `plugin.yml` 的 `folia-supported: true`
- 恢复 `build.gradle.kts` 的 `folia-api` 依赖
- `NmsNametagSender.sendNametag`：Folia 下统一走 `SchedulerWrapper`，不再直接同步调用
- `NmsNametagSender.sendNametagNonAsync`：加实体有效性检查 + 反射判空
- `NmsNametagSender.cloneEntityData`：`as Array<Any>` 改为 `as? Array<Any> ?: return null`
- `NametagQueueManager`：Folia 下也走队列 + `EntityScheduler`，不再绕过队列直通

<br /><hr />

## Learn More at [✈️ HangarMC](https://hangar.papermc.io/ArcanePlugins/LevelledMobs) or [🚰 SpigotMC](https://www.spigotmc.org/resources/levelledmobs.74304/)

### Also see: [Errors and Running LM](https://arcaneplugins.gitbook.io/levelledmobs-the-ultimate-mob-levelling-solution/levelledmobs-v4.0/errors-and-running-lm) • [Installation Instructions](https://arcaneplugins.gitbook.io/levelledmobs-the-ultimate-mob-levelling-solution/levelledmobs-v4.0/installation)

</td>

<br /><hr />

## Embedded Projects

We are grateful to the authors and contributors of these projects,
as they make the current version of LevelledMobs possible.

Remember to give these projects a star. :)

- [CommandAPI](https://github.com/JorelAli/CommandAPI) (JorelAli)
- [Configurate](https://github.com/SpongePowered/Configurate/) (SpongePowered Team)
- [Crunch](https://github.com/Redempt/Crunch) (Redempt)
- [MineDown](https://github.com/Phoenix616/MineDown) (Phoenix616)
- [MorePersistentDataTypes](https://github.com/JEFF-Media-GbR/MorePersistentDataTypes) (JEFF-Media-GbR)
- [Item-NBT-API](https://github.com/tr7zw/Item-NBT-API) (tr7zw)
- [Paper-API](https://github.com/PaperMC/Paper) (PaperMC Team)
- [PlaceholderAPI](https://github.com/PlaceholderAPI/PlaceholderAPI) (PlaceholderAPI Team)
- [Spigot-API](https://www.spigotmc.org/) (SpigotMC Team)

## License

[![GPLv3 or Later](https://www.gnu.org/graphics/gplv3-with-text-84x42.png)](https://www.gnu.org/licenses/gpl-3.0.html)

> Copyright © 2020-2024 lokka30
>
> Copyright © 2020-2024 PenalBuffalo (aka stumper66)
>
> Copyright © 2020-2024 UltimaOath (aka Oathkeeper)
>
> Copyright © 2020-2024 LevelledMobs Contributors
>
> Copyright © 2026 xiaobingkuai123 (Folia restoration fork)
>
> This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.
>
> This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details.
>
> You should have received a copy of the GNU General Public License along with this program.  If not, see <https://www.gnu.org/licenses/>.

**[View License Document: `LICENSE.md`](LICENSE.md)**

<br /><hr />

<td style="text-align: center;">

## Learn More at [✈️ HangarMC](https://hangar.papermc.io/ArcanePlugins/LevelledMobs) or [🚰 SpigotMC](https://www.spigotmc.org/resources/levelledmobs.74304/)

### Also see: [Server Compatibility](https://arcaneplugins.gitbook.io/levelledmobs-the-ultimate-mob-levelling-solution/levelledmobs-v4.0/installation#are-you-running-a-compatible-server-software) • [Installation Instructions](https://arcaneplugins.gitbook.io/levelledmobs-the-ultimate-mob-levelling-solution/levelledmobs-v4.0/installation)

</td>
