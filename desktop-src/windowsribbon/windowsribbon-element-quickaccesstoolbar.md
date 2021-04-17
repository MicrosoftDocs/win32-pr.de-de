---
title: Quickaccesstoolbar-Element
description: Stellt die Symbolleiste für den schnell Zugriff (QAT) dar, eine kleine Symbolleiste, die Verknüpfungen zu Menü Band Befehlen anzeigt.
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- Windows-Menüband für quickaccesstoolbar-Element
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0076890a8d9858d4bf410ecfdd866bf4f48fdbb6
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389804"
---
# <a name="quickaccesstoolbar-element"></a>Quickaccesstoolbar-Element

Stellt die [Symbolleiste für den schnell Zugriff (QAT)](windowsribbon-controls-quickaccesstoolbar.md)dar, eine kleine Symbolleiste, die Verknüpfungen zu Menü Band Befehlen anzeigt.

## <a name="usage"></a>Verbrauch

``` syntax
<QuickAccessToolbar
  CommandName = "xs:positiveInteger or xs:string"
  CustomizeCommandName = "xs:positiveInteger or xs:string">
  child elements
</QuickAccessToolbar>
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
<tr class="even">
<td><strong>Customizecommandname</strong><br/></td>
<td>xs: positiveingeteger oder xs: String<br/></td>
<td>Nein<br/></td>
<td>Fügt ein zusätzliches Befehls Element in das QAT-Menü ein.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)<br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich). <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                                   | BESCHREIBUNG                                   |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Quickaccesstoolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [**Menüband. quickaccesstoolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Erforderlich.

Muss für jede [**Multifunktionsleiste. quickaccesstoolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)genau einmal auftreten.

Elemente im QAT können zur Laufzeit hinzugefügt oder entfernt werden.

Aus Gründen der Konsistenz zwischen Menüband-Anwendungen wird empfohlen, dass der *customizecommandname* -Befehls Handler ein QAT-Anpassungs Dialogfeld startet.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für die **quickaccesstoolbar** veranschaulicht.

In diesem Code Abschnitt wird die **quickaccesstoolbar** -Befehls Deklaration veranschaulicht.


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



In diesem Code Abschnitt wird die Deklaration des **quickaccesstoolbar** -Steuer Elements veranschaulicht.


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a>Elementinformationen



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Nein        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Symbolleisten-Steuerelement schnell Zugriff](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





