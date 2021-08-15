---
title: EventID (SystemPropertiesType)-Element
description: Der Bezeichner, den der Anbieter zum Identifizieren des Ereignisses verwendet hat.
ms.assetid: 2d5ac44b-4157-4b87-bd8f-e992e85dd0b1
keywords:
- EventID-Element EventLog
topic_type:
- apiref
api_name:
- EventID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bfc3db28af21f26224433faf299200f4b262cd7583a1cafb27e0e700fdc1d36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055788"
---
# <a name="eventid-systempropertiestype-element"></a>EventID (SystemPropertiesType)-Element

Der Bezeichner, den der Anbieter zum Identifizieren des Ereignisses verwendet hat.

``` syntax
<xs:element name="EventID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedInt"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

Das **EventID-Element** wird vom komplexen [**SystemPropertiesType-Typ**](eventschema-systempropertiestype-complextype.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**System (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





