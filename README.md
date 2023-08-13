# plex-edition-manager
plex-edition-manager 是一个用于管理 Plex 电影版本信息的 Python 脚本。它会根据电影的文件名自动检测电影的版本（如 REMUX、BD、WEB-DL 等），并在 Plex 中更新版本信息。

## 效果展示
![版本](https://github.com/x1ao4/plex-edition-manager/assets/112841659/4d048665-1438-4c11-9b7e-a163adb1f7ba)

## 版本说明
- **REMUX** 是从 Blu-ray 光盘中提取音视频数据无损封装到其他格式中，质量与原版 Blu-ray 光盘没有区别。
- **BD** 是直接从 Blu-ray 光盘上复制而来的，画质和音质都非常好。
- **BDRIP** 是将 Blu-ray 光盘中的内容进行压缩，损失了一些画质和音质，但仍然保持了较高的清晰度。
- **WEB-DL** 是从在线流媒体服务下载的视频，画质和音质较好，但不及 Blu-ray。
- **WEBRIP** 是通过录制在线流媒体服务播放的视频获得的版本，画质和音质不及 WEB-DL。
- **HR-HDTV** 是从 HR-HDTV 广播中录制而来的，画质较好。
- **HDTV** 是从 HDTV 广播中录制而来的，画质较好。
- **HDRIP** 是由高清电影压缩而来的，损失了一些画质和音质。
- **DVDRIP** 是用 DVD 光盘中的内容压缩而成的，损失了一些画质和音质。
- **DVDSCR** 是用于奖项评选和宣传推广的 DVD 版本，可能会有水印或其他标识。
- **DVD** 是从 DVD 光盘上直接复制而来的，画质和音质适中。
- **HDTC** 是使用 Telecine 机器将胶片电影转换为数字格式，画质和音质较好。
- **TC** 与 HDTC 类似，但画质和音质适中。
- **HQCAM** 是使用高质量摄像机在电影院内录制的版本，画质和音质较差。
- **CAM** 与 HQCAM 类似，但画质和音质更差。
- **TS** 是使用专业设备在电影院内录制的版本，画质和音质较差。
- **DV** 是指杜比视界，是一种 HDR 格式，提供丰富色彩和高对比度，能显示更多细节，带来逼真观影体验。

## 运行条件
- 安装了 Python 3.0 或更高版本。
- 安装了必要的第三方库：plexapi。
- 有可用的 Plex Pass 账号，并配置了 Plex 服务器。

## 使用方法
1. 将仓库克隆或下载到计算机上的一个目录中。
2. 修改 `start.command (Mac)` 或 `start.bat (Win)` 中的路径，以指向您存放 `plex-edition-manager.py` 脚本的目录。
3. 双击运行 `start.command` 或 `start.bat` 脚本以执行 `plex-edition-manager.py` 脚本。
4. 首次运行时需要您在控制台中输入您的 Plex 用户名、密码和服务器名称。这些信息将被保存在与脚本相同目录下的 `config.json` 文件中，以便将来使用。
5. 脚本将连接到您的 Plex 服务器并从您的库中检索所有电影。
6. 对于每部电影，脚本将根据其文件名确定其版本，并在 Plex 中更新相应的版本信息。脚本将在控制台中显示每部电影的更新情况。
7. 当脚本运行完成时，您将看到更新的电影总数。

## 注意事项
- 请确保您提供了正确的 Plex 账号信息和服务器名称。
- 请确保运行脚本的设备可以连接到您的服务器。
- 脚本依赖文件名来识别电影版本，请确保文件名中包含版本相关的信息。如果文件名中不包含任何可识别的版本信息，则不会更新版本。
- 脚本仅更新 Plex 中未设置版本的电影。
- 脚本仅支持电影类型的资料库，不支持其他类型的库（例如，电视节目）。
- 当一部电影存在多个版本时，脚本会使用第一个文件的文件名识别和更新版本信息。

## 已知问题
- 由于电影版本命名的多样性，脚本可能无法准确识别某些特定版本。
- 在某些情况下，可能需要手动校正电影版本信息。
<br>

# plex-edition-manager
plex-edition-manager is a Python script for managing Plex movie edition information. It automatically detects the edition of a movie (such as REMUX, BD, WEB-DL, etc.) based on its filename and updates the edition information in Plex.

## Demo
![版本](https://github.com/x1ao4/plex-edition-manager/assets/112841659/4d048665-1438-4c11-9b7e-a163adb1f7ba)

## Editions
- **REMUX**: Extracts audio and video data from Blu-ray discs, losslessly repackages them into another format, maintaining original quality.
- **BD**: Directly copies content from Blu-ray discs, providing high-quality audio and video.
- **BDRIP**: Compresses content from Blu-ray discs to achieve smaller file sizes while preserving good quality.
- **WEB-DL**: Downloads high-quality videos from online streaming services, slightly lower quality than Blu-ray.
- **WEBRIP**: Obtained by recording streaming content online, slightly lower quality than WEB-DL.
- **HR-HDTV**: Recorded from high-resolution HDTV broadcasts, offers high-quality visuals.
- **HDTV**: Recorded from HDTV broadcasts, provides good quality visuals.
- **HDRIP**: Compressed version of high-definition movies, may have slightly reduced quality.
- **DVDRIP**: Compressed version of DVD content, moderate reduction in quality.
- **DVDSCR**: Intended for awards promotion, may have watermarks or other identifiers, good quality.
- **DVD**: Directly copies content from DVDs, moderate quality.
- **HDTC**: Digitized from film using a Telecine machine, offers higher quality.
- **TC**: Similar to HDTC, moderate quality.
- **HQCAM**: Recorded in theaters using high-quality cameras, lower quality.
- **CAM**: Recorded in theaters using cameras, even lower quality.
- **TS**: Recorded in theaters using professional equipment, lowest quality.
- **DV**: Refers to Dolby Vision, an HDR format that offers enhanced colors, contrast, and detail, providing a more immersive viewing experience.

## Requirements
- Python 3.0 or higher installed.
- Required third-party library: plexapi.
- A valid Plex Pass account with a configured Plex server.

## Usage
1. Clone or download the repository to a directory on your computer.
2. Modify the path in `start.command (Mac)` or `start.bat (Win)` to point to the directory where you store the `plex-edition-manager.py` script.
3. Double-click `start.command` or `start.bat` to execute the `plex-edition-manager.py` script.
4. On first run, you will need to enter your Plex username, password, and server name in the console. This information will be saved in the `config.json` file in the same directory as the script for future use.
5. The script will connect to your Plex server and retrieve all movies from your library.
6. For each movie, the script will determine its edition based on its filename and update the corresponding edition information in Plex. The script will display the update status of each movie in the console.
7. Once the script completes, you will see the total number of movies updated.

## Notes
- Make sure you provide correct Plex account information and server name.
- Make sure the device running the script is connected to your Plex server.
- The script relies on filenames to identify movie editions, so make sure that filenames contain edition-related information. If no recognizable edition information is included in the filename, no edition will be updated.
- The script only updates movies that do not have an edition set in Plex.
- The script only supports movie-type libraries and does not support other types of libraries (e.g., TV shows).
- When a movie has multiple versions, the script uses the filename of the first file to identify and update edition information.

## Known Issues
- Due to the diversity of movie edition naming, the script may not accurately identify certain specific editions.
- In some cases, manual correction of movie edition information may be required.
