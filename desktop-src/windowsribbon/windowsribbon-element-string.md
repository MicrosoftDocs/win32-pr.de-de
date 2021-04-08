---
title: String-Element
description: Stellt eine Zeichen folgen Ressource dar.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- String-Element Windows-Menüband
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 577d318292081dddf4e2839967642c6115a474d6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038048"
---
# <a name="string-element"></a>String-Element

Stellt eine Zeichen folgen Ressource dar.

## <a name="usage"></a>Verbrauch

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>type</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Inhalt</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>xs: positiveingeteger oder xs: String<br/></td>
<td>Nein<br/></td>
<td>Die eindeutige Ressourcen-ID. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)<br/> </dt> <dd> Ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder 0x2 und 0xea5f in Hexadezimal (einschließlich). <br/> Die maximale Länge beträgt 10 Zeichen, einschließlich optionaler führender Nullen. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Symbol</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Das Ressourcen Symbol für die Zeichenfolge.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Ein Buchstabe oder Unterstrich, gefolgt von einer beliebigen Reihenfolge von Buchstaben, Ziffern oder unterstrichen.<br/> Die maximale Länge beträgt 100 Zeichen.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                   | BESCHREIBUNG                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [**String. Content**](windowsribbon-element-string-content.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/> |
| [**String.Id**](windowsribbon-element-string-id.md)<br/>           | Kann höchstens einmal vorkommen<br/> <br/> |
| [**String. Symbol**](windowsribbon-element-string-symbol.md)<br/>   | Kann höchstens einmal vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [**Command. KeyTip**](windowsribbon-element-command-keytip.md)<br/>                         |
| [**Command. labeldescription**](windowsribbon-element-command-labeldescription.md)<br/>     |
| [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [**Command. tooltipdescription**](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [**Command. ToolTipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jedes [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md)-, [**Command. labeldescription**](windowsribbon-element-command-labeldescription.md)-, [**Command. KeyTip**](windowsribbon-element-command-keytip.md)-, [**Command. ToolTipTitle**](windowsribbon-element-command-tooltiptitle.md)-oder [**Command. tooltipdescription**](windowsribbon-element-command-tooltipdescription.md) -Element auftreten.

Die Zeichen folgen Definition wird der Menüband-Header Datei hinzugefügt, z `#define strSave 59999` . b..

Die Zeichenfolge wird einer Zeichen folgen Tabelle in der Ressourcen Datei des Menübands hinzugefügt, in der ein Name und eine ID vom Menüband-Framework generiert werden, wenn keine deklariert sind.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) -Element mit einer **Zeichen** folgen Deklaration veranschaulicht.


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a>Elementinformationen



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Nein        |



 

 





