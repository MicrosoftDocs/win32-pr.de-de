---
description: Bei der Videoprozessor-MFT handelt es sich um eine Microsoft Media Foundation Transformation (MFT), die eine colorspace-Konvertierung, eine Videogröße, eine Deinterlacing, eine Frameraten Konvertierung, Drehung, Zuschneiden, räumliche linke und Rechte Ansicht zum Entpacken und Spiegelung ausführt.
ms.assetid: 1476995A-9692-4B08-8EF7-7DB6321BEC24
title: MFT des Video Prozessors (camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53783b42073414e4dc440546698bf295b404dcc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369254"
---
# <a name="video-processor-mft"></a>MFT des Video Prozessors

Bei der Videoprozessor-MFT handelt es sich um eine Microsoft Media Foundation Transformation (MFT), die eine colorspace-Konvertierung, eine Videogröße, eine Deinterlacing, eine Frameraten Konvertierung, Drehung, Zuschneiden, räumliche linke und Rechte Ansicht zum Entpacken und Spiegelung ausführt.

## <a name="clsid"></a>CLSID

CLSID \_ videoprocess ormft

## <a name="interfaces"></a>Schnittstellen

-   [**Imfrealtimecliumtex**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
-   [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMF videoprocess Control**](/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol)

## <a name="input-formats"></a>Eingabeformate

-   **MF-Format \_ ARGB32**
-   **MF-Format ( \_ ayuv)**
-   **MF-Format \_ I420**
-   **MF-Format ( \_ IYUV)**
-   **MF-Format \_ NV11**
-   **MF-Format \_ NV12**
-   **MF-Format \_ RGB24**
-   **MF-Format \_ RGB32**
-   **MF-Format \_ RGB555**
-   **MF-Format \_ RGB565**
-   **MF-Format \_ RGB8**
-   **MF-Format ( \_ UYVY)**
-   **MF-Format \_ v410**
-   **MF-Format \_ Y216**
-   **MF-Format \_ im y41p**
-   **MF-Format \_ Y41T**
-   **MF-Format \_ Y42T**
-   **MF-Format \_ im YUY2**
-   **MF-Format \_ YV12**
-   **Mfvideoformat \_ yvyu**

## <a name="output-formats"></a>Ausgabeformate

-   **MF-Format \_ ARGB32**
-   **MF-Format ( \_ ayuv)**
-   **MF-Format \_ I420**
-   **MF-Format ( \_ IYUV)**
-   **MF-Format \_ NV12**
-   **MF-Format \_ RGB24**
-   **MF-Format \_ RGB32**
-   **MF-Format \_ RGB555**
-   **MF-Format \_ RGB565**
-   **MF-Format ( \_ UYVY)**
-   **MF-Format \_ Y216**
-   **MF-Format \_ im YUY2**
-   **MF-Format \_ YV12**

Nicht jede Kombination aus Eingabe-und Ausgabeformaten wird unterstützt. Um zu testen, ob eine Konvertierung unterstützt wird, legen Sie den Eingabetyp fest, und klicken Sie dann auf [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).

Weitere Informationen zu diesen Formaten finden Sie [unter Video Untertyp-GUIDs](video-subtype-guids.md).

## <a name="remarks"></a>Bemerkungen

Eine Instanz des Video Prozessors kann auf eine der folgenden Arten erstellt werden:

-   Durch Aufrufen von [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). Der Videoprozessor ist unter der Kategorie " **MFT \_ Category \_ Video \_ Processor** " registriert.
-   Durch Aufrufen der com-Funktion **CoCreateInstance** , die der CLSID- **CLSID \_ videoprocess ormft** übergeben wird.

Die folgenden Hinweise beziehen sich auf die Arbeit mit Quell Rechtecke und Ziel Rechtecke im **Video Prozessor-MFT**. Quell-und Ziel Rechtecke werden mit [**IMF videoprocess orcontrol:: setdestinationrechteck**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) und [**setsourcerectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) und mehrmals mit [**IMF mediaengineex:: updatevideostream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream)festgelegt.

-   Das Quell Rechteck sollte ausgerichtet und gerundet werden, um die Anforderungen des Farb Formats des Frame Abbilds zu erfüllen, der für den Videoprozessor eingegeben wurde. Dies ist wichtig, da Formate wie 420 und 422 Anforderungen an die Dimensionen und Offsets haben, die erstellt werden können und auf die zugegriffen werden kann. Ein Quell Rechteck von {1, 0, 319, 240} (Links, oben, rechts, unten) wird z. b. auf {2, 0, 320, 240} gerundet, wenn das Eingabeformat auf 420 fest steht.
-   Sowohl das Ziel-als auch das Quell Rechteck werden immer an die entsprechenden Frames gebunden – das Quell Rechteck zum Quellframe und das Ziel Rechteck zum Zielframe. Dies bedeutet, dass negative Werte nicht aussagekräftig sind – Sie werden immer an 0 gebunden.
-   Das Quell Rechteck befindet sich im Koordinatensystem des Zielframes abzüglich aller Ziel Rechtecks. Dies bedeutet, dass Transformationen wie die Drehung im Quell Rechteck "Rückgängig" sind. Daher müssen Sie nicht wissen, ob das Video gedreht oder 3D entpackt wurde. Sie könnten z. b. ein Rechteck oberhalb des videotags zeichnen, die relativen Koordinaten (relativ zum videotag) verwenden, diese normalisieren (Bereich zwischen 0 und 1) und Sie als Quell Rechteck weitergeben, und Sie sollten erwartungsgemäß funktionieren, auch wenn das Video gedreht wird.

Der Videoprozessor unterstützt eine GPU-beschleunigte Videoverarbeitung mit Microsoft Direct3D 11. Weitere Informationen finden Sie unter [MF \_ sa \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md).

### <a name="stereoscopic-video"></a>Stereoskopisches Video

Der Videoprozessor unterstützt den Vorgang zum Entpacken der Ansicht auf 3D-Video Frames:

Wenn der Eingabe Rahmen zwei Ansichten enthält, die im gleichen Frame verpackt sind, kann der Videoprozessor die Ansichten in separate Puffer aufteilen oder die Basis Ansicht extrahieren und die zweite Ansicht verwerfen. Um das Entpacken von Ansichten zu aktivieren, legen Sie das [MF-Attribut " \_ \_ 3dvideo- \_ Ausgabe aktivieren](mf-enable-3dvideo-output.md) " auf **MF3DVideoOutputType \_ Stereo** oder **MF3DVideoOutputType \_ baseview** fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Camerauicontrol. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Digitale Signal Prozessoren](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




