# Self-hosted Complete Media Stack

Transform your home server into a powerful self-hosted media stack, granting you unparalleled privacy and absolute control over your personal data. This media stack comprises a collection of cutting-edge tools, each serving a specific purpose to provide you with an exceptional media streaming experience.

## Components:

1. **Jellyfin** — Embrace the power of Free and Open Source software with Jellyfin, a versatile platform that lets you effortlessly manage and stream your media library. By hosting Jellyfin on your home server, you can enjoy seamless access to your movies, TV shows, music, and more, all without relying on third-party services.

2. **Radarr** — Elevate your media collection by integrating Radarr, an intuitive and Free Open Source tool that automatically fetches and downloads movies via Usenet and BitTorrent. With Radarr's advanced features, you'll always stay up-to-date with your favorite films while retaining complete control over the downloading process.

3. **Sonarr** — Take your TV show management to new heights with Sonarr, another brilliant Free and Open Source software. This tool works alongside Radarr to automatically download your favorite TV shows via Usenet and BitTorrent, ensuring that you never miss a single episode.

4. **Jackett** — Maintain privacy and enhance efficiency with Jackett, a reliable proxy server that seamlessly parses results from various tracker sites. As a Free and Open Source application, Jackett ensures that your media stack operates smoothly and securely, even when interacting with diverse sources.

5. **Transmission** — Optimize your BitTorrent experience using Transmission, a Free and Open Source BitTorrent client designed for downloading, seeding, and peering on the torrent network. With Transmission at your disposal, you can efficiently manage your torrent activity while safeguarding your data on your home server.

## Workflow:

Let's dive into the seamless workflow of this self-hosted media stack, showcasing how each component works in harmony:

1. **Searching for Movies and TV Shows:** When you search for a movie or TV show in Radarr or Sonarr, these applications query The Movie Database (TMDb) to find the desired content.

2. **Requesting Indexers with Jackett:** After you add a movie to Radarr or a TV show to Sonarr, these applications send a query/request to Jackett. Jackett acts as a proxy server, communicating with various torrent indexers to look for the specific movies or TV shows.

3. **Finding the Content:** Jackett scours the configured torrent indexers and returns search results to Radarr or Sonarr. If the content meeting all the specified criteria is found in any of the configured torrent indexers, Radarr or Sonarr proceeds to the next step.

4. **Downloading with Transmission:** Once the desired movie or TV show with all the requirements met is found in any of the setup torrent indexers, Radarr or Sonarr sends the magnet link to Transmission. Transmission is a Free and Open Source BitTorrent client that takes over the downloading process.

5. **Downloading and Linking:** Transmission then begins to download or "leech" the movie or TV show from the torrent network, interacting with peers and seeders. Upon completion of the download, Transmission creates a hard link to the downloaded content in the root folder of Radarr or Sonarr.

6. **Adding to Jellyfin Library:** During the scheduled periodic scan of media libraries, Jellyfin detects the movie or TV show present in the root folder of Radarr or Sonarr. Jellyfin then automatically adds the media to its library, making it available for smooth streaming to your devices.

7. **Streaming with Jellyfin:** Now that the movie or TV show is in Jellyfin's library, you can conveniently stream it directly from your self-hosted media server to any supported device, all while enjoying the benefits of privacy and complete control over your data.

The process repeats for each new movie or TV show you add to Radarr or Sonarr, ensuring a streamlined and automated media management system.

Enjoy the freedom of hosting your own media, with privacy and data control in your hands!