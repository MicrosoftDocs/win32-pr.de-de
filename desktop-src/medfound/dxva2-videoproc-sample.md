---
description: Zeigt die Verwendung der DXVA-Videoverarbeitung.
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: DXVA2_VideoProc Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc4be1bad6a3955af255cb083a4595ecedfd30
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473926"
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



| Option | BESCHREIBUNG                                                                          |
|--------|--------------------------------------------------------------------------------------|
| -hh    | Erzwingt, dass die Anwendung ein Direct3D-Hardwaregerät und ein DXVA-Hardwaregerät verwendet. |
| -hs    | Zwingt die Anwendung, ein Direct3D-Hardwaregerät und ein DXVA-Softwaregerät zu verwenden. |
| -ss    | Zwingt die Anwendung, ein Direct3D-Softwaregerät und ein DXVA-Softwaregerät zu verwenden. |



 

Tastaturbefehle:



| Schlüssel       | BESCHREIBUNG                                             |
|-----------|---------------------------------------------------------|
| ALT+EINGABE | Wechseln Sie zwischen dem Fenstermodus und dem Vollbildmodus.      |
| F1–F8     | Geben Sie einen der in der folgenden Tabelle gezeigten Modi ein.    |
| ENDE       | Aktivieren oder deaktivieren Sie die Debugprotokollierung für gelöschte Frames. |
| POS1      | Setzen Sie einen Parameter auf seinen Anfangswert zurück.                 |



 

Jede der Funktionstasten F1 bis F8 wechselt in einen Modus, in dem die Pfeiltasten verwendet werden können, um einen bestimmten Renderingparameter anzupassen. Darüber hinaus ändert sich die Farbe des Unterstreams.




| Schlüssel | BESCHREIBUNG | 
|-----|-------------|
| F1 | Passen Sie die Alphawerte an.<br /><ul><li>UP: Erhöhen Sie den planaren Alphawert beider Streams.</li><li>DOWN: Verringern Sie den planaren Alphawert beider Streams.</li><li>RIGHT: Erhöhen Sie das Pixel alpha des Unterstreams.</li><li>LEFT: Verringern Sie das Pixel alpha des Unterstreams.</li></ul>Unterstreamfarbe: Weiß<br /> | 
| F2 | Passen Sie den Quellbereich des primären Streams an (Zoom).<br /><ul><li>NACH OBEN: Vertikal erhöhen (Vergrößern).</li><li>DOWN: Vertikal verkleinern (verkleinern).</li><li>RIGHT: Horizontal erhöhen (Vergrößern).</li><li>LEFT: Horizontal verkleinern (verkleinern).</li></ul>Unterstreamfarbe: Rot<br /> | 
| F3 | Verschieben Sie den Quellbereich des primären Streams.<br /><ul><li>NACH OBEN: Nach oben.</li><li>NACH UNTEN: Nach unten.</li><li>RIGHT: Nach rechts verschieben.</li><li>LEFT: Nach links verschieben.</li></ul>Unterstreamfarbe: Gelb<br /> | 
| F4 | Passen Sie den Zielbereich des primären Streams an.<br /><ul><li>UP: Vertikal erhöhen.</li><li>DOWN: Vertikal verringern.</li><li>RIGHT: Horizontal erhöhen.</li><li>LEFT: Horizontal verringern.</li></ul>Unterstreamfarbe: Grün<br /> | 
| F5 | Verschieben Sie den Zielbereich des primären Streams.<br /><ul><li>NACH OBEN: Nach oben.</li><li>NACH UNTEN: Nach unten.</li><li>RIGHT: Nach rechts verschieben.</li><li>LEFT: Nach links verschieben.</li></ul>Unterstreamfarbe: Cyan<br /> | 
| F6 | Ändern Sie die Hintergrundfarbe oder den Farbraum.<br /><ul><li>UP, DOWN: Durchknaben von Farbräumen.</li><li>RIGHT, LEFT: Durchfing die Hintergrundfarben.</li></ul>Substreamfarbe: Blau<br /> | 
| F7 | Passen Sie Helligkeit und Kontrast an.<br /><ul><li>UP: Erhöhen Sie die Helligkeit.</li><li>DOWN: Helligkeit verringern.</li><li>RIGHT: Erhöhen Sie den Kontrast.</li><li>LEFT: Kontrast verringern.</li></ul>Unterstreamfarbe: Magenta<br /> | 
| F8 | Anpassen von Farbton und Sättigung.<br /><ul><li>NACH OBEN: Erhöhen Sie den Farbton.</li><li>DOWN: Verringern Sie den Farbton.</li><li>RIGHT: Erhöhen Sie die Sättigung.</li><li>LEFT: Sättigung verringern.</li></ul>Unterstreamfarbe: Schwarz<br /> | 




 

In jedem Modus setzt das Drücken der HOME-Taste die Parameter für diesen Modus auf ihre Anfangswerte zurück.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository Windows klassischen Beispielen verfügbar.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Videobeschleunigung 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA-Videoverarbeitung](dxva-video-processing.md)
</dt> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




