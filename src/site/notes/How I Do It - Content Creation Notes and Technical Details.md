---
{"dg-publish":true,"permalink":"/how-i-do-it-content-creation-notes-and-technical-details/","pinned":true}
---


### Resources Notes

This project uses open standards, with simplicity, ease of accessibility, sensible defaults and privacy emphasised.

All software recommended will be the most secure option practical, with simpler alternatives provided. 

Older content is in the process of being updated and brought into conformity with these standards.

For any questions please email thewordsmithspeaks@pm.me

#### All Software and Services Used

- Passwords are handled through Bitwarden
- Two Factor Authentication through Authy
- Email is handled through Protonmail
- Scheduling is handled through Proton Calendar
- Documents are written in CommonMark and stored in plain text files in an Obsidian Notes Vault located in the Resources Folder
- Payments are handled through a Wise Business Account
- Buttondown for the Newsletter, switching to a simple email list in ProtonMail is a future plan to improve privacy protections
- Website Domains are held in Njalla

Website - LocalWP app using the free GeneratePress Theme, then using the free Simply Static Plugin to export a static version to Github which is then rendered by Netlify. Provides a simple GUI to design, plus free from end to end and all the benefits of a static website including free hosting. 

Resources Folder - Using the secure Filen service as a base, then a Google Drive Link for redundancy and user preference. A monthly file snapshot is shared using qBittorrent and the opentrackr.org tracker.

Erotic and Safe-For-Work Audios - Recorded on my phones built-in microphone (usually), then transferred by Filen to desktop computer, edited in OcenAudio and exported as Lossless FLAC for archival purposes and 128Kpbs AAC for use using FFMPEG Batch Encoder (green icon with a white line in it). [https://soundgasm.net/](https://soundgasm.net/)to stream audio files directly to people through the browser.

Podcast - Used to be on Anchor before they were bought out by Spotify, now it's on there and shared via RSS to other providers.

Digital Garden - Hosted in an Obsidian Notes Vault located in the Resources Folder, then shared for free using the https://github.com/oleeskild/Obsidian-Digital-Garden plugin, and hosted in Github and rendered on Vercel. Free end to end.

There are lots of other ways to do it. If you are interested, I have conducted a massive in-depth study of the hypnokink content distribution ecosystem. Message me on Signal and I'll share my conclusions with you

#### Commitment to Data Longevity

All content is distributed in ONLY open formats, with delivery methods having multiple failovers and redundancies.

There is the direct download link on Filen, and monthly torrent snapshots as well as a Google Drive Backup Link.

I encourage you to download your own copy of the resources folder and share it with anyone you wish.

Audio is formatted as OPUS format for lossy, and FLAC for lossless. Video as AV1. Documents as Plaintext, formatted in CommonMark, or as LibreOffice-compatible Open Document Format (ODF) and Portable Document Format (PDF) where needed.

#### Communications

All communications are conducted over anonymous, zero-knowledge-encrypted, end-to-end-encrypted connections only.

Texting, Audio Messages and Voice Calls are through Signal.

Email is through ProtonMail.

https://signal.org/

https://proton.me/

#### Writing

All documents are published as text files in UTF encoding in the "source files" subdirectory, then published as a PDF.

All documents are written in CommonMark, a simple, human-readable, strongly defined and highly compatible open version of MarkDown.

Any documents requiring more advanced formatting are published in Open Document Format (ODF) then exported to PDF.

https://obsidian.md/

https://commonmark.org/

I am currently experimenting with the Typst typesetting system as a possible, scalable alternative.

#### Audio

All audio is encoded as either Lossless FLAC, or lossy OPUS using FFmpeg Batch AV Encoder.

This is a simplified GUI frontend to the ffmpeg encoding framework.

The exact parameters used for podcast episodes are:

-vn -c:a libopus -ac 1 -b:a 32K

(remove any video, use libopus, set stereo to mono, encode at 32K bitrate)

https://ffmpeg-batch.sourceforge.io/

https://ffmpeg.org/

#### Video

MP4 container using AV1 at the original resolution for video, OPUS @ 32 kbps for audio

https://handbrake.fr/

https://ffmpeg-batch.sourceforge.io/

#### Standard Process for Content Creation

 1. Clarify the Intention of what you want to create. If it isn't written down it isn't real. 
 2. Create a Brand and Identity.
 3. Get an email address.
 4. Create Group Chat for your supporters.
 5. Create your Content. 
 6. Register for Filesharing Account.
 7. Create Website.
 8. Create Reddit / Fetlife or other social media account to popularise.

#### Keys to Success

Focus on Intention and answer the Content Creation Questions:

- What is it intended to do?
- Who is it for?
- How will I know when it’s done?

Avoid Drama. Do not make a publicly accessible Discord server. Do not allow known Hypnokink Troublemakers (See List) to access your content.

Be true to yourself and your inner voice when it comes to who you are and what unique contributions you have to make to the world :-) Do not allow anyone else to make the decisions or do the thinking for you. Seek help and advice from people BEFORE you need it, but remember that you are under no obligation to follow it. 

