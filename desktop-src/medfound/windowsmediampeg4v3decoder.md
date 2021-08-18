---
description: Der Windows Media MPEG-4 V3-Decoder decodiert MPEG-4 V3-Videostreams.
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: Windows Media MPEG-4 V3 Decoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 975351d04b0876b5f1793d442e41d54a585062bd1fed778902fee5c4c83dcd6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100916"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a>Windows Mpeg-4 V3-Mediendecoder

Der Windows Media MPEG-4 V3-Decoder decodiert MPEG-4 V3-Videostreams.

## <a name="class-identifier"></a>Klassenbezeichner

Der Klassenbezeichner (CLSID) für den Windows MPEG-4 V3-Decoder wird durch die Konstante **CLSID \_ CMpeg43DecMediaObject dargestellt.** Sie können eine Instanz des MPEG-4 V3-Decoders erstellen, indem Sie **CoCreateInstance aufrufen.**

## <a name="formats"></a>Formate

Der Windows Media MPEG-4 V3-Decoder unterstützt die folgenden Eingabemedientypen.

-   MEDIASUBTYPE \_ MP43
-   MEDIASUBTYPE \_ mp43

Der Windows Media MPEG-4 V3-Decoder unterstützt die folgenden Ausgabemedienuntertypen, wenn er als DirectX Media Object (DMO.

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UY WIE
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

Der Windows Media MPEG-4 V3-Decoder unterstützt die folgenden Ausgabemedienuntertypen, wenn er als Media Foundation Transform (MFT) agiert.

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UY WIES
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>Hinweise

Das Windows Media MPEG-4 V3-Decoderobjekt macht die [**IMediaObject-Schnittstelle**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und macht die [**INTERFACETRANSFORM-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) verfügbar, sodass das Objekt als Media Foundation Transform (MFT) verwendet werden kann. Das Objekt hat denselben Klassenbezeichner (CLSID), unabhängig davon, ob es als DMO oder MFT fungiert.

Der MPEG-4 V3-Decoder verhält sich wie DMO oder MFT, je nachdem, welche Schnittstellen Sie abrufen und welche Version Windows wird. Die folgende Tabelle zeigt die Bedingungen, unter denen sich ein MPEG-4 V3-Decoder als DMO MFT verhält.



| Betriebssystem            | Decoderverhalten                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Der MPEG-4 V3-Decoder verhält sich immer wie ein DMO.                                                                                                                      |
| Windows Vista und Windows 7 | Standardmäßig verhält sich der MPEG-4 V3-Decoder wie DMO. Wenn Sie im MPEG-4 V3-Decoder eine [**BERTRANSFORM-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) abrufen, verhält sie sich wie ein MFT. |



 

Die GUIDs (Globally Unique Identifiers) für RGB-Medienuntertypen unterscheiden sich abhängig davon, ob ein Decoder als DMO oder MFT agiert. Die GUIDs für Nicht-RGB-Medienuntertypen sind identisch, unabhängig davon, ob ein Decoder als DMO oder MFT agiert. Informationen zu den GUIDs, die Medienuntertypen darstellen, finden Sie unter [Video Subtype GUIDs](video-subtype-guids.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MP43DECD.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 
