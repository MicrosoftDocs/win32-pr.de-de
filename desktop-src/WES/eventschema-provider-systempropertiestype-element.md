---
title: Provider (SystemPropertiesType)-Element
description: Identifiziert den Anbieter, der das Ereignis protokolliert hat.
ms.assetid: 4560c938-4e2a-40d5-97f9-85a38141ac8f
keywords:
- Provider-Element EventLog
topic_type:
- apiref
api_name:
- Provider
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5327bc267272942df30044678a96244d957122c9fbf7878a805bfd48433e20c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904524"
---
# <a name="provider-systempropertiestype-element"></a>Provider (SystemPropertiesType)-Element

Identifiziert den Anbieter, der das Ereignis protokolliert hat.

``` syntax
<xs:element name="Provider">
    <xs:complexType>
        <xs:attribute name="Name"
            type="anyURI"
            use="optional"
         />
        <xs:attribute name="Guid"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="EventSourceName"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

Das **Provider-Element** wird durch den komplexen [**SystemPropertiesType-Typ**](eventschema-systempropertiestype-complextype.md) definiert.

## <a name="attributes"></a>Attributes



| Name            | type                                                | BESCHREIBUNG                                                                                                                                        |
|-----------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| EventSourceName | Zeichenfolge                                              | Der Name der Ereignisquelle, die das Ereignis veröffentlicht hat (wenn die Ereignisquelle von der [Legacy-Ereignisprotokollierungs-API stammt).](/windows/desktop/EventLog/event-logging)<br/> |
| Guid            | [**GUIDType**](eventschema-guidtype-simpletype.md) | Der global eindeutige Bezeichner, der den Anbieter eindeutig identifiziert.<br/>                                                                   |
| Name            | anyURI                                              | Der Name des Ereignisanbieters, der das Ereignis protokolliert hat.<br/>                                                                                   |



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

 

