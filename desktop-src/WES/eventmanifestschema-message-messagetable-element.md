---
title: message (messageTable)-Element
description: Enthält einen Verweis auf eine Zeichenfolge im Lokalisierungsabschnitt des Manifests. | message (messageTable)-Element
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- Message-Element EventLog
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79020fa18717a3a2338a8ac243bb95e0fa14de47f0e434fb52c475c956afa101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865670"
---
# <a name="message-messagetable-element"></a>message (messageTable)-Element

Enthält einen Verweis auf eine Zeichenfolge im Lokalisierungsabschnitt des Manifests.

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

Das **message-Element** wird durch das [**messageTable-Element**](eventmanifestschema-messagetable-instrumentationtype-element.md) definiert.

## <a name="attributes"></a>Attributes



| Name    | type   | BESCHREIBUNG                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| message | Zeichenfolge | Ein Verweis auf die lokalisierte Zeichenfolge in der Zeichenfolgentabelle.<br/>                                |
| mId     | Zeichenfolge | Wird nicht verwendet.<br/>                                                                               |
| Symbol  | Zeichenfolge | Der symbolische Name, den der Nachrichtencompiler für diese Meldungszeichenfolge erstellen soll.<br/> |
| value   | Zeichenfolge | Die Zahl, die als Nachrichtenbezeichner für diese Nachricht verwendet werden soll.<br/>                           |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnete Elemente**
</dt> <dt>

[**messageTable (EventsType)**](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[**messageTable (MetadataType)**](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





