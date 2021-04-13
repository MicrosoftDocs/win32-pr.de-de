---
description: Zeigt, wie Sie die DXVA-Video Verarbeitung verwenden.
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: DXVA2_VideoProc Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8497a241baf07b76148a5bc2e7ddb4dd5e878e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342498"
---
# <a name="dxva2_videoproc-sample"></a>DXVA2 \_ videoproc-Beispiel

Zeigt, wie Sie die [DXVA-Video Verarbeitung](dxva-video-processing.md)verwenden.

Dieses Beispiel generiert Programm gesteuert Videos mit einem primären Stream und einem substream. Der primäre Stream zeigt SMPTE-Farb leisten an, und der unter Datenstrom ist ein semitransparentes Rechteck. Anschließend wird das Video mithilfe eines DXVA-Video Prozessors verarbeitet und angezeigt. Der Benutzer kann die planaren Alpha Werte, die Quell-und Ziel Rechtecke, Farbanpassungen und den Farbbereich ändern.

![Screenshot des dxva2 \- videoproc-Beispiels](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden DXVA-Schnittstellen veranschaulicht:

-   [**Idirectxvideoprocess-Service**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [**Idirectxvideoprocessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a>Verbrauch

Mit dem DXVA2 \_ videoproc-Beispiel wird eine Windows-Anwendung erstellt.

Befehlszeilenoptionen:



| Option | BESCHREIBUNG                                                                          |
|--------|--------------------------------------------------------------------------------------|
| -hh    | Zwingt die Anwendung, ein Hardware Direct3D Gerät und ein Hardware-DXVA-Gerät zu verwenden. |
| -HS    | Zwingt die Anwendung, ein Hardware Direct3D Gerät und ein DXVA-Software Gerät zu verwenden. |
| -ss    | Zwingt die Anwendung, ein Software Direct3D Gerät und ein DXVA-Software Gerät zu verwenden. |



 

Tastaturbefehle:



| Schlüssel       | BESCHREIBUNG                                             |
|-----------|---------------------------------------------------------|
| ALT+EINGABE | Wechseln zwischen dem Fenstermodus und dem Vollbildmodus.      |
| F1 – F8     | Geben Sie einen der Modi in der folgenden Tabelle ein.    |
| ENDE       | Aktivieren oder Deaktivieren der Debugprotokollierung für gelöschte Frames. |
| POS1      | Setzen Sie einen Parameter auf seinen Anfangswert zurück.                 |



 

Jeder der Funktionstasten (F1 bis F8) wechselt zu einem Modus, in dem die Pfeiltasten zum Anpassen eines bestimmten renderingparameters verwendet werden können. Außerdem wird die Farbe des Substreams geändert.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Schlüssel</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>F1</td>
<td>Passen Sie die Alpha Werte an.<br/>
<ul>
<li>UP: Vergrößern Sie das planare Alpha beider Streams.</li>
<li>Down: verringern Sie den planaren Alpha beider Streams.</li>
<li>Right: Vergrößern Sie das Pixel Alpha des Substreams.</li>
<li>Left: verringern Sie das Pixel Alpha des Substreams.</li>
</ul>
Substreamfarbe: weiß<br/></td>
</tr>
<tr class="even">
<td>F2</td>
<td>Passen Sie den Quellbereich (Zoom) des primären Streams an.<br/>
<ul>
<li>UP: vertikal vergrößern (vergrößern).</li>
<li>Down: Vertikal verkleinern (verkleinern).</li>
<li>Right: horizontal vergrößern (vergrößern).</li>
<li>Left: Horizontal verkleinern (verkleinern).</li>
</ul>
Substreamfarbe: rot<br/></td>
</tr>
<tr class="odd">
<td>F3</td>
<td>Verschieben Sie den Quellbereich des primären Streams.<br/>
<ul>
<li>Aufwärts: nach oben verschieben.</li>
<li>Down: nach unten verschieben.</li>
<li>Right: nach rechts verschieben.</li>
<li>Left: nach links verschieben.</li>
</ul>
Substreamfarbe: gelb<br/></td>
</tr>
<tr class="even">
<td>F4</td>
<td>Passen Sie den Zielbereich des primären Streams an.<br/>
<ul>
<li>UP: vertikal vergrößern.</li>
<li>Down: Vertikal verkleinern.</li>
<li>Right: horizontal vergrößern.</li>
<li>Left: verringern Sie den horizontalen.</li>
</ul>
Substreamfarbe: grün<br/></td>
</tr>
<tr class="odd">
<td>F5</td>
<td>Verschieben Sie den Zielbereich des primären Streams.<br/>
<ul>
<li>Aufwärts: nach oben verschieben.</li>
<li>Down: nach unten verschieben.</li>
<li>Right: nach rechts verschieben.</li>
<li>Left: nach links verschieben.</li>
</ul>
Substreamfarbe: Cyan<br/></td>
</tr>
<tr class="even">
<td>F6</td>
<td>Ändern Sie die Hintergrundfarbe oder den Farb Raum.<br/>
<ul>
<li>Nach oben, nach unten: Durchlaufen von Farbräumen.</li>
<li>Right, Left: Durchlaufen der Hintergrundfarben.</li>
</ul>
Substreamfarbe: blau<br/></td>
</tr>
<tr class="odd">
<td>F7</td>
<td>Anpassen von Helligkeit und Kontrast.<br/>
<ul>
<li>UP: erhöhen Sie die Helligkeit.</li>
<li>Down: Helligkeit verringern.</li>
<li>Right: Vergrößern des kontra stists.</li>
<li>Left: Kontrast verringern.</li>
</ul>
Substreamfarbe: Magenta<br/></td>
</tr>
<tr class="even">
<td>F8</td>
<td>Anpassen von Hue und Sättigung.<br/>
<ul>
<li>UP: erhöhen Sie den Farbton.</li>
<li>Down: verringern Sie den Farbton.</li>
<li>Right: erhöhen Sie die Sättigung.</li>
<li>Left: verringern Sie die Sättigung.</li>
</ul>
Substreamfarbe: schwarz<br/></td>
</tr>
</tbody>
</table>



 

Wenn Sie die Start Taste drücken, werden die Parameter für diesen Modus in jedem Modus auf ihre Anfangswerte zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Video Beschleunigung 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA-Video Verarbeitung](dxva-video-processing.md)
</dt> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




