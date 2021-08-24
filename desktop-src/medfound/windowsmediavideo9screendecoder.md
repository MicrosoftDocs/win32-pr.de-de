---
description: Der Windows Media Video 9 Screen-Decoder decodiert Streams, die vom Windows Media Video 9 Screen Encoder codiert wurden.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Windows Media Video 9 Screen Decoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c2e081423c4c5efc2d44fdf78c7c6a94a00dae86d40d761a06ab0de07fa5d1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462390"
---
# <a name="windows-media-video-9-screen-decoder"></a>Windows Medienvideo 9-Bildschirmdecoder

Der Windows Media Video 9 Screen-Decoder decodiert Streams, die vom [**Windows Media Video 9 Screen Encoder**](windowsmediavideo9screenencoder.md)codiert wurden.

## <a name="class-identifier"></a>Klassenbezeichner

Der Klassenbezeichner (CLSID) für den Windows Media Video 9 Screen-Decoder wird durch die Konstante **CLSID \_ CMSSCDecMediaObject** dargestellt. Sie können eine Instanz des Decoders erstellen, indem Sie **CoCreateInstance** aufrufen.

## <a name="input-types"></a>Eingabetypen

Der vierstellige Code (FOURCC) für Windows Media Video Screen Version 9-codierter Inhalt ist "MSS2".

Die folgenden Eingabetypen werden vom Bildschirmdecoder der Version 9 unterstützt.

-   MEDIASUBTYPE \_ MSS2

## <a name="output-types"></a>Ausgabetypen

Die folgenden Ausgabetypen werden vom Bildschirmdecoder der Version 9 unterstützt, wenn er als DirectX-Medienobjekt (DMO) verwendet wird.

-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

Die folgenden Ausgabetypen werden vom Bildschirmdecoder der Version 9 unterstützt, wenn er als Media Foundation Transform (MFT) verwendet wird.

-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ ARGB32
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="remarks"></a>Hinweise

Ein Bildschirmdecoderobjekt macht die [**IMediaObject-Schnittstelle**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und macht die [**INTERFACESTransform-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) verfügbar, sodass das Objekt als Media Foundation Transform (MFT) verwendet werden kann.

Ein Bildschirmdecoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird. Die folgende Tabelle zeigt die Bedingungen, unter denen sich ein Bildschirmdecoder als DMO oder MFT verhält.



| Betriebssystem            | Decoderverhalten                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Ein Windows Medienbildschirmdecoder verhält sich immer als DMO.                                                                                                                 |
| Windows Vista und Windows 7 | Standardmäßig verhält sich ein Windows Medienbildschirmdecoder als DMO. Wenn Sie eine [**DECODERTransform-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in einem Bildschirmdecoder erhalten, verhält sie sich wie ein MFT. |



 

Sie können dieselbe CLSID (CLSID \_ CMSSCDecMediaObject) verwenden, um den Bildschirmdecoder der Version 7 und den Bildschirmdecoder der Version 9 zu erstellen. FOURCC für Windows Media Video Screen Version 7-codierter Inhalt ist "MSS1". Der Bildschirmdecoder der Version 7 unterstützt den MEDIASUBTYPE \_ MSS1-Eingabetyp.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista oder Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsdecd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Codecimplementierung](codecimplementation.md)
</dt> <dt>

[Verwenden des Windows Media Video 9-Bildschirmcodecs](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Windows Media Video 9 Screen Encoder](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
