---
title: Komplexer namedquerytype-Typ
description: Nicht verwendet. Definiert eine Liste benannter Abfragen, die die Ereignis Meldungs Zeichenfolge nach einem Wert Abfragen und eine angegebene Aktion ausführen, sofern gefunden. | Komplexer namedquerytype-Typ
ms.assetid: 2606094d-ae1b-4a3f-a78f-30659fa141ab
keywords:
- Namedquerytype komplexer Typ EventLog
topic_type:
- apiref
api_name:
- NamedQueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e296847cbed635d88f4fa58efa53fda030affffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365043"
---
# <a name="namedquerytype-complex-type"></a>Komplexer namedquerytype-Typ

Nicht verwendet. Definiert eine Liste benannter Abfragen, die die Ereignis Meldungs Zeichenfolge nach einem Wert Abfragen und eine angegebene Aktion ausführen, sofern gefunden.

``` syntax
<xs:complexType name="NamedQueryType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="patternMaps"
            type="PatternMapListType"
         />
        <xs:any
            processContents="lax"
            maxOccurs="unbounded"
            minOccurs="0"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                       | type                                                                             | BESCHREIBUNG                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**patternmaps**](eventmanifestschema-patternmaps-namedquerytype-element.md) | [**Patternmaplisttype**](eventmanifestschema-patternmaplisttype-complextype.md) | Definiert eine Liste von Paaren für reguläre Ausdrücke, die zum Ändern der Meldungs Zeichenfolge verwendet werden.<br/> |



## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie das [**namedqueries**](eventmanifestschema-namedqueries-metadatatype-element.md) -Element verwendet wird. In diesem Beispiel wird der Inhalt der Meldungs Zeichenfolge in die Zeichenfolge eingefügt https://www .*Messagestring*. com. Anschließend wird die Meldungs Zeichenfolge durch das Ergebnis ersetzt. Wenn die Meldungs Zeichenfolge z. b. Microsoft enthält, würde die Abfrage die Microsoft-Nachrichten Zeichenfolge durch ersetzen https://www.Microsoft.com .


```XML
<namedqueries>
   <patternmap name="SearchStrings" format="winrxv1">
       <map name="/${1}/" value="/http:\/\/www\.*\.com\/"/>
   </patternmap>
</namedqueries>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





