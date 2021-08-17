---
description: Der Windows Media MPEG4 V1/V2-Decoder decodiert MPEG4 V1/V2-Videostreams.
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: Windows Media MPEG4 V1/V2 Decoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c55d5c64cec2a0ad08978064d40c26267d7729adeee9a9f148c8e682ba168509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100932"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a>Windows Media MPEG4 V1/V2-Decoder

Der Windows Media MPEG4 V1/V2-Decoder decodiert MPEG4 V1/V2-Videostreams.

## <a name="class-identifier"></a>Klassenbezeichner

Der Klassenbezeichner (CLSID) für den Windows Media MPEG4 V1/V2-Decoder wird durch die Konstante **CLSID \_ CMpeg4DecMediaObject dargestellt.** Sie können eine Instanz des MPEG4 V1/V2-Decoders erstellen, indem Sie **CoCreateInstance aufrufen.**

## <a name="formats"></a>Formate

Der Windows Media MPEG4 V1/V2-Decoder unterstützt die folgenden Eingabemedientypen.

-   MEDIASUBTYPE \_ MPG4
-   MEDIASUBTYPE \_ mpg4
-   MEDIASUBTYPE \_ MP42
-   MEDIASUBTYPE \_ mp42

Der Windows Media MPEG4 V1/V2-Decoder unterstützt die folgenden Ausgabemedienuntertypen, wenn er als DirectX Media Object (DMO.

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UY WIE
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

Der Windows Media MPEG4 V1/V2-Decoder unterstützt die folgenden Ausgabemedienuntertypen, wenn er als Media Foundation Transform (MFT) agiert.

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UY WIES
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>Hinweise

Das Windows Media MPEG4 V1/V2-Decoderobjekt macht die [**IMediaObject-Schnittstelle**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und macht die [**INTERFACETRANSFORM-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) verfügbar, sodass das Objekt als Media Foundation Transform (MFT) verwendet werden kann. Das Objekt hat denselben Klassenbezeichner (CLSID), unabhängig davon, ob es als DMO oder MFT fungiert.

Ein MPEG4 V1/V2-Decoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie abrufen und welche Version von Windows wird. Die folgende Tabelle zeigt die Bedingungen, unter denen sich ein MPEG4 V1/V2-Decoder wie ein DMO MFT verhält.



| Betriebssystem            | Decoderverhalten                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Ein MPEG4 V1/V2-Decoder verhält sich immer wie ein DMO.                                                                                                                                 |
| Windows Vista und Windows 7 | Standardmäßig verhält sich ein MPEG4 V1/V2-Decoder wie ein DMO. Wenn Sie eine [Video Subtype GUIDs-Schnittstelle](video-subtype-guids.md) für einen MPEG4 V1/V2-Decoder abrufen, verhält sie sich wie ein MFT. |



 

Die GUIDs (Globally Unique Identifiers) für RGB-Medienuntertypen unterscheiden sich abhängig davon, ob ein Decoder als DMO oder MFT agiert. Die GUIDs für Nicht-RGB-Medienuntertypen sind identisch, unabhängig davon, ob ein Decoder als DMO oder MFT agiert. Informationen zu den GUIDs, die Videountertypen darstellen, finden Sie unter [Video Subtype GUIDs](video-subtype-guids.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MPG4DECD.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 
