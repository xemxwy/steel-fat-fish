# 背景音乐素材

页面右下角「♫ 开启配乐」按钮启动播放；浏览器要求先有一次用户点击，之后才能出声。

曲目随剧情推进切换，切换时有 1.2 秒淡入淡出（`changeMusic()`）：

| 触发时点 | 曲目 | 文件 | 时长 |
|---|---|---|---|
| 开局 | Let Me Go | `let-me-go.aac` | 3:57 |
| 唯一正统投票 | Bella Ciao | `bella-ciao.mp3` | 1:58 |
| 全面开战 | 保卫黄河 | `baowei-huanghe.mp3` | 2:49 |
| 第三阶段 | 国际歌 | `internationale.mp3` | 4:54 |

**格式**：除开局的 `.aac` 外全部统一为 **MP3（libmp3lame, 192 kbps, 44.1 kHz 立体声）**。
`.aac` 与 `.mp3` 在 Chrome / Edge / Firefox / **Safari** 上均可播放，无兼容性缺口。

---

## 游戏内曲目

### `let-me-go.aac` — Let Me Go

项目作者提供，非公开来源素材，**不在下方许可清单内**。

### `bella-ciao.mp3` — Bella Ciao（纯器乐）

- **许可：** 公有领域（Commons 标注 `PD-user`）
- **作者：** Pracchia-78，2015 年用 LMMS 1.1.0 自制
- **来源：** [Wikimedia Commons 文件页](https://commons.wikimedia.org/wiki/File:Anonimo_-_Bella_ciao_(versione_solo_strumentale).ogg)
- 时长 1:58（118 秒），原为 OGG，已转 MP3

意大利反法西斯游击队歌，象征抵抗运动，亦为反法西斯纪念活动的常用曲目。

### `baowei-huanghe.mp3` — 保卫黄河

- **来源：** [Internet Archive 条目 `lp_yellow-river-cantata_central-philharmonic-society`](https://archive.org/details/lp_yellow-river-cantata_central-philharmonic-society)
- **文件路径：** `disc1/02.02. 保卫黄河 = Defend The Yellow River.mp3`
- **演出：** 中央乐团（Central Philharmonic Society）
- **藏品来源：** Boston Public Library 黑胶馆藏，属 `album_recordings` / `vinyl_bostonpubliclibrary` 合集
- **许可：** ⚠️ **该条目未标注任何许可（无 `licenseurl`，无 `rights` 字段）**
- 时长 2:49（169 秒），VBR MP3，**原件未转码**

《黄河大合唱》第七乐章，冼星海 1939 年作于延安，光未然作词。曲作者 1945 年去世，乐谱在中国境内仍受版权保护；**这份录音本身的出版年代未能确认**。上传者未声明许可，因此这里**不能主张它是公有领域或自由许可素材**。

> **使用前提（由项目作者确认）**：本作为公开、非盈利的同人作品，不进行任何商业利用，并按此保留来源与不确定性说明。
> **如需收紧**：把 `music/baowei-huanghe.mp3` 删除，或改用 `备用曲目/` 中的替代曲，并把 `index.html` 里 `musicTracks.yellowRiver.file` 指过去即可。

### `internationale.mp3` — 国际歌（中文旧录音）

- **许可：** CC0（Commons 文件页标注）
- **来源：** [Wikimedia Commons 文件页](https://commons.wikimedia.org/wiki/File:Internationale-cmn_(英特纳雄耐尔).ogg)
- 时长 4:54（294 秒），原为 OGG，已转 MP3

---

## 备用曲目（`备用曲目/`，未接入游戏）

想换曲时直接改 `musicTracks` 里对应项的 `file` 路径即可。

### `internationale-toscanini-CC0.mp3` — 国际歌（器乐版）

- **许可：** **CC0 1.0**（公有领域贡献，无署名义务）
- **演出：** Arturo Toscanini 指挥 NBC Symphony Orchestra
- **来源：** [Internet Archive 条目 `InternationaleInstrumentalToscanini`](https://archive.org/details/InternationaleInstrumentalToscanini)
- 时长 2:31（151 秒）

第三阶段若想从中文旧录音换成器乐版，用这一首。

### `bandiera-rossa-CC-BY-NC-SA.ogg` — Bandiera Rossa（红旗歌）

- **许可：** **CC BY-NC-SA 2.0**（署名 — 非商业性使用 — 相同方式共享）
- **演出：** Jim Larkin
- **来源：** [Internet Archive 条目 `Larkin_Bandiera_Rossa`](https://archive.org/details/Larkin_Bandiera_Rossa)
- 时长 2:35（155 秒）

> ⚠️ 这是唯一带「非商业性使用」限制的曲目。本作非盈利，符合该条款；但若日后有任何商业化，必须把它移除。另需按 CC BY-NC-SA 署名，并以相同协议共享改编版本。
> 仍是 `.ogg`，**若要接入游戏请先转 MP3**（见下方命令）。

### `march-of-the-volunteers-instrumental-CC0.mp3` — 义勇军进行曲（器乐版）

- **许可：** 公有领域（Commons 标注 `PD`，美国海军军乐队演奏录音）
- **来源：** [Wikimedia Commons 文件页](https://commons.wikimedia.org/wiki/File:March_of_the_Volunteers_instrumental.ogg)
- 时长 0:44，原为 OGG，已转 MP3
- 田汉作词、聂耳作曲，1935 年。**是中华人民共和国国歌，象征意义极强**，是否用于游戏请自行判断。

### 原件备份

`bella-ciao-原件.ogg`、`internationale-中文版-原件.ogg`、`march-of-the-volunteers-instrumental-CC0-原件.ogg`
是转码前的 OGG 原件，仅供回溯，**不参与游戏加载**。确认无误后可自行删除。

---

## 转码记录

本机原本没有 ffmpeg，但系统内已装有多个副本。实际使用的一个带 `libmp3lame`：

```
C:\Users\mxwy\AppData\Local\oopz\ffmpeg.exe
```

转码命令（`-map_metadata -1` 是清掉原件里可能残留的元数据）：

```powershell
$ff = 'C:\Users\mxwy\AppData\Local\oopz\ffmpeg.exe'
& $ff -hide_banner -loglevel error -y -i 输入.ogg `
      -codec:a libmp3lame -b:a 192k -ar 44100 -map_metadata -1 输出.mp3
```

转码后**逐首核对了时长**，与原件完全一致（误差 0.02–0.04 秒）：

| 文件 | 原件 | 转码后 |
|---|---|---|
| bella-ciao | 00:01:58.09 | 00:01:58.13 |
| internationale | 00:04:54.31 | 00:04:54.35 |
| march-of-the-volunteers | 00:00:43.94 | 00:00:43.96 |

> 注：本机 ffmpeg 没有 `ffprobe`，核对时长是用 `ffmpeg -i 文件` 读 stderr 的 `Duration:` 得到的。

---

## 曾考察但未采用的来源

- **Wikimedia Commons 的中文抗战歌曲**：没有《保卫黄河》《游击队歌》《在太行山上》等的自由许可录音（多为朗读版或无关条目）。
- **FreePD.com**：站点已于 2025 年永久关闭。
- **Musopen**：返回 403，拒绝自动访问。
- **Internet Archive 的《黄河大合唱》FLAC 母带**：单面 300–340 MB，体积不适合网页游戏，故取同条目的 VBR MP3 音轨。
