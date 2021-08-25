---
description: Ermöglicht dem Erweiterten Videorenderer (Enhanced Video Renderer, EVR), die Leistung zu verbessern, indem das zweite Feld jedes geschachtelten Frames übersprungen wird.
ms.assetid: de7efc6a-19ae-4f3a-8675-38fda3c979e2
title: EVRConfig_AllowDropToHalfInterlace-Attribut (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cfae2bf47e71d1c6cb7dbed60069a79f56cee3249c362acf6c0efc99dc06f55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828150"
---
# <a name="evrconfig_allowdroptohalfinterlace-attribute"></a>EVRConfig \_ AllowDropToHalfInterlace-Attribut

Ermöglicht dem Erweiterten Videorenderer (Enhanced Video Renderer, EVR), die Leistung zu verbessern, indem das zweite Feld jedes geschachtelten Frames übersprungen wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Dieses Attribut kann für die EVR-Mediensenke festgelegt werden. Um das Attribut festzulegen, verwenden Sie **QueryInterface,** um die EVR-Mediensenke für die [**SCHNITTSTELLE "ATTRIBUTESAttributes"**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) abzufragen.

Das Festlegen dieses Attributs hat die gleiche Auswirkung wie das Festlegen des **MFVideoMixPrefs \_ AllowDropToHalfInterlace-Flags** auf der EVR. Eine Beschreibung dieses Flags finden Sie unter [**MFVideoMixPrefs.**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs)

Die GUID-Konstante für dieses Attribut wird aus strmiids.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Uuids.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[EVR-Attribute](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Videoqualitätsverwaltung](video-quality-management.md)
</dt> </dl>

 

 




