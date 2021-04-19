---
title: messagetable (eventstype)-Element
description: Enthält einen Verweis auf eine Zeichenfolge im Lokalisierungs Abschnitt des Manifests. | messagetable (eventstype)-Element
ms.assetid: 4dcc1afe-8f2b-4baf-b40b-406f60368575
keywords:
- messagetable-Element EventLog
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85ce478fb30389ba911ef9dd76473a6261974f55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366395"
---
# <a name="messagetable-eventstype-element"></a>messagetable (eventstype)-Element

Enthält einen Verweis auf eine Zeichenfolge im Lokalisierungs Abschnitt des Manifests.

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

Das **messagetable** -Element wird durch den komplexen [**eventstype**](eventmanifestschema-eventstype-complextype.md) -Typ definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                             | type | BESCHREIBUNG                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**Nachricht**](eventmanifestschema-message-messagetable-element.md) |      | Gibt einen Verweis auf eine Zeichenfolge im Lokalisierungs Abschnitt des Manifests an.<br/> |



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

[**Events (InstrumentationType)-Element**](eventmanifestschema-events-instrumentationtype-element.md)
</dt> </dl>

 

 





