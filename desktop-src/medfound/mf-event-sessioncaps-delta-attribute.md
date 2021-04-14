---
description: Enthält Flags, die angeben, welche Funktionen in der Medien Sitzung basierend auf der aktuellen Präsentation geändert wurden.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: MF_EVENT_SESSIONCAPS_DELTA-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284a31a8d3fc661c15e7de991972455468efbd40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393533"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a>\_Delta-Ereignis \_ sessioncaps- \_ Delta Attribut

Enthält Flags, die angeben, welche Funktionen in der Medien Sitzung basierend auf der aktuellen Präsentation geändert wurden.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut enthält eine Bitmaske, die angibt, welche Funktionen Flags geändert haben. Eine Liste möglicher Flags finden Sie unter [**imfmediasession:: gezession-Funktionen**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities). Bits werden aus folgenden Gründen in der Bitmaske auf 1 festgelegt:

-   Das entsprechende Funktionen-Bit wurde von 0 in 1 geändert.
-   Das entsprechende Funktionen-Bit wurde von 1 in 0 geändert.
-   Das entsprechende Funktionen-Bit blieb 1, aber die Details der Funktion wurden geändert. Beispielsweise wurde die maximale Wiedergabe Rate geändert.

Dieses Attribut wird mit dem [mesessioncapabilitieschge](mesessioncapabilitieschanged.md) -Ereignis verwendet.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Ereignisattribute](event-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




