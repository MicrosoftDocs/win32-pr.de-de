---
description: Der Windows Media MPEG-4 V3-Decoder decodiert MPEG-4 V3-Videostreams.
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: Windows Media MPEG-4 V3-Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ee98a0a3c4b221da6f2000e32d4c75bc3e3a93b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355714"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a>Windows Media MPEG-4 V3-Decoder

Der Windows Media MPEG-4 V3-Decoder decodiert MPEG-4 V3-Videostreams.

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) für den Windows MPEG-4 V3-Decoder wird durch die Konstante **CLSID \_ CMpeg43DecMediaObject** dargestellt. Sie können eine Instanz des MPEG-4 V3-Decoders erstellen, indem Sie **CoCreateInstance** aufrufen.

## <a name="formats"></a>Formate

Der Windows Media MPEG-4 V3-Decoder unterstützt die folgenden Eingabemedien Typen.

-   Mediasubtype \_ MP43
-   Mediasubtype \_ MP43

Der Windows Media MPEG-4 V3-Decoder unterstützt die folgenden Ausgabemedien-Untertypen, wenn er als DirectX-Medienobjekt (DMO) fungiert.

-   Mediasubtype \_ im YUY2
-   mediasubtype \_ UYVY
-   Mediasubtype \_ RGB32
-   Mediasubtype \_ RGB24
-   Mediasubtype \_ RGB565
-   Mediasubtype \_ RGB8
-   Mediasubtype \_ RGB555

Der Windows Media MPEG-4 V3-Decoder unterstützt die folgenden Ausgabemedien-Untertypen, wenn er als Media Foundation Transformation (MFT) fungiert.

-   MF-Format \_ im YUY2
-   MF-Format ( \_ UYVY)
-   MF-Format \_ RGB32
-   MF-Format \_ RGB24
-   MF-Format \_ RGB565
-   MF-Format \_ RGB8
-   MF-Format \_ RGB555

## <a name="remarks"></a>Bemerkungen

Das Windows Media MPEG-4 V3-Decoder-Objekt macht die [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) -Schnittstelle verfügbar, sodass das Objekt als DirectX Media Object (DMO) verwendet werden kann, und stellt die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann. Das-Objekt verfügt über denselben Klassen Bezeichner (CLSID), unabhängig davon, ob er als DMO oder MFT fungiert.

Der MPEG-4 V3-Decoder verhält sich je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird, als DMO oder MFT. In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein MPEG-4 V3-Decoder als DMO oder MFT verhält.



| Betriebssystem            | Decoderverhalten                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Der MPEG-4 V3-Decoder verhält sich immer als DMO.                                                                                                                      |
| Windows Vista und Windows 7 | Standardmäßig verhält sich der MPEG-4 V3-Decoder als DMO. Wenn Sie eine [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle für den MPEG-4 V3-Decoder erhalten, verhält sie sich wie eine MFT. |



 

Die global eindeutigen Bezeichner (GUIDs) für RGB-Medien Untertypen unterscheiden sich abhängig davon, ob ein Decoder als DMO oder MFT fungiert. Die GUIDs für nicht-RGB-Medien Untertypen sind identisch, unabhängig davon, ob ein Decoder als DMO oder MFT fungiert. Informationen zu den GUIDs, die Medien Untertypen darstellen, finden Sie [unter Video Untertyp-GUIDs](video-subtype-guids.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MP43DECD.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 
