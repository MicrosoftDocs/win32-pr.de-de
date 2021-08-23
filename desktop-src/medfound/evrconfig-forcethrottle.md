---
description: Erzwingt, dass der Enhanced Video Renderer (EVR) seine Ausgabe an die GPU-Bandbreite angrenzt.
ms.assetid: e81e67d6-aa72-44c1-90e9-72ab18bca1c9
title: EVRConfig_ForceThrottle -Attribut (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad09d0c3133039975a04a026ec84233987dfd4033b120a4b8fc6272e2fd72b9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346140"
---
# <a name="evrconfig_forcethrottle-attribute"></a>EVRConfig \_ ForceThrottle-Attribut

Erzwingt, dass der Enhanced Video Renderer (EVR) seine Ausgabe an die GPU-Bandbreite angrenzt.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Dieses Attribut kann für die EVR-Mediensenke festgelegt werden. Verwenden Sie zum Festlegen des Attributs **IUnknown::QueryInterface,** um die EVR-Mediensenke für die [**SCHNITTSTELLE ATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) abfragt.

Das Festlegen dieses Attributs hat die gleiche Auswirkung wie das Festlegen des **Flags "MFVideoRenderPrefs \_ ForceOutputThrottling"** auf der EVR. Eine Beschreibung dieses Flags finden Sie unter [**MFVideoRenderPrefs.**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs)

Die GUID-Konstante für dieses Attribut wird aus strmiids.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Uuids.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[EVR-Attribute](enhanced-video-renderer-attributes.md)
</dt> <dt>

[VideoQualitätsverwaltung](video-quality-management.md)
</dt> </dl>

 

 




