---
title: messagetable (metadataType)-Element
description: Enthält Verweise auf Zeichen folgen, die im Abschnitt mit den Metadaten des Ereignis Instrumentations Manifests verwendet werden. Die Zeichen folgen werden in einer Gruppe von Nachrichten Elementen und IDs zusammengefasst.
ms.assetid: 868af191-0f9c-435b-878f-ef0584e097d1
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
ms.openlocfilehash: eb5efc261a2c055a95f71ba556c9acbc0ad45373
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103082"
---
# <a name="messagetable-metadatatype-element"></a>messagetable (metadataType)-Element

Enthält Verweise auf Zeichen folgen, die im Abschnitt mit den Metadaten des Ereignis Instrumentations Manifests verwendet werden. Die Zeichen folgen werden in einer Gruppe von [**Nachrichten**](eventmanifestschema-message-messagetable-element.md) Elementen und IDs zusammengefasst.

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

Das **messagetable** -Element wird durch den komplexen [**metadataType**](eventmanifestschema-metadatatype-complextype.md) -Typ definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                             | type | BESCHREIBUNG                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**Nachricht**](eventmanifestschema-message-messagetable-element.md) |      | Gibt einen Verweis auf eine Zeichenfolge im Lokalisierungs Abschnitt des Manifests an.<br/> |



## <a name="attributes"></a>Attributes



| Name    | type   | BESCHREIBUNG                                                              |
|---------|--------|--------------------------------------------------------------------------|
| message | Zeichenfolge | Ein Verweis auf die lokalisierte Zeichenfolge in der Zeichen folgen Tabelle.<br/>      |
| mId     | Zeichenfolge | Nicht verwendet.<br/>                                                     |
| Symbol  | Zeichenfolge | Das Symbol, mit dem auf die Meldung verwiesen wird.<br/>                     |
| value   | Zeichenfolge | Die Zahl, die als Nachrichten-ID für diese Nachricht verwendet werden soll.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**MetadataType**](eventmanifestschema-metadatatype-complextype.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Metadaten (instrumentationmanifest)**](eventmanifestschema-metadata-instrumentationmanifest-element.md)
</dt> </dl>

 

 





