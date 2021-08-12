---
title: Komplexer DataDefinitionType-Typ
description: Definiert ein Datenelement, das Sie in das Ereignis ein-/ausdingen möchten. | Komplexer DataDefinitionType-Typ
ms.assetid: f4234e54-a5a8-48e4-941f-05107dcd3f88
keywords:
- Komplexer DataDefinitionType-Typ EventLog
topic_type:
- apiref
api_name:
- DataDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa492acf00740b0df9b761c40797ec05feb5b2e38b84ec0682296dd845cbe613
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589605"
---
# <a name="datadefinitiontype-complex-type"></a>Komplexer DataDefinitionType-Typ

Definiert ein Datenelement, das Sie in das Ereignis ein-/ausdingen möchten.

``` syntax
<xs:complexType name="DataDefinitionType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="inType"
                type="QName"
                use="required"
             />
            <xs:attribute name="outType"
                type="QName"
                use="optional"
             />
            <xs:attribute name="map"
                type="string"
                use="optional"
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
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributes



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>Typ</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>count</td>
<td><a href="eventmanifestschema-counttype-simpletype.md"><strong>CountType</strong></a></td>
<td>Die Anzahl der Elemente im Array, wenn das Datenelement ein Array ist. Sie können die tatsächliche Anzahl oder den Namen eines anderen Datenelements angeben, das die Anzahl enthält. <br/></td>
</tr>
<tr class="even">
<td>inType</td>
<td><strong>QName</strong></td>
<td>Der Datentyp für dieses Datenelement. Eine Liste der vordefinierten Eingabedatentypen finden Sie unter Dem komplexen <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType-Typ.</strong></a><br/></td>
</tr>
<tr class="odd">
<td>length</td>
<td><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>LengthType</strong></a></td>
<td>Die Länge eines Datenelements variabler Länge, z. B. eines binären Blobs. Geben Sie für Binärdaten die Länge in Bytes und für Zeichenfolgendaten die Länge in Zeichen an. Sie können die tatsächliche Länge oder den Namen eines anderen Datenelements angeben, das die Länge enthält.<br/> Wenn Sie das Length-Attribut verwenden, um eine Zeichenfolge mit fester Länge anzugeben, müssen Sie die Zeichenfolge bis zu ihrer festen Länge aufhängen, sodass das Nullabschlusszeichen am Ende möglich ist (wenn die Länge beispielsweise 5 beträgt, muss die Zeichenfolge abc als abc aufpaddiert &quot; &quot; &quot; &quot; werden. Die Zeichenfolgenlänge muss das Nullabschlusszeichen enthalten.<br/></td>
</tr>
<tr class="even">
<td>Karte</td>
<td>Zeichenfolge</td>
<td>Der Name der Name-Wert-Zuordnung, die zum Zuordnen von ganzzahligen Werten zu Zeichenfolgen verwendet werden soll. Der Datentyp des Datenelements muss einen der folgenden Typen haben:<br/>
<ul>
<li>win:UInt8</li>
<li>win:UInt16</li>
<li>win:UInt32</li>
</ul></td>
</tr>
<tr class="odd">
<td>name</td>
<td>Zeichenfolge</td>
<td>Der Name des Datenelements. Sie können den Namen verwenden, um auf dieses Datenelement in Ihrem XML-Fragment zu verweisen, wenn Sie einen <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData-Abschnitt</strong></a> in Ihrer Vorlage angeben. Sie können auch in einem length- oder count-Attribut eines anderen Datenelements auf diesen Namen verweisen, wenn dieses Datenelement seinen Längen- oder Anzahlwert enthält.<br/> <strong>Windows Vista:</strong> Dieses Attribut ist optional.<br/></td>
</tr>
<tr class="even">
<td>outType</td>
<td><strong>QName</strong></td>
<td>Der Datentyp, der beim Rendern dieses Datenelements verwendet werden soll. Eine Liste der vordefinierten Ausgabedatentypen finden Sie unter Komplexer <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType-Typ.</strong></a><br/> <strong>Windows Vista:</strong> Der Ausgabetyp wird ignoriert, und der Dienst bestimmt den Typ basierend auf dem Eingabetyp.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Für Eingabetypen variabler Länge, z. B. binäre Blobs, müssen Sie das Length-Attribut verwenden, um die Größe der Daten explizit anzugeben. Geben Sie für Zeichenfolgen das Length-Attribut nur an, wenn die Zeichenfolgen eine feste Länge haben.

## <a name="examples"></a>Beispiele

Im Folgenden finden Sie einige Beispiele für die Datenelementdefinitionen.


```XML
<!-- The data item is an 8-bit integer -->
<data name="binaryChar" inType="win:UInt8">
 
<!-- The data item is a single ANSI character -->
<data name="ansiChar" inType="win:UInt8" outtype="xs:string">
 
<!-- The data item is a single Unicode character -->
<data name="unicodeChar" inType="win:UInt16" outtype="xs:string">
 
<!-- The data item is an IP address that is rendered as a dot separated list of interger values -->
<data name="ipAddress" inType="win:UInt32" outtype="win:IPv4">
 
<!-- The data item is a Boolean value -->
<data name="success" inType="win:boolean">
 
<!-- The data item is a null-terminated ANSI string -->
<data name="string" inType="win:AnsiString"> 

<!-- The data item is a fixed length ANSI string -->
<data name="string" inType="win:AnsiString" length="42"> 
 
<!-- The data item is a fixed length array of null-terminated ANSI strings -->
<data name="strings" inType="win:AnsiString" count="20">
 
<!-- The data item is a fixed length array of fixed length ANSI strings -->
<data name="strings" inType="win:AnsiString" length="42" count="20">
 
<!-- The data item is a variable length array of same sized ANSI strings -->
<data name="stringLength" inType="win:UInt16">
<data name="arrayCount" inType="win:Uint16">
<data name="strings" inType="win:AnsiString" length="stringLength" count="arrayCount"> 
 
<!-- For binary data, you must specify the size.
<!-- The data item is a fixed length array of fixed length binary blobs -->
<data name="blobs" inType="win:Binary" length="42" count="20">

<!-- The data item is a fixed length binary blob -->
<data name="blob" inType="win:Binary" length="42">

<!-- The following are illegal binary data definitions -->
<!-- This definition is illegal because no length is specified -->
<data name="blob" inType="win:Binary"> 
 
<!-- This definition is illegal because you cannot determine the length of each binary blob -->
<data name="blob" inType="win:Binary" count="20"> 
 
<!-- The data item is a variable length array of structures. Each structure -->
<!-- contains an array of same sized ANSI strings --> 
<data name="arrayStructCount" inType="win:UInt16">
<struct name="countedStrings" count="arrayStructCount">
      <data name="stringLength" inType="win:UInt16">
      <data name="string" inType="win:AnsiString" length="stringLength">
</struct>
 
<!-- The data item is a time stamp that is rendered in 100ns units -->
<data name="timestamp" inType="win:UInt32" outType="win:ETWTIME">

<!-- The data item is a fixed length array of integers --> 
<data name="integers" inType="win:UInt32" count="20">

<!-- The data item is a variable length array of integers -->
<data name="arrayCount" inType="win:UInt16"> 
<data name="integers" inType="win:UInt32" count="arrayCount"> 

<!-- The following is illegal because you cannot assign a length value to a data type of a known size -->
<data name="integer" inType="win:UInt32" length="42">
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





