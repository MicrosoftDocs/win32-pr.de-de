---
description: Der Windows Media MPEG4 V1/V2-Decoder decodiert die Videostreams von MPEG4 v1/v2.
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: Windows Media MPEG4 V1/V2-Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b14cf22e29c1266ac9bb3593375ee4485d79df2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106365224"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a>Windows Media MPEG4 V1/V2-Decoder

Der Windows Media MPEG4 V1/V2-Decoder decodiert die Videostreams von MPEG4 v1/v2.

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) für den Windows Media MPEG4 V1/V2-Decoder wird durch die Konstante **CLSID \_ CMpeg4DecMediaObject** dargestellt. Sie können eine Instanz des MPEG4 V1/V2-Decoders erstellen, indem Sie **CoCreateInstance** aufrufen.

## <a name="formats"></a>Formate

Der Windows Media MPEG4 V1/V2-Decoder unterstützt die folgenden Eingabemedien Typen.

-   Mediasubtype \_ MPG4
-   Mediasubtype \_ MPG4
-   Mediasubtype \_ MP42
-   Mediasubtype \_ mp42

Der Windows Media MPEG4 V1/V2-Decoder unterstützt die folgenden Ausgabemedien-Untertypen, wenn er als DirectX-Medienobjekt (DMO) fungiert.

-   Mediasubtype \_ im YUY2
-   mediasubtype \_ UYVY
-   Mediasubtype \_ RGB32
-   Mediasubtype \_ RGB24
-   Mediasubtype \_ RGB565
-   Mediasubtype \_ RGB8
-   Mediasubtype \_ RGB555

Der Windows Media MPEG4 V1/V2-Decoder unterstützt die folgenden Ausgabemedien-Untertypen, wenn er als Media Foundation Transformation (MFT) fungiert.

-   MF-Format \_ im YUY2
-   MF-Format ( \_ UYVY)
-   MF-Format \_ RGB32
-   MF-Format \_ RGB24
-   MF-Format \_ RGB565
-   MF-Format \_ RGB8
-   MF-Format \_ RGB555

## <a name="remarks"></a>Bemerkungen

Das Windows Media MPEG4 V1/V2-Decoderobjekt macht die [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) -Schnittstelle verfügbar, sodass das Objekt als DirectX Media Object (DMO) verwendet werden kann, und stellt die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann. Das-Objekt verfügt über denselben Klassen Bezeichner (CLSID), unabhängig davon, ob er als DMO oder MFT fungiert.

Ein MPEG4 V1/V2-Decoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird. In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein MPEG4 V1/V2-Decoder als DMO oder MFT verhält.



| Betriebssystem            | Decoderverhalten                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Ein MPEG4 V1/V2-Decoder verhält sich immer als DMO.                                                                                                                                 |
| Windows Vista und Windows 7 | Standardmäßig verhält sich ein MPEG4 V1/V2-Decoder als DMO. Wenn Sie in einem MPEG4 V1/V2-Decoder eine Schnittstelle für den [Video Untertyp "GUIDs](video-subtype-guids.md) " erhalten, verhält sie sich wie eine MFT. |



 

Die global eindeutigen Bezeichner (GUIDs) für RGB-Medien Untertypen unterscheiden sich abhängig davon, ob ein Decoder als DMO oder MFT fungiert. Die GUIDs für nicht-RGB-Medien Untertypen sind identisch, unabhängig davon, ob ein Decoder als DMO oder MFT fungiert. Informationen zu den GUIDs, die Video Untertypen darstellen, finden Sie [unter Video Untertyp-GUIDs](video-subtype-guids.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MPG4DECD.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 
