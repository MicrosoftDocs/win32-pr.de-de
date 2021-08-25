---
title: messageTable -Element (MetadataType)
description: Enthält Verweise auf Zeichenfolgen, die im Metadatenabschnitt des Ereignisinstrumentierungsmanifests verwendet werden. Die Zeichenfolgen werden in einer Gruppe von Nachrichtenelementen und IDs gespeichert, die miteinander gekoppelt sind.
ms.assetid: 868af191-0f9c-435b-878f-ef0584e097d1
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
ms.openlocfilehash: f7c614210a22bc6c6d160a7c161c5b5a89aab85116285822465b43ba75e63095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865660"
---
# <a name="messagetable-metadatatype-element"></a>messageTable -Element (MetadataType)

Enthält Verweise auf Zeichenfolgen, die im Metadatenabschnitt des Ereignisinstrumentierungsmanifests verwendet werden. Die Zeichenfolgen werden in einer Gruppe von [**Nachrichtenelementen**](eventmanifestschema-message-messagetable-element.md) und miteinander gekoppelten IDs gespeichert.

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

Das **messageTable-Element** wird vom komplexen [**MetadataType-Typ**](eventmanifestschema-metadatatype-complextype.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                             | type | BESCHREIBUNG                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**Nachricht**](eventmanifestschema-message-messagetable-element.md) |      | Gibt einen Verweis auf eine Zeichenfolge im Lokalisierungsabschnitt des Manifests an.<br/> |



## <a name="attributes"></a>Attributes



| Name    | type   | BESCHREIBUNG                                                              |
|---------|--------|--------------------------------------------------------------------------|
| message | Zeichenfolge | Ein Verweis auf die lokalisierte Zeichenfolge in der Zeichenfolgentabelle.<br/>      |
| mId     | Zeichenfolge | Wird nicht verwendet.<br/>                                                     |
| Symbol  | Zeichenfolge | Das Symbol, das verwendet wird, um auf die Nachricht zu verweisen.<br/>                     |
| value   | Zeichenfolge | Die Zahl, die als Nachrichtenbezeichner für diese Nachricht verwendet werden soll.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**MetadataType**](eventmanifestschema-metadatatype-complextype.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**metadata (instrumentationManifest)**](eventmanifestschema-metadata-instrumentationmanifest-element.md)
</dt> </dl>

 

 





