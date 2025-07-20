---
{"dg-publish":true,"permalink":"/how-i-do-it-content-creation-notes-and-technical-details/","pinned":true}
---


### Resources Notes

This project uses open standards, with simplicity, ease of accessibility, sensible defaults and privacy emphasised.

All software recommended will be the most secure option practical, with simpler alternatives provided. 

Older content is in the process of being updated and brought into conformity with these standards.

For any questions please email thewordsmithspeaks@pm.me

#### All Software and Services Used

- Passwords are handled through Bitwarden. I will likely move to KeepassXC and a Sync Plugin in the new year for additional security
- Two Factor Authentication through Authy and Yubikey
- Email is handled through Protonmail
- Scheduling is handled through Proton Calendar
- Documents are written in CommonMark and stored in plain text files in an Obsidian Notes Vault located in the Resources Folder
- Payments are handled through a Wise Business Account
- Buttondown for the Newsletter, switching to a simple email list in ProtonMail is a future plan to improve privacy protections
- Website Domains are held in Njalla

Main Website - LocalWP app using the free GeneratePress Theme, then using the free Simply Static Plugin to export a static version to Github which is then rendered by Netlify. Provides a simple GUI to design, plus free from end to end and all the benefits of a static website including free hosting. 

https://localwp.com/ then https://generatepress.com/ then https://simplystatic.com/ then https://github.com/ then https://www.netlify.com/

Resources Folder - Using the secure Filen service as a base, then a Google Drive Link for redundancy and user preference. A monthly file snapshot is shared using qBittorrent and the opentrackr.org tracker under the "MindKInk" and "TheWordSmithSpeaks" search terms for easy accessibility and indexing.

https://filen.io/ then https://drive.google.com/ then https://www.qbittorrent.org/ then https://opentrackr.org/

Erotic and Safe-For-Work Audios - Recorded on my phones built-in microphone (usually), then transferred by Filen to desktop computer, edited in OcenAudio and exported as Lossless FLAC for archival purposes and 128Kpbs AAC for use using FFMPEG Batch Encoder (green icon with a white line in it). https://soundgasm.net/ to stream audio files directly to people through the browser.

https://www.ocenaudio.com/ then https://ffmpeg-batch.sourceforge.io/

Podcast - Used to be on Anchor before they were bought out by Spotify, now it's on there and shared via RSS to other providers.

This Wiki / Knowledgebase (What you are reading now) - Hosted in an Obsidian Notes Vault located in the Resources Folder, then shared for free using the https://github.com/oleeskild/Obsidian-Digital-Garden plugin, and hosted in Github and rendered on Netlify. Free end to end. Future versions will likely be based upon mkdocs or done using the Starlight Documentation Theme on the Astro NPM framework, and retain the same structure for accessibility.

There are lots of other ways to do it. If you are interested, I have conducted a massive in-depth study of the hypnokink content distribution ecosystem. Message me on Signal and I'll share my conclusions with you

#### Commitment to Data Longevity

All content is distributed in only open formats, with delivery methods having multiple failovers and redundancies.

There is the direct download link on Filen, as well as a Google Drive Backup Link, and monthly torrent snapshots 

I encourage you to download your own copy of the resources folder and share it with anyone you wish.

Audio is formatted as OPUS format for lossy, and FLAC for lossless. Video as AV1. Documents as Plaintext, formatted in CommonMark, or as LibreOffice-compatible Open Document Format (ODF) and Portable Document Format (PDF) where needed.

#### Communications

All communications are conducted over anonymous, zero-knowledge-encrypted, end-to-end-encrypted connections only.

Texting, Audio Messages and Voice Calls are through Signal.

Email is through ProtonMail.

https://signal.org/

https://proton.me/

#### Writing

All documents are published as text files in UTF encoding in the wiki or in the "Source Files" subdirectory, then published as a PDF.

All documents are written in CommonMark, a simple, human-readable, strongly defined and highly compatible open version of MarkDown.

Any documents requiring more advanced formatting are published in Open Document Format (ODF) then exported to PDF.

https://obsidian.md/

https://commonmark.org/

I am currently experimenting with the Typst typesetting system as a possible, scalable alternative.

#### Audio

All audio is encoded as either Lossless FLAC, or lossy OPUS using the FFmpeg Batch AV Encoder.

This is a simplified GUI frontend to the ffmpeg encoding framework.

The exact parameters used for lossy podcast episodes are:

-vn -c:a libopus -ac 1 -b:a 32K

(remove any video, use libopus, set stereo to mono, encode at 32K bitrate)

https://ffmpeg-batch.sourceforge.io/

https://ffmpeg.org/

#### Video

MP4 container using AV1 at the original resolution for video, OPUS @ 32 kbps for audio

https://handbrake.fr/

https://ffmpeg-batch.sourceforge.io/