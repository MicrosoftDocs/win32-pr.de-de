---
title: HelpButton-Element
description: Stellt das Steuerelement Hilfeschaltfläche dar.
ms.assetid: 24c709da-539e-4ea0-bd3e-d3fbd72dfb97
keywords:
- HelpButton-Element Im Windows-Menüband
topic_type:
- apiref
api_name:
- HelpButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f34f04133b7628cce01ac0ce2808923b4f6bbdb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442841"
---
# <a name="helpbutton-element"></a>HelpButton-Element

Stellt das Steuerelement [Hilfeschaltfläche](windowsribbon-controls-helpbutton.md) dar.

## <a name="usage"></a>Verwendung

``` syntax
<HelpButton
  CommandName = "xs:positiveInteger or xs:string"/>
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
<th>attribute</th>
<th>Typ</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger oder xs:string<br/></td>
<td>Nein<br/></td>
<td>Ordnet das Element einem Befehl <a href="windowsribbon-element-command.md"><strong>zu.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich. <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                         |
|---------------------------------------------------------------------------------|
| [**Ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a>Hinweise

Dies ist optional.

Kann für jedes [**Ribbon.HelpButton--Menüband nur einmal auftreten.**](windowsribbon-element-ribbon-helpbutton.md)

Öffnet ein Anwendungshilfedialogfeld, wenn darauf geklickt wird.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup veranschaulicht, das zum Implementieren eines [Menüband-Hilfeschaltfläche-Steuerelements erforderlich](windowsribbon-controls-helpbutton.md) ist.

Dieser Codeabschnitt zeigt die **HelpButton-Befehlsdeklaration.**


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



Dieser Codeabschnitt zeigt die **HelpButton-Steuerelementdeklaration.**


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a>Elementinformationen

* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Ja



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schaltflächen-Steuerelement "Hilfe"](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 





