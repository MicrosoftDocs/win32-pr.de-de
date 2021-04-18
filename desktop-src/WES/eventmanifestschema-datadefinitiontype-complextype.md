---
title: Komplexer DataDefinitionType-Typ
description: Definiert ein Datenelement, das Sie mit dem-Ereignis einschließen möchten. | Komplexer DataDefinitionType-Typ
ms.assetid: f4234e54-a5a8-48e4-941f-05107dcd3f88
keywords:
- DataDefinitionType komplexer Typ (Ereignisprotokoll)
topic_type:
- apiref
api_name:
- DataDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19584c28a7bdf7ae01b87d1f414b9464b7b4271d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354303"
---
# <a name="datadefinitiontype-complex-type"></a>Komplexer DataDefinitionType-Typ

Definiert ein Datenelement, das Sie mit dem-Ereignis einschließen möchten.

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
<th>type</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>count</td>
<td><a href="eventmanifestschema-counttype-simpletype.md"><strong>"Count Type"</strong></a></td>
<td>Die Anzahl der Elemente im Array, wenn das Datenelement ein Array ist. Sie können die tatsächliche Anzahl oder den Namen eines anderen Datenelements angeben, das die Anzahl enthält. <br/></td>
</tr>
<tr class="even">
<td>intype</td>
<td><strong>QName</strong></td>
<td>Der Datentyp für dieses Datenelement. Eine Liste der vordefinierten Eingabe Datentypen finden Sie unter der komplexe Typ " <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> ".<br/></td>
</tr>
<tr class="odd">
<td>length</td>
<td><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>Längen-Typ</strong></a></td>
<td>Die Länge eines Datenelements variabler Länge, z. b. ein binäres Blob. Geben Sie für binäre Daten die Länge in Bytes an, und geben Sie für Zeichen folgen Daten die Länge in Zeichen an. Sie können die tatsächliche Länge oder den Namen eines anderen Datenelements angeben, das die Länge enthält.<br/> Wenn Sie das length-Attribut verwenden, um eine Zeichenfolge mit fester Länge anzugeben, müssen Sie die Zeichenfolge in die festgelegte Länge auffüllen, damit das NULL-Terminator-Zeichen am Ende zugelassen wird (wenn die Länge beispielsweise 5 beträgt, muss die Zeichenfolge &quot; ABC &quot; als ABC aufgefüllt werden &quot; &quot; . Die Zeichen folgen Länge muss das NULL-Terminator-Zeichen enthalten.<br/></td>
</tr>
<tr class="even">
<td>Karte</td>
<td>Zeichenfolge</td>
<td>Der Name der Name-Wert-Zuordnung, die zum Zuordnen von ganzzahligen Werten zu Zeichen folgen verwendet werden soll. Der Datentyp des Datenelements muss einen der folgenden Typen aufweisen:<br/>
<ul>
<li>win:UInt8</li>
<li>win:UInt16</li>
<li>win:UInt32</li>
</ul></td>
</tr>
<tr class="odd">
<td>name</td>
<td>Zeichenfolge</td>
<td>Der Name des Datenelements. Sie können den Namen verwenden, um auf dieses Datenelement in Ihrem XML-Fragment zu verweisen, wenn Sie einen <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> -Abschnitt in ihrer Vorlage angeben. Sie können auch in einem length-oder count-Attribut eines anderen Datenelements auf diesen Namen verweisen, wenn dieses Datenelement seinen Längen-oder Anzahl Wert enthält.<br/> <strong>Windows Vista:</strong> Dieses Attribut ist optional.<br/></td>
</tr>
<tr class="even">
<td>outtype</td>
<td><strong>QName</strong></td>
<td>Der Datentyp, der beim Rendern dieses Datenelements verwendet werden soll. Eine Liste der vordefinierten Ausgabe Datentypen finden Sie unter der komplexe Typ " <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> ".<br/> <strong>Windows Vista:</strong> Der Ausgabetyp wird ignoriert, und der Dienst bestimmt den Typ basierend auf dem Eingabetyp.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Für Eingabetypen mit variabler Länge (z. b. binäre BLOB) müssen Sie das length-Attribut verwenden, um die Größe der Daten explizit anzugeben. Geben Sie für Zeichen folgen nur dann das length-Attribut an, wenn die Zeichen folgen eine festgelegte Länge haben.

## <a name="examples"></a>Beispiele

Im folgenden sind einige Beispiele für die Datenelement Definitionen aufgeführt.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





