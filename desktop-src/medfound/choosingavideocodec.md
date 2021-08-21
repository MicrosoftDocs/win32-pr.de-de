---
description: Auswählen eines Videocodecs
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Auswählen eines Videocodecs (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b560666ddeebb88fc3bb720cbc9f1be26308e7ecd8a4ad872fbb1f0991826fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035368"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a>Auswählen eines Videocodecs (Microsoft Media Foundation)

Der Windows Media Video 9 Encoder unterstützt drei Kategorien codierter Ausgabe: Hauptprofil, Erweitertes Profil und Bild. Die Kategorie Hauptprofil bietet allgemeine Videokomprimierung für komplexe Videoinhalte wie Filme oder Musikvideos. Die Features des Hauptprofils bieten eine Vielzahl von Codierungseinstellungen. Sie können das Hauptprofil verwenden, um Videos mit sehr niedrigen Bitraten für die Übermittlung auf Smartphones zu erstellen, oder am anderen Ende des Spektrums können Sie es verwenden, um High-Definition-Video für digitale Automaten zu erstellen.

Der Schwerpunkt der Codierungsalgorithmen im Hauptprofil liegt auf dynamischen Videoinhalten, aber sie eignen sich auch für andere Videoinhalte. Das Hauptprofil sollte Ihre Standardkategorie für Videoinhalte sein. Um bestimmte Anforderungen zu erfüllen, können Sie die Kategorie Erweitertes Profil, die Kategorie Bild oder einen separaten Encoder namens Windows Media Video 9-Bildschirmencoder verwenden. In der folgenden Tabelle sind die vier Optionen aufgeführt.



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
<td><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a><dl> Profil: Main<br />
</dl></td>
</tr>
<tr class="even">
<td>Codieren von High Definition-Videos oder Videos, die dem ADVANCED Profile SMPTE-Standard von VC-1 entsprechen</td>
<td><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a><dl> Erweitertes Profil<br />
</dl></td>
</tr>
<tr class="odd">
<td>Konvertieren von Bitmapbildern in dynamische Videos</td>
<td><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a><dl> Image<br />
</dl></td>
</tr>
<tr class="even">
<td>Codieren von Computeranwendungsvideos (Bildschirmaufnahme) oder anderen hoch statischen Videos</td>
<td><a href="windowsmediavideo9screenencoder.md"><strong>Windows Media Video 9 Screen Encoder</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 



