---
title: HelpButton-Element
description: Stellt das Hilfe Button-Steuerelement dar.
ms.assetid: 24c709da-539e-4ea0-bd3e-d3fbd72dfb97
keywords:
- HelpButton-Element Windows-Menüband
topic_type:
- apiref
api_name:
- HelpButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5be084ff6fc92d4eac4bbaffb3c507142f91eba8
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "106341911"
---
# <a name="helpbutton-element"></a>HelpButton-Element

Stellt das [Hilfe Button](windowsribbon-controls-helpbutton.md) -Steuerelement dar.

## <a name="usage"></a>Verbrauch

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
<th>Attribut</th>
<th>type</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CommandName</strong><br/></td>
<td>xs: positiveingeteger oder xs: String<br/></td>
<td>Nein<br/></td>
<td>Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich). <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                         |
|---------------------------------------------------------------------------------|
| [**Menüband. HelpButton**](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jede [**Multifunktionsleiste. HelpButton**](windowsribbon-element-ribbon-helpbutton.md)auftreten.

Öffnet das Dialogfeld Anwendungs Hilfe, wenn darauf geklickt wird.

## <a name="examples"></a>Beispiele

Das folgende Beispiel veranschaulicht das grundlegende Markup, das zum Implementieren eines [Schalt](windowsribbon-controls-helpbutton.md) Flächen-Steuer Elements für die Multifunktionsleiste erforderlich ist.

Dieser Code Abschnitt zeigt die **HelpButton** -Befehls Deklaration.


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



In diesem Code Abschnitt wird die **HelpButton** -Steuerelement Deklaration gezeigt.


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a>Elementinformationen



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Ja       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Hilfe Button-Steuerelement](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 





