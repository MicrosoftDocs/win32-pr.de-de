---
title: Komplexer StructDefinitionType-Typ
description: Definiert eine -Struktur, die ein oder mehrere Datenelemente enthält, die In das Ereignis eingeschlossen werden soll. | Komplexer StructDefinitionType-Typ
ms.assetid: eb6b3682-1035-472b-8027-583d43c31748
keywords:
- Komplexer StructDefinitionType-Typ EventLog
topic_type:
- apiref
api_name:
- StructDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 035b8abe5440ffb80b902e1f4b1564b2fb80b77ee34b20f4f068d298b251478a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124250"
---
# <a name="structdefinitiontype-complex-type"></a>Komplexer StructDefinitionType-Typ

Definiert eine -Struktur, die ein oder mehrere Datenelemente enthält, die In das Ereignis eingeschlossen werden soll.

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



| Element                                                               | type                                                                             | Beschreibung                                                               |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**Daten**](eventmanifestschema-data-structdefinitiontype-element.md) | [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md) | Definiert ein Datenelement, das Sie in die -Struktur ein-/ausdingen möchten.<br/> |



## <a name="attributes"></a>Attributes



| Name   | type                                                            | Beschreibung                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count  | [**CountType**](eventmanifestschema-counttype-simpletype.md)   | Die Anzahl der Elemente in einem Array von -Strukturen. Dieses Attribut gibt an, dass die -Struktur ein Array von -Strukturen definiert. Sie können die tatsächliche Anzahl oder den Namen eines Datenelements außerhalb der Struktur angeben, die die Anzahl enthält. <br/>                               |
| length | [**LengthType**](eventmanifestschema-lengthtype-simpletype.md) | Nicht verfügbar.<br/> **Windows Server 2008 und Windows Vista:** Die Länge dieser -Struktur in Bytes. Ab 7 Windows nicht mehr verfügbar.<br/>                                                                                                                            |
| name   | Zeichenfolge                                                          | Der Name der -Struktur. Sie können den Namen verwenden, um auf das Datenelement in Ihrem XML-Fragment zu verweisen, wenn Sie einen [**UserData-Abschnitt**](eventmanifestschema-userdata-templateitemtype-element.md) in Ihrer Vorlage angeben.<br/> **Windows Vista:** Dieses Attribut ist optional.<br/> |



## <a name="remarks"></a>Hinweise

Anbieter schreiben die Struktur als Blob und nicht als einzelne Member der Struktur. Wenn die C-Struktur, die Sie schreiben, Zeiger enthält (z. B. ein Zeiger vom Typ LPWSTR), enthalten die Ereignisdaten den Zeigerwert, nicht die dereferenzierten Daten.

Sie sollten keine Strukturen verwenden, sondern Datenelemente für jedes Member definieren und separat schreiben. Wenn Sie sich für die Verwendung der -Struktur entscheiden, sollte die -Struktur nur integrale Typen enthalten, und Sie müssen sicherstellen, dass die Member der -Struktur an einer 8-Byte-Grenze ausgerichtet sind. Anderst erhalten Sie wahrscheinlich Ausrichtungsfehler, wenn Sie versuchen, auf die Daten zu zugreifen. Erwägen Sie die \# Verwendung der pragma pack()-Direktive, um die Ausrichtung an einer 8-Byte-Grenze zu erzwingen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





