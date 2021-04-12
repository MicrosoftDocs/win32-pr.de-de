---
title: Command-Element
description: Stellt eine Befehls Definition dar.
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- Windows-Menüband des Befehls Elements
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b684b361927180a4bb87d2d7814d2f26d4fdcd91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316137"
---
# <a name="command-element"></a>Command-Element

Stellt eine Befehls Definition dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Command
  Name = "xs:string"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string"
  Comment = "xs:string"
  LabelTitle = "xs:string"
  LabelDescription = "xs:string"
  TooltipTitle = "xs:string"
  TooltipDescription = "xs:string"
  Keytip = "xs:string">
  child elements
</Command>
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
<td><strong>Kommentar</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Wird verwendet, um das Command-Element mit Anmerkungen zu versehen.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.<br/> Maximale Länge: 250 Zeichen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>xs: positivan teger Union xs: String<br/></td>
<td>Nein<br/></td>
<td>Die eindeutige Ressourcen-ID. <br/> <br/>
<dt><span></span><span></span><strong></strong> (Die Vereinigung von xs: positiveingeteger und xs: String)<br/> </dt> <dd> Ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder 0x2 und 0xea5f in Hexadezimal (einschließlich). <br/> Die maximale Länge beträgt 10 Zeichen, einschließlich optionaler führender Nullen. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>KeyTip</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Eine Zeichenfolge, die die Tastenkombination eines Command-Elements darstellt.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Labeldescription</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Eine Zeichenfolge, die den Text darstellt, der in einem Command-Element angezeigt wird.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Labeltitle</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Eine Zeichenfolge, die den Text darstellt, der in einem Command-Element angezeigt wird.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Name</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine Zeichenfolge, die aus einem Buchstaben oder einem Unterstrich gefolgt von einer beliebigen Folge von Ziffern, Buchstaben oder unterstrichen besteht.<br/> Maximale Länge: 100 Zeichen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Symbol</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine Zeichenfolge, die aus einem Buchstaben oder einem Unterstrich gefolgt von einer beliebigen Folge von Ziffern, Buchstaben oder unterstrichen besteht.<br/> Maximale Länge: 100 Zeichen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Tooltipdescription</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Eine Zeichenfolge, die den Text darstellt, der in einem Command-Element angezeigt wird.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ToolTipTitle</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Eine Zeichenfolge, die den Text darstellt, der in einem Command-Element angezeigt wird.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                     | BESCHREIBUNG                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Command. Comment**](windowsribbon-element-command-comment.md)<br/>                                 | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Command.Id**](windowsribbon-element-command-id.md)<br/>                                           | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Command. KeyTip**](windowsribbon-element-command-keytip.md)<br/>                                   | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Command. labeldescription**](windowsribbon-element-command-labeldescription.md)<br/>               | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md)<br/>                           | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Command. largehighkontra stimages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Command. largeimages**](windowsribbon-element-command-largeimages.md)<br/>                         | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Command.Name**](windowsribbon-element-command-name.md)<br/>                                       | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Command. smallhighkontra stimages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Command. smallimages**](windowsribbon-element-command-smallimages.md)<br/>                         | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Command. Symbol**](windowsribbon-element-command-symbol.md)<br/>                                   | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Command. tooltipdescription**](windowsribbon-element-command-tooltipdescription.md)<br/>           | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Command. ToolTipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>                       | Kann höchstens einmal vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                               |
|---------------------------------------------------------------------------------------|
| [**Application. Commands**](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Erforderlich.

Kann für jedes [**Application. Commands**](windowsribbon-element-application-commands.md) -Element einmal oder mehrmals vorkommen.

Die untergeordneten Elemente des **Command** -Elements können in beliebiger Reihenfolge auftreten.

In der Regel werden Befehls Ressourcen in Menüband-Markup deklariert, Sie können jedoch auch zur Laufzeit mit einem Aufruf von [**setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)festgelegt werden. Beispielsweise ist es möglich, die Benutzeroberflächen [- \_ pkey- \_ KeyTip](windowsribbon-reference-properties-uipkey-keytip.md) -Eigenschaft für einen Befehl festzulegen, anstatt einen Wert im Markup mit dem [**Command. KeyTip**](windowsribbon-element-command-keytip.md) -Element zu deklarieren.

In Fällen, in denen Befehls Eigenschaften, z. b. Bezeichnungen und Bilder, nicht mit [**setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden können, können Sie mit einem- [**Befehl von invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)ungültig gemacht werden. Nach der Invalidierung fragt das Framework die Host Anwendung nach den Ressourcen Details ab.

> [!Note]  
> Eine Ressource kann nicht aus der Markup Ressourcen Tabelle wieder hergestellt werden, nachdem Sie ungültig gemacht wurde.

 

Der Menüband-Markup Header Datei wird für jeden **Befehl** , der im Markup deklariert ist, eine Befehls Definition hinzugefügt.

Der Wert von *KeyTip* fungiert als Tastaturbeschleuniger für einen Befehl, es sei denn, dieser Befehl wird über ein Menü Element verfügbar gemacht. In diesem Fall ignoriert das Framework den *KeyTip* -Wert und verwendet stattdessen ein Zeichen, dem ein kaufmännisches und-Zeichen gemäß der Bezeichnung " *labeltitle* " oder " [UI \_ pkey \_](windowsribbon-reference-properties-uipkey-label.md)" vorangestellt ist. Wenn kein kaufmännisches und-Zeichen von der Bezeichnung " *labeltitle* " oder "UI pkey" angegeben wird \_ \_ , wird kein KeyTip oder keine Tastatur Beschleunigung bereitgestellt.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt ein Manifest der **Befehls** Elemente für eine Registerkarte **Home** .


```XML
<Application.Commands>
```




```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```




```XML
</Application.Commands>
```



## <a name="element-information"></a>Elementinformationen



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Nein        |



 

