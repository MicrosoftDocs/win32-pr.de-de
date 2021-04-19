---
title: Komplexer StructDefinitionType-Typ
description: Definiert eine-Struktur, die ein oder mehrere Datenelemente enthält, die Sie mit dem-Ereignis einschließen möchten. | Komplexer StructDefinitionType-Typ
ms.assetid: eb6b3682-1035-472b-8027-583d43c31748
keywords:
- StructDefinitionType komplexer Typ (Ereignisprotokoll)
topic_type:
- apiref
api_name:
- StructDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 01e739077d38dec94c0a407e5779bec90369ffb9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366406"
---
# <a name="structdefinitiontype-complex-type"></a>Komplexer StructDefinitionType-Typ

Definiert eine-Struktur, die ein oder mehrere Datenelemente enthält, die Sie mit dem-Ereignis einschließen möchten.

``` syntax
<xs:complexType name="StructDefinitionType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="data"
            type="DataDefinitionType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="length"
        type="LengthType"
        use="optional"
     />
    <xs:attribute name="count"
        type="CountType"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                               | type                                                                             | BESCHREIBUNG                                                               |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**Vorrats**](eventmanifestschema-data-structdefinitiontype-element.md) | [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md) | Definiert ein Datenelement, das Sie in die Struktur einschließen möchten.<br/> |



## <a name="attributes"></a>Attributes



| Name   | type                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count  | [**"Count Type"**](eventmanifestschema-counttype-simpletype.md)   | Die Anzahl der Elemente in einem Array von-Strukturen. Dieses Attribut gibt an, dass die Struktur ein Array von Strukturen definiert. Sie können die tatsächliche Anzahl oder den Namen eines Datenelements außerhalb der Struktur angeben, die die Anzahl enthält. <br/>                               |
| length | [**Längen-Typ**](eventmanifestschema-lengthtype-simpletype.md) | Nicht verfügbar.<br/> **Windows Server 2008 und Windows Vista:** Die Länge dieser-Struktur in Bytes. Ab Windows 7 nicht verfügbar.<br/>                                                                                                                            |
| name   | Zeichenfolge                                                          | Der Name der-Struktur. Sie können den Namen verwenden, um auf das Datenelement in Ihrem XML-Fragment zu verweisen, wenn Sie einen [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) -Abschnitt in ihrer Vorlage angeben.<br/> **Windows Vista:** Dieses Attribut ist optional.<br/> |



## <a name="remarks"></a>Bemerkungen

Anbieter schreiben die Struktur als BLOB und nicht als einzelne Member der Struktur. Wenn die C-Struktur, die Sie schreiben, Zeiger enthält (z. b. ein Zeiger vom Typ LPWSTR), enthalten die Ereignisdaten den Zeiger Wert, nicht die dereferenzierten Daten.

Strukturen sollten nicht verwendet werden, stattdessen sollten Sie für jedes Elementdaten Elemente definieren und diese separat schreiben. Wenn Sie sich dafür entscheiden, die Struktur zu verwenden, sollte die Struktur nur ganzzahlige Typen enthalten, und Sie müssen sicherstellen, dass die Elemente der Struktur an einer 8-Byte-Grenze ausgerichtet sind. Wenn Sie dies nicht tun, erhalten Sie wahrscheinlich Ausrichtungsfehler, wenn Sie versuchen, auf die Daten zuzugreifen. Verwenden Sie die \# pragma pack ()-Direktive, um die Ausrichtung an einer 8-Byte-Grenze zu erzwingen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





