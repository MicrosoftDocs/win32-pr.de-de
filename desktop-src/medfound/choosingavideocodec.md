---
description: Auswählen eines Videocodecs
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Auswählen eines Videocodecs (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9186c7e7e60f5822ec2e50e3e5c7e16e96b91839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214339"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a>Auswählen eines Videocodecs (Microsoft Media Foundation)

Der Windows Media Video 9-Encoder unterstützt drei Kategorien codierter Ausgabe: Hauptprofil, erweitertes Profil und Image. Die Hauptprofil Kategorie bietet allgemeine Video Komprimierung für komplexe Videoinhalte, z. b. Filme oder Musikvideos. Die Features des Haupt Profils bieten eine große Bandbreite an Codierungs Einstellungen. Sie können das Hauptprofil verwenden, um Videos mit sehr niedrigen Bitraten für die Übermittlung auf handgehaltenen Geräten zu erstellen, oder am anderen Ende des Spektrums können Sie es verwenden, um Videos mit hoher Definition für digitales Kino zu erstellen.

Der Schwerpunkt der Codierungs Algorithmen im Hauptprofil liegt auf dynamischen Videoinhalten, Sie sind jedoch auch für andere Videoinhalte geeignet. Das Hauptprofil sollte die Standard Kategorie für Videoinhalte sein. Um bestimmte Anforderungen zu erfüllen, können Sie die Kategorie "Erweiterter Profil", die Kategorie "Image" oder einen separaten Encoder namens "Windows Media Video 9 Screen Encoder" verwenden. In der folgenden Tabelle sind die vier Optionen aufgeführt.



<table>
<thead>
<tr class="header">
<th>Zweck</th>
<th>Codec</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Allgemeine Videocodierung</td>
<td><a href="windowsmediavideo9encoder.md">Windows Media Video 9-Encoder</a><dl> Profil: Main<br />
</dl></td>
</tr>
<tr class="even">
<td>Codieren von High Definition-Videos oder-Videos, die dem SMPTE-Standard von VC-1 Advanced Profile entsprechen</td>
<td><a href="windowsmediavideo9encoder.md">Windows Media Video 9-Encoder</a><dl> Erweitertes Profil<br />
</dl></td>
</tr>
<tr class="odd">
<td>Wandeln von Bitmapbildern in dynamisches Video</td>
<td><a href="windowsmediavideo9encoder.md">Windows Media Video 9-Encoder</a><dl> Image<br />
</dl></td>
</tr>
<tr class="even">
<td>Codieren von Computern: Anwendungs Video (Bildschirmaufnahme) oder andere hoch statische Videos</td>
<td><a href="windowsmediavideo9screenencoder.md"><strong>Windows Media Video 9-Bildschirm Encoder</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 



