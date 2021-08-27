---
title: String-Element
description: Stellt eine Zeichenfolgenressource dar.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- Zeichenfolgenelement Windows Menüband
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a34a417b6ad4d57bea83fcae13d810b22114271
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630956"
---
# <a name="string-element"></a>String-Element

Stellt eine Zeichenfolgenressource dar.

## <a name="usage"></a>Verwendung

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
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Typ</th>
<th>Erforderlich</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Inhalt</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>xs:positiveInteger oder xs:string<br/></td>
<td>Nein<br/></td>
<td>Die eindeutige Ressourcen-ID. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)<br/> </dt> <dd> Ein ganzzahliger Wert zwischen 2 und 59999, einschließlich oder 0x2 und 0xea5f in Hexadezimal, einschließlich. <br/> Die maximale Länge beträgt 10 Zeichen, einschließlich optionaler führender Nullen. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Symbol</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Das Ressourcensymbol für die Zeichenfolge.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Ein Buchstabe oder Unterstrich, gefolgt von einer beliebigen Sequenz von Buchstaben, Ziffern oder Unterstrichen.<br/> Die maximale Länge beträgt 100 Zeichen.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                   | Beschreibung                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [**String.Content**](windowsribbon-element-string-content.md)<br/> | Kann höchstens einmal auftreten.<br/> <br/> |
| [**String.Id**](windowsribbon-element-string-id.md)<br/>           | Kann höchstens einmal auftreten.<br/> <br/> |
| [**String.Symbol**](windowsribbon-element-string-symbol.md)<br/>   | Kann höchstens einmal auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [**Command.Keytip**](windowsribbon-element-command-keytip.md)<br/>                         |
| [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md)<br/>     |
| [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a>Hinweise

Optional.

Kann höchstens einmal für jedes [**Command.LabelTitle-,**](windowsribbon-element-command-labeltitle.md) [**Command.LabelDescription-,**](windowsribbon-element-command-labeldescription.md) [**Command.Keytip-,**](windowsribbon-element-command-keytip.md) [**Command.TooltipTitle-**](windowsribbon-element-command-tooltiptitle.md)oder [**Command.TooltipDescription-Element**](windowsribbon-element-command-tooltipdescription.md) auftreten.

Die Zeichenfolgendefinition wird der Menübandheaderdatei hinzugefügt, z. `#define strSave 59999` B. .

Die Zeichenfolge wird einer Zeichenfolgentabelle in der Menübandressourcendatei hinzugefügt, in der ein Name und eine ID vom Menübandframework generiert werden, wenn keine deklariert sind.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command.LabelTitle-Element**](windowsribbon-element-command-labeltitle.md) mit einer **String-Deklaration** veranschaulicht.


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

- **Unterstütztes Mindestsystem:** Windows 7 
- **Kann leer sein:** Nein



 

 





