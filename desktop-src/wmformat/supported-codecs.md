---
title: Unterstützte Codecs
description: Unterstützte Codecs
ms.assetid: d5907d38-2e26-442e-a0d1-1d7e267b9948
keywords:
- Windows Media-Format-SDK, unterstützte Codecs
- Windows Media-Format-SDK, IWMCodecInfo3-Schnittstelle
- Codecs, unterstützt
- IWMCodecInfo3, Informationen zu
- Codecs, IWMCodecInfo3-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac06ad3d58d066254fa666f96283dca9b8b6ae
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723589"
---
# <a name="supported-codecs"></a>Unterstützte Codecs

Das Windows Media-Format SDK bietet Unterstützung für die folgenden Codecs, die bei der Installation des SDK enthalten sind.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Codec</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Media Audio</td>
<td>Audiocodec zur allgemeinen Verwendung bei der Codierung komplexer Audiodaten, z. b. für Musik. Die neuesten Versionen dieses Codecs sind der Windows Media Audio 9-Codec und der Windows Media Audio 9,1-Codec.<br/></td>
</tr>
<tr class="even">
<td>Windows Media Audio Professional</td>
<td>Audiocodec für komplexe Audiodaten, wie z. b. Musik. Unterstützt die Multichannel-und 24-Bit-Codierung. Es gibt zwei Versionen dieses Codecs:<br/>
<ul>
<li>Windows Media Audio 9 Professional</li>
<li>Windows Media Audio 9,1 Professional</li>
</ul></td>
</tr>
<tr class="odd">
<td>Verlust von Windows Media Audio Verlust</td>
<td>Audiocodec für Verlust lose Codierung. Es gibt zwei Versionen dieses Codecs:<br/>
<ul>
<li>Windows Media Audio 9 verlustfreier</li>
<li>Windows Media Audio 9,1 verlustfreie</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows Media Audio 9-Stimme</td>
<td>Audiocodec, der für die Codierung der menschlichen Stimme bei hohen Komprimierungs Verhältnissen optimiert ist. Dies ist der bevorzugte Codec für Streams, die größtenteils aus gesprochenen Wörtern bestehen. Für Inhalte, die gemischte Musik und Sprache sind, kann dieser Codec den Codierungs Algorithmus dynamisch ändern, der zum Erzielen optimaler Qualität verwendet wird.</td>
</tr>
<tr class="odd">
<td>Windows Media Video 9</td>
<td>Videocodec zur allgemeinen Verwendung bei der Codierung komplexer Videos, z. b. Filme.</td>
</tr>
<tr class="even">
<td>Erweiterte profile Windows Media Video 9</td>
<td>Videocodec, der erweiterte Codierungs Funktionen enthält, einschließlich Zeilen Sprung Codierung.</td>
</tr>
<tr class="odd">
<td>Windows Media Video 9-Bildschirm</td>
<td>Videocodec für die Codierung sequenzieller Screenshots optimiert. Dieser Codec wird häufig für Software Schulungen oder-Unterstützung verwendet, indem Überwachungs Images aufgezeichnet werden, wenn Computeranwendungen verwendet werden.</td>
</tr>
<tr class="even">
<td>Bild Windows Media Video</td>
<td>Videocodec zum wandeln von Bitmapbildern mit demarkerinformationen in komprimiertes Video. Es gibt zwei Versionen dieses Codecs:<br/>
<ul>
<li>Bild Windows Media Video 9</li>
<li>Windows Media Video 9 Abbild v2</li>
</ul></td>
</tr>
</tbody>
</table>



 

Abhängig von der Version des Windows Media-Format-SDKs, das Sie installieren, sind verschiedene Versionen der Windows Media Audio-und Video Codecs für die Codierung verfügbar. Wenn Sie die-Methoden verwenden, wenn die [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) -Schnittstelle zum Auflisten von Codecs und Codec-Formaten verwendet wird, werden nur die neuesten unterstützten Versionen aufgelistet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Auswählen einer Codierungsmethode**](choosing-an-encoding-method.md)
</dt> <dt>

[**Codec-Features**](codec-features.md)
</dt> </dl>

 

 





