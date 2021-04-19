---
description: Der Windows Media Video 9-Bildschirm Decoder decodiert Datenströme, die vom Windows Media Video 9-Bildschirm Encoder codiert wurden.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Windows Media Video 9-Bildschirm Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9dcdce920fa39437edb769fd575a7d7a0d68fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359364"
---
# <a name="windows-media-video-9-screen-decoder"></a>Windows Media Video 9-Bildschirm Decoder

Der Windows Media Video 9-Bildschirm Decoder decodiert Datenströme, die vom [**Windows Media Video 9-Bildschirm Encoder**](windowsmediavideo9screenencoder.md)codiert wurden.

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) für den Windows Media Video 9-Bildschirm Decoder wird durch die Konstante **CLSID \_ cmsscdecmediaobject** dargestellt. Sie können eine Instanz des Decoders erstellen, indem Sie **CoCreateInstance** aufrufen.

## <a name="input-types"></a>Eingabetypen

Der aus vier Zeichen bestehende Code (FourCC) für Windows Media Video Bildschirm codierten Inhalt der Version 9 ist "MSS2".

Die folgenden Eingabetypen werden vom Bildschirm Decoder der Version 9 unterstützt.

-   Mediasubtype \_ MSS2

## <a name="output-types"></a>Ausgabetypen

Die folgenden Ausgabetypen werden vom Bildschirm Decoder der Version 9 unterstützt, wenn Sie als DirectX-Medienobjekt (DMO) verwendet werden.

-   Mediasubtype \_ RGB24
-   Mediasubtype \_ RGB32
-   Mediasubtype \_ ARGB32
-   Mediasubtype \_ RGB565
-   Mediasubtype \_ RGB555
-   Mediasubtype \_ RGB8

Die folgenden Ausgabetypen werden vom Bildschirm Decoder der Version 9 unterstützt, wenn Sie als Media Foundation Transformation (MFT) verwendet wird.

-   MF-Format \_ RGB24
-   MF-Format \_ RGB32
-   MF-Format \_ ARGB32
-   MF-Format \_ RGB565
-   MF-Format \_ RGB555
-   MF-Format \_ RGB8

## <a name="remarks"></a>Bemerkungen

Ein Bildschirm Decoder-Objekt macht die [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) -Schnittstelle verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und stellt die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann.

Ein Bildschirm Decoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird. In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein Bildschirm Decoder als DMO oder MFT verhält.



| Betriebssystem            | Decoderverhalten                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Ein Windows Media-Bildschirm Decoder verhält sich immer als DMO.                                                                                                                 |
| Windows Vista und Windows 7 | Standardmäßig verhält sich ein Windows Media-Bildschirm Decoder als DMO. Wenn Sie eine [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle auf einem Bildschirm Decoder abrufen, verhält sie sich wie eine MFT. |



 

Sie können die gleiche CLSID (CLSID \_ cmsscdecmediaobject) verwenden, um den Bildschirm Decoder der Version 7 und den Bildschirm Decoder der Version 9 zu erstellen. Der FourCC for Windows Media Video Screen Version 7-codierter Inhalt ist "MSS1". Der Bildschirm Decoder der Version 7 unterstützt den \_ Eingabetyp mediasubtype MSS1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista oder Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsdecd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Codec-Implementierung](codecimplementation.md)
</dt> <dt>

[Verwenden des Windows Media Video 9-Bildschirm Codecs](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Windows Media Video 9-Bildschirm Encoder](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
