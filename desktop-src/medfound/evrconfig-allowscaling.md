---
description: Der Erweiterte Videorenderer (EVR) kann das Video in einem Rechteck mischen, das kleiner als das Ausgaberechteck ist, und dann das Ergebnis skalieren.
ms.assetid: 7e3b8fe1-959b-4391-a715-5d5a7a7dda39
title: EVRConfig_AllowScaling -Attribut (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83323c42ac81d4cce0bb42733bd4246959cf0fc9a58b5705579a86aee9b2bd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879424"
---
# <a name="evrconfig_allowscaling-attribute"></a>EVRConfig \_ AllowScaling-Attribut

Der Erweiterte Videorenderer (EVR) kann das Video in einem Rechteck mischen, das kleiner als das Ausgaberechteck ist, und dann das Ergebnis skalieren.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Dieses Attribut kann für die EVR-Mediensenke festgelegt werden. Um das Attribut zu festlegen, verwenden Sie **QueryInterface,** um die EVR-Mediensenke für die [**SCHNITTSTELLE DURCHATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) abfragt.

Das Festlegen dieses Attributs hat die gleiche Auswirkung wie das Festlegen des **MFVideoRenderPrefs-AllowScaling-Flags \_** auf der EVR. Eine Beschreibung dieses Flags finden Sie unter [**MFVideoRenderPrefs.**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs)

Die GUID-Konstante für dieses Attribut wird aus strmiids.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Uuids.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[EVR-Attribute](enhanced-video-renderer-attributes.md)
</dt> <dt>

[VideoQualitätsverwaltung](video-quality-management.md)
</dt> </dl>

 

 




