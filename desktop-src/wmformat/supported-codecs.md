---
title: Unterstützte Codecs
description: Unterstützte Codecs
ms.assetid: d5907d38-2e26-442e-a0d1-1d7e267b9948
keywords:
- Windows Medienformat-SDK, unterstützte Codecs
- Windows Medienformat-SDK, IWMCodecInfo3-Schnittstelle
- Codecs, unterstützt
- IWMCodecInfo3,About
- codecs,IWMCodecInfo3-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12734c73145b13a02c0b97cab283e0ba104d37f41592b5d55d64bb2502101302
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006590"
---
# <a name="supported-codecs"></a>Unterstützte Codecs

Das Windows Media Format SDK bietet Unterstützung für die folgenden Codecs, die bei der Installation des SDK enthalten sind.



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
<td>Audiocodec für die allgemeine Verwendung bei der Codierung komplexer Audiodaten, z. B. Musik. Die neuesten Versionen dieses Codecs sind der Windows Media Audio 9-Codec und der Windows Media Audio 9.1-Codec.<br/></td>
</tr>
<tr class="even">
<td>Windows Medienaudio Professional</td>
<td>Audiocodec für komplexe Audiodaten, z. B. Musik. Unterstützt Multichannel- und 24-Bit-Codierung. Es gibt zwei Versionen dieses Codecs:<br/>
<ul>
<li>Windows Media Audio 9 Professional</li>
<li>Windows Media Audio 9.1 Professional</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows Medienaudio verlustfrei</td>
<td>Audiocodec für verlustfreie Codierung. Es gibt zwei Versionen dieses Codecs:<br/>
<ul>
<li>Windows Media Audio 9 – verlustfrei</li>
<li>Windows Medienaudio 9.1 Verlustlos</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows Media Audio 9 Voice</td>
<td>Audiocodec, der für die Codierung der menschlichen Stimme mit hohen Komprimierungsverhältnissen optimiert ist. Dies ist der bevorzugte Codec für Streams, die größtenteils aus gesprochenen Wörtern bestehen. Bei Inhalten mit gemischter Musik und Sprache kann dieser Codec den Codierungsalgorithmus, der verwendet wird, dynamisch ändern, um eine optimale Qualität zu erzielen.</td>
</tr>
<tr class="odd">
<td>Windows Medienvideo 9</td>
<td>Videocodec für die allgemeine Verwendung bei der Codierung komplexer Videos, z. B. Filme.</td>
</tr>
<tr class="even">
<td>Windows Media Video 9 – Erweitertes Profil</td>
<td>Videocodec mit erweiterten Codierungsfunktionen, einschließlich Interlacingcodierung.</td>
</tr>
<tr class="odd">
<td>Windows Bildschirm "Medienvideo 9"</td>
<td>Für die Codierung sequenzieller Screenshots optimierter Videocodec. Dieser Codec wird häufig für Softwaretraining oder -unterstützung verwendet, indem Überwachungsbilder aufgezeichnet werden, während Computeranwendungen verwendet werden.</td>
</tr>
<tr class="even">
<td>Windows Medienvideobild</td>
<td>Videocodec zum Konvertieren von Bitmapbildern mit Infodaten in komprimierte Videos. Es gibt zwei Versionen dieses Codecs:<br/>
<ul>
<li>Windows Video 9-Medienbild</li>
<li>Windows Media Video 9 Image v2</li>
</ul></td>
</tr>
</tbody>
</table>



 

Je nach Version des Windows Media Format SDK, das Sie installieren, stehen verschiedene Versionen der Windows Medienaudio- und Videocodecs für die Codierung zur Verfügung. Wenn Sie die Methoden verwenden, wenn die [**IWMCodecInfo3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) zum Auflisten von Codecs und Codecformaten verwendet wird, werden nur die neuesten unterstützten Versionen aufgeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Auswählen einer Codierungsmethode**](choosing-an-encoding-method.md)
</dt> <dt>

[**Codecfunktionen**](codec-features.md)
</dt> </dl>

 

 





