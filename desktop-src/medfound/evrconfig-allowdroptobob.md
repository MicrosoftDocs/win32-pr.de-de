---
description: Ermöglicht es dem Enhanced Video Renderer (EVR), die Leistung mithilfe von Bob-Deinterlacing zu verbessern.
ms.assetid: e145e862-b987-4962-a94b-f8370bbcd5ac
title: EVRConfig_AllowDropToBob -Attribut (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dea0dc405f746ad6bbcd37e5bf5428e1f50b5e32049e10c71a196b461f03f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974479"
---
# <a name="evrconfig_allowdroptobob-attribute"></a>\_EVRConfig-Attribut "AllowDropToBob"

Ermöglicht es dem Enhanced Video Renderer (EVR), die Leistung mithilfe von Bob-Deinterlacing zu verbessern.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Dieses Attribut kann für die EVRmedia-Senke festgelegt werden. Um das -Attribut fest zu legen, **queryInterface,** um die EVR-Mediensenke für die [**BENUTZEROBERFLÄCHEAttributes-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) abfragt.

Das Festlegen dieses Attributs hat die gleiche Auswirkung wie das Festlegen des **MFVideoMixPrefs-Flags \_ AllowDropToBob** auf der EVR. Eine Beschreibung dieses Flags finden Sie unter [**MFVideoMixPrefs.**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs)

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

 

 