#### Audio Recording - Software and Hardware including Example Setups

**Intention**

Create an extremely simple list covering the hardware and software useful to create your own recordings. Voice techniques and recording content are covered separately.

**Quickstart**

**Software**

Use Ocenaudio for recording and editing audio. Hook it up with Waves Clarity Vx for background Noise Cancellation.

**Hardware**

The best microphone is the one that you have on you. Using your phone is completely fine. An excellent midrange microphone is AudioTechnica AT2020USB+ or Blue Microphones Yeti. For a Recording setup you will need a Microphone, a Pop Filter and a Microphone Stand (to hold the Microphone).

#### My Exact Setup

Summary - Record on iPhone using Voice Memos built-in app. Upload to computer using Filen. Edit in Ocenaudio. Move to another Filen folder for distribution.

For spontaneous, non-scripted audios I use my iPhone with the Voice Memos app and an uncompressed file format - you can change this in the settings, then compress down for publication once on your computer.

For scripted audios I use a AudioTechnica AT2020USB+ with this stand and popfilter. Editing in Ocenaudio, importing into Audacity only if I want to add background music, then export to a Filen folder for distribution.

**Eliminating Background Noise FROM recordings**

Buy a license to Waves Clarity Vx Plugin. Note that Pro version is not needed, just the basic version.

Open Ocenaudio, add plugin and add the folder location below. It will pick up Waveshell, in Mono and Stereo versions.

Windows:
64 - bit — **C:\Program Files\VSTPlugins**
32 - bit — **C:\Program Files (x86)\VSTPlugins**
Mac: **Macintosh HD > Library > Audio > Plugins > VST**

Make recordings.
Run Plugin and tweak to reduce noise.
Publish

**Eliminating Background Noise WHILE recording**

A little trickier but basically the same.

Download and install Waves Clarity Vx, run it through LightHost, then use Voicemeeter to connect all your virtual inputs together so your recording / streaming software can connect to it and record. Buy a license to Waves Clarity Vx Plugin. Note that Pro version is not needed, just the basic version.

Download and run LightHost
Run the right version 32 or 64 bit and RUN AS ADMINISTRATOR

https://github.com/rolandoislas/LightHost/releases

Add the location Folder and Scan to show up plugins
Turn the plugin on

During installation, the WaveShell-VST is placed in these default locations:

Windows:
64 - bit — **C:\Program Files\VSTPlugins**
32 - bit — **C:\Program Files (x86)\VSTPlugins**
Mac: **Macintosh HD > Library > Audio > Plugins > VST**

Install Voicemeeter and connect up inputs

https://vb-audio.com/Voicemeeter/

Open Ocenaudio or Audacity and record from that input

#### Master List of all Software and Hardware

**Software**

Inputs - https://vb-audio.com/Cable/index.htm

Mixing - https://vb-audio.com/
Mixing - https://vb-audio.com/Voicemeeter/ - RECOMMENDED

Eliminating Noise - https://www.waves.com/
Eliminating Noise - https://www.waves.com/plugins/clarity-vx - Basic, very affordable
Eliminating Noise - https://www.waves.com/plugins/clarity-vx-pro - Advanced, expensive

Recording and Editing - https://www.audacityteam.org/
Recording and Editing - https://www.ocenaudio.com/ - RECOMMENDED

#### Audio Editing Resources

With all credit to TheSecretSubject at https://www.keepittrancey.com/

Audio Resource List Helpful Tip Resources: 10 Tips for Better Sounding Vocal Recordings for Beginners (FAQ Series) https://www.youtube.com/watch?v=Ty8YLqOmbV

How To Set Your Microphone's Gain / Level for Beginners (FAQ Series) https://www.youtube.com/watch?v=1l86SOlxyps

E & E Sound Guide! By Mister E and Ellechemy https://twitter.com/MisterEAudio/status/1286815677068636160?s=

Finding the Right Mic! https://www.bandrewscott.com/findtherightmic

Where I Watch Mic Review Videos! https://www.youtube.com/channel/UCvOU-zTlankT-JjN3ZzvuKA

Budget Room Treatment Tips! https://www.youtube.com/watch?v=7h84lrQQTl

PRO Asmr Tips (Sound) by Gentle Whisper ASMR https://www.youtube.com/watch?v=nzpwbPwWWEs&t=1167s

PRO Asmr Tips (Video) by Gentle Whisper ASMR https://www.youtube.com/watch?v=85gsEPZl0a

A Comprehensive ASMR Microphone Guide (Zoom H5, Rode NT1, NT5 & 3DIO Tingle Test) https://www.youtube.com/watch?v=euyWwz9nfOs

How to EQ https://blog.landr.com/eq-basics-everything-musicians-need-know-eq/

Getting PRO Level Audio with Audacity Editing https://www.youtube.com/watch?v=TYF5ytMDFpA&t=101s