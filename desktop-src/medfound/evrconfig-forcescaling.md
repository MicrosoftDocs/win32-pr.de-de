---
description: Zwingt den Enhanced Video Renderer (EVR), das Video innerhalb eines Rechtecks zu mischen, das kleiner als das Ausgaberechteck ist, und skaliert dann das Ergebnis.
ms.assetid: f85c4114-ac94-4deb-a1cf-896209079f8b
title: EVRConfig_ForceScaling-Attribut (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd85fa67af3cea27564400b86cf6c8e32e3c15645cbb4f84cc97344fbab9ef60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346200"
---
# <a name="evrconfig_forcescaling-attribute"></a>EVRConfig \_ ForceScaling-Attribut

Zwingt den Enhanced Video Renderer (EVR), das Video innerhalb eines Rechtecks zu mischen, das kleiner als das Ausgaberechteck ist, und skaliert dann das Ergebnis.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Dieses Attribut kann für die EVR-Mediensenke festgelegt werden. Um das Attribut festzulegen, verwenden Sie **QueryInterface,** um die EVR-Mediensenke für die [**SCHNITTSTELLE "ATTRIBUTESAttributes"**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) abzufragen.

Das Festlegen dieses Attributs hat die gleiche Auswirkung wie das Festlegen des **Flags MFVideoRenderPrefs \_ ForceScaling** auf der EVR. Eine Beschreibung dieses Flags finden Sie unter [**MFVideoRenderPrefs.**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs)

Die GUID-Konstante für dieses Attribut wird aus strmiids.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Uuids.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[EVR-Attribute](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Videoqualitätsverwaltung](video-quality-management.md)
</dt> </dl>

 

 




