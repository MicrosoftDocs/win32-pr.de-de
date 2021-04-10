---
title: Provider-Element (systempropertiestype)
description: Identifiziert den Anbieter, der das Ereignis protokolliert hat.
ms.assetid: 4560c938-4e2a-40d5-97f9-85a38141ac8f
keywords:
- Anbieter Element-Ereignisprotokoll
topic_type:
- apiref
api_name:
- Provider
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3dc6ae072ed6491915067bea4395a1a84369b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040261"
---
# <a name="provider-systempropertiestype-element"></a>Provider-Element (systempropertiestype)

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

Das **Provider** -Element wird durch den komplexen [**systempropertiestype**](eventschema-systempropertiestype-complextype.md) -Typ definiert.

## <a name="attributes"></a>Attributes



| Name            | type                                                | BESCHREIBUNG                                                                                                                                        |
|-----------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| EventSourceName | Zeichenfolge                                              | Der Name der Ereignis Quelle, die das Ereignis veröffentlicht hat (wenn die Ereignis Quelle von der Legacy- [Ereignisprotokollierungs](/windows/desktop/EventLog/event-logging) -API stammt).<br/> |
| GUID            | [**Guidtype**](eventschema-guidtype-simpletype.md) | Der Globally Unique Identifier, der den Anbieter eindeutig identifiziert.<br/>                                                                   |
| Name            | anyURI                                              | Der Name des Ereignis Anbieters, der das Ereignis protokolliert hat.<br/>                                                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**System (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

