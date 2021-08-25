---
description: Zeigt die Verwendung der DXVA-Videoverarbeitung.
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: DXVA2_VideoProc Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160fda9829398b97e7670bb2d1f8cc076c00cda77e1ad06131603603f6f49191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828285"
---
# <a name="dxva2_videoproc-sample"></a>DXVA2 \_ VideoProc-Beispiel

Zeigt, wie [DXVA Video Processing verwendet wird.](dxva-video-processing.md)

In diesem Beispiel wird programmgesteuert ein Video mit einem primären Stream und einem Unterstream generiert. Der primäre Stream zeigt SMPTE-Farbbalken an, und der Unterstream ist ein halbtransparentes Rechteck. Das Video wird dann mithilfe eines DXVA-Videoprozessors verarbeitet und angezeigt. Der Benutzer kann die planaren Alphawerte, Quell- und Zielrechtecke, Farbanpassungen und den Farbraum ändern.

![Screenshot des \- dxva2-Videoproc-Beispiels](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden DXVA-Schnittstellen veranschaulicht:

-   [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a>Verbrauch

Das DXVA2 \_ VideoProc-Beispiel erstellt eine Windows Anwendung.

Befehlszeilenoptionen:



| Option | Beschreibung                                                                          |
|--------|--------------------------------------------------------------------------------------|
| -hh    | Erzwingt, dass die Anwendung ein Direct3D-Hardwaregerät und ein DXVA-Hardwaregerät verwendet. |
| -hs    | Zwingt die Anwendung, ein Direct3D-Hardwaregerät und ein DXVA-Softwaregerät zu verwenden. |
| -ss    | Zwingt die Anwendung, ein Direct3D-Softwaregerät und ein DXVA-Softwaregerät zu verwenden. |



 

Tastaturbefehle:



| Key       | Beschreibung                                             |
|-----------|---------------------------------------------------------|
| ALT+EINGABE | Wechseln Sie zwischen dem Fenstermodus und dem Vollbildmodus.      |
| F1–F8     | Geben Sie einen der in der folgenden Tabelle gezeigten Modi ein.    |
| ENDE       | Aktivieren oder deaktivieren Sie die Debugprotokollierung für gelöschte Frames. |
| POS1      | Setzen Sie einen Parameter auf seinen Anfangswert zurück.                 |



 

Jede der Funktionstasten F1 bis F8 wechselt in einen Modus, in dem die Pfeiltasten verwendet werden können, um einen bestimmten Renderingparameter anzupassen. Darüber hinaus ändert sich die Farbe des Unterstreams.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Key</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>F1</td>
<td>Passen Sie die Alphawerte an.<br/>
<ul>
<li>UP: Erhöhen Sie den planaren Alphawert beider Streams.</li>
<li>DOWN: Verringern Sie den planaren Alphawert beider Datenströme.</li>
<li>RIGHT: Erhöhen Sie das Pixel alpha des Unterstreams.</li>
<li>LEFT: Verringern Sie das Pixel alpha des Unterstreams.</li>
</ul>
Unterstreamfarbe: Weiß<br/></td>
</tr>
<tr class="even">
<td>F2</td>
<td>Passen Sie den Quellbereich des primären Streams an (Zoom).<br/>
<ul>
<li>NACH OBEN: Vertikal erhöhen (Vergrößern).</li>
<li>DOWN: Vertikal verkleinern (verkleinern).</li>
<li>RIGHT: Horizontal erhöhen (Vergrößern).</li>
<li>LEFT: Horizontal verkleinern (verkleinern).</li>
</ul>
Unterstreamfarbe: Rot<br/></td>
</tr>
<tr class="odd">
<td>F3</td>
<td>Verschieben Sie den Quellbereich des primären Streams.<br/>
<ul>
<li>NACH OBEN: Nach oben.</li>
<li>NACH UNTEN: Nach unten.</li>
<li>RIGHT: Nach rechts verschieben.</li>
<li>LEFT: Nach links verschieben.</li>
</ul>
Unterstreamfarbe: Gelb<br/></td>
</tr>
<tr class="even">
<td>F4</td>
<td>Passen Sie den Zielbereich des primären Streams an.<br/>
<ul>
<li>UP: Vertikal erhöhen.</li>
<li>DOWN: Vertikal verringern.</li>
<li>RIGHT: Horizontal erhöhen.</li>
<li>LEFT: Horizontal verringern.</li>
</ul>
Unterstreamfarbe: Grün<br/></td>
</tr>
<tr class="odd">
<td>F5</td>
<td>Verschieben Sie den Zielbereich des primären Streams.<br/>
<ul>
<li>NACH OBEN: Nach oben.</li>
<li>NACH UNTEN: Nach unten.</li>
<li>RIGHT: Nach rechts verschieben.</li>
<li>LEFT: Nach links verschieben.</li>
</ul>
Unterstreamfarbe: Cyan<br/></td>
</tr>
<tr class="even">
<td>F6</td>
<td>Ändern Sie die Hintergrundfarbe oder den Farbraum.<br/>
<ul>
<li>UP, DOWN: Durchknaben von Farbräumen.</li>
<li>RIGHT, LEFT: Durchfing die Hintergrundfarben.</li>
</ul>
Substreamfarbe: Blau<br/></td>
</tr>
<tr class="odd">
<td>F7</td>
<td>Passen Sie Helligkeit und Kontrast an.<br/>
<ul>
<li>UP: Erhöhen Sie die Helligkeit.</li>
<li>DOWN: Helligkeit verringern.</li>
<li>RIGHT: Erhöhen Sie den Kontrast.</li>
<li>LEFT: Kontrast verringern.</li>
</ul>
Unterstreamfarbe: Magenta<br/></td>
</tr>
<tr class="even">
<td>F8</td>
<td>Anpassen von Farbton und Sättigung.<br/>
<ul>
<li>NACH OBEN: Erhöhen Sie den Farbton.</li>
<li>DOWN: Verringern Sie den Farbton.</li>
<li>RIGHT: Erhöhen Sie die Sättigung.</li>
<li>LEFT: Sättigung verringern.</li>
</ul>
Unterstreamfarbe: Schwarz<br/></td>
</tr>
</tbody>
</table>



 

In jedem Modus setzt das Drücken der HOME-Taste die Parameter für diesen Modus auf ihre Anfangswerte zurück.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [github-Repository Windows klassischen Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA-Videoverarbeitung](dxva-video-processing.md)
</dt> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




