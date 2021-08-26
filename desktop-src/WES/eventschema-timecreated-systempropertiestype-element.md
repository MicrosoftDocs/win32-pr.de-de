---
title: TimeCreated (SystemPropertiesType)-Element
description: Der Zeitstempel, der identifiziert, wann das Ereignis protokolliert wurde.
ms.assetid: 16b2b71b-078e-4862-b1be-ef7cec315bc5
keywords:
- TimeCreated-Element – EventLog
topic_type:
- apiref
api_name:
- TimeCreated
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5026bed56e3e065a403c0e6076daa0ec478223c4d742db0a35109a41cc98d5c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005300"
---
# <a name="timecreated-systempropertiestype-element"></a>TimeCreated (SystemPropertiesType)-Element

Der Zeitstempel, der identifiziert, wann das Ereignis protokolliert wurde.

``` syntax
<xs:element name="TimeCreated">
    <xs:complexType>
        <xs:attribute name="SystemTime"
            type="dateTime"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

Das **TimeCreated-Element** wird durch den komplexen [**SystemPropertiesType-Typ**](eventschema-systempropertiestype-complextype.md) definiert.

## <a name="attributes"></a>Attributes



| Name       | type     | BESCHREIBUNG                                              |
|------------|----------|----------------------------------------------------------|
| SystemTime | dateTime | Die Systemzeit, zu der das Ereignis protokolliert wurde.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**System (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





