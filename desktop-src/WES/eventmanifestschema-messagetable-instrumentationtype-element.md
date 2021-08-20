---
title: messageTable(EventsType)-Element
description: Enthält einen Verweis auf eine Zeichenfolge im Lokalisierungsabschnitt des Manifests. | messageTable(EventsType)-Element
ms.assetid: 4dcc1afe-8f2b-4baf-b40b-406f60368575
keywords:
- messageTable-Element EventLog
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5a2bcf374e336047deaa1339ac749fde3fa7c4f27b38e046f6c9bc651c0e0ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120889"
---
# <a name="messagetable-eventstype-element"></a>messageTable(EventsType)-Element

Enthält einen Verweis auf eine Zeichenfolge im Lokalisierungsabschnitt des Manifests.

``` syntax
<xs:element name="messageTable">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="message"
                minOccurs="0"
                maxOccurs="unbounded"
            >
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Das **messageTable-Element** wird durch den komplexen [**EventsType-Typ**](eventmanifestschema-eventstype-complextype.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                             | Typ | Beschreibung                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**Nachricht**](eventmanifestschema-message-messagetable-element.md) |      | Gibt einen Verweis auf eine Zeichenfolge im Lokalisierungsabschnitt des Manifests an.<br/> |



## <a name="attributes"></a>Attributes



| Name    | Typ   | Beschreibung                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| message | Zeichenfolge | Ein Verweis auf die lokalisierte Zeichenfolge in der Zeichenfolgentabelle.<br/>                                |
| mId     | Zeichenfolge | Wird nicht verwendet.<br/>                                                                               |
| Symbol  | Zeichenfolge | Der symbolische Name, den der Nachrichtencompiler für diese Meldungszeichenfolge erstellen soll.<br/> |
| value   | Zeichenfolge | Die Zahl, die als Nachrichtenbezeichner für diese Nachricht verwendet werden soll.<br/>                           |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnete Elemente**
</dt> <dt>

[**events(InstrumentationType)-Element**](eventmanifestschema-events-instrumentationtype-element.md)
</dt> </dl>

 

 





