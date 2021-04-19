---
title: Message (messagetable)-Element
description: Enthält einen Verweis auf eine Zeichenfolge im Lokalisierungs Abschnitt des Manifests. | Message (messagetable)-Element
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- Message-Element-Ereignisprotokoll
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e1165e3a613434fb76befb87cd1a83ed3af95d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363072"
---
# <a name="message-messagetable-element"></a>Message (messagetable)-Element

Enthält einen Verweis auf eine Zeichenfolge im Lokalisierungs Abschnitt des Manifests.

``` syntax
<xs:element name="message">
    <xs:complexType>
        <xs:attribute name="value"
            type="string"
            use="required"
         />
        <xs:attribute name="mid"
            type="string"
            use="optional"
         />
        <xs:attribute name="message"
            type="string"
            use="required"
         />
        <xs:attribute name="symbol"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

Das **Message** -Element wird durch das [**messagetable**](eventmanifestschema-messagetable-instrumentationtype-element.md) -Element definiert.

## <a name="attributes"></a>Attributes



| Name    | type   | BESCHREIBUNG                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| message | Zeichenfolge | Ein Verweis auf die lokalisierte Zeichenfolge in der Zeichen folgen Tabelle.<br/>                                |
| mId     | Zeichenfolge | Nicht verwendet.<br/>                                                                               |
| Symbol  | Zeichenfolge | Der symbolische Name, den der Nachrichten Compiler für diese Meldungs Zeichenfolge erstellen soll.<br/> |
| value   | Zeichenfolge | Die Zahl, die als Nachrichten-ID für diese Nachricht verwendet werden soll.<br/>                           |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnete Elemente**
</dt> <dt>

[**messagetable (eventstype)**](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[**messagetable (metadataType)**](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





