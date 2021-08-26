---
title: Command-Element
description: Stellt eine Befehlsdefinition dar.
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- Command-Element Windows Menüband
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2def999c89994965f705f53edee684a3f1882fa2b47d43e512942715a8fc51f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931550"
---
# <a name="command-element"></a>Command-Element

Stellt eine Befehlsdefinition dar.

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
<th>attribute</th>
<th>type</th>
<th>Erforderlich</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Comment</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Wird zum Kommentieren des Befehlselements verwendet.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.<br/> Maximale Länge: 250 Zeichen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>xs:positiveInteger union xs:string<br/></td>
<td>Nein<br/></td>
<td>Die eindeutige Ressourcen-ID. <br/> <br/>
<dt><span></span><span></span><strong></strong> (Die Vereinigung von xs:positiveInteger und xs:string)<br/> </dt> <dd> Ein ganzzahliger Wert zwischen 2 und 59999, einschließlich oder 0x2 und 0xea5f in Hexadezimal, einschließlich. <br/> Die maximale Länge beträgt 10 Zeichen, einschließlich optionaler führender Nullen. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Keytip</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Eine Zeichenfolge, die die Tastenkombination eines Befehlselements darstellt.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>LabelDescription</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Eine Zeichenfolge, die den auf einem Befehlselement angezeigten Text darstellt.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>LabelTitle</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Eine Zeichenfolge, die den auf einem Befehlselement angezeigten Text darstellt.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Name</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die aus einem Buchstaben oder Unterstrich gefolgt von einer beliebigen Sequenz von Ziffern, Buchstaben oder Unterstrichen besteht.<br/> Maximale Länge: 100 Zeichen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Symbol</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die aus einem Buchstaben oder Unterstrich gefolgt von einer beliebigen Sequenz von Ziffern, Buchstaben oder Unterstrichen besteht.<br/> Maximale Länge: 100 Zeichen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>QuickInfoDescription</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Eine Zeichenfolge, die den auf einem Befehlselement angezeigten Text darstellt.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>QuickInfoTitle</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Eine Zeichenfolge, die den auf einem Befehlselement angezeigten Text darstellt.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                     | Beschreibung                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Command.Comment**](windowsribbon-element-command-comment.md)<br/>                                 | Kann höchstens einmal auftreten.<br/> <br/> |
| [**Command.Id**](windowsribbon-element-command-id.md)<br/>                                           | Kann höchstens einmal auftreten.<br/> <br/> |
| [**Command.Keytip**](windowsribbon-element-command-keytip.md)<br/>                                   | Kann höchstens einmal auftreten.<br/> <br/> |
| [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md)<br/>               | Kann höchstens einmal auftreten.<br/> <br/> |
| [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md)<br/>                           | Kann höchstens einmal auftreten.<br/> <br/> |
| [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> | Kann höchstens einmal auftreten.<br/> <br/> |
| [**Command.LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         | Kann höchstens einmal auftreten.<br/> <br/> |
| [**Command.Name**](windowsribbon-element-command-name.md)<br/>                                       | Kann höchstens einmal auftreten.<br/> <br/> |
| [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | Kann höchstens einmal auftreten.<br/> <br/> |
| [**Command.SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         | Kann höchstens einmal auftreten.<br/> <br/> |
| [**Command.Symbol**](windowsribbon-element-command-symbol.md)<br/>                                   | Kann höchstens einmal auftreten.<br/> <br/> |
| [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)<br/>           | Kann höchstens einmal auftreten.<br/> <br/> |
| [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>                       | Kann höchstens einmal auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                               |
|---------------------------------------------------------------------------------------|
| [**Application.Commands**](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a>Hinweise

Erforderlich.

Kann ein oder mehrere Male für jedes [**Application.Commands-Element**](windowsribbon-element-application-commands.md) auftreten.

Die untergeordneten Elemente des **Command-Elements** können in beliebiger Reihenfolge auftreten.

In der Regel werden Befehlsressourcen im Menübandmarkup deklariert, können aber auch zur Laufzeit mit einem Aufruf von [**SetUICommandProperty festgelegt werden.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) Beispielsweise kann die [ \_ PKEY \_ Keytip-Eigenschaft](windowsribbon-reference-properties-uipkey-keytip.md) der Benutzeroberfläche für einen Befehl festgelegt werden, anstatt einen Wert im Markup mit dem [**Command.Keytip-Element zu deklarieren.**](windowsribbon-element-command-keytip.md)

In Fällen, in denen Befehlseigenschaften wie Bezeichnungen und Bilder nicht mit [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden können, können sie mit einem Aufruf von [**InvalidateUICommand für**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)ungültig erklärt werden. Nach der Ungültigkeit fragt das Framework die Hostanwendung nach den Ressourcendetails ab.

> [!Note]  
> Eine Ressource kann nicht erneut aus der Markupressourcentabelle restatiert werden, nachdem sie für ungültig erklärt wurde.

 

Eine Befehlsdefinition wird der Menüband-Markupheaderdatei für jeden Befehl hinzugefügt, **der** im Markup deklariert ist.

Der Wert von *Keytip* fungiert als Zugriffstaste für einen Befehl, es sei denn, dieser Befehl wird über ein Menüelement verfügbar gemacht. In diesem Fall ignoriert das Framework den *Keytip-Wert* und verwendet stattdessen ein Zeichen, dem ein ampersand vorangegangen ist, wie durch *LabelTitle* oder [UI \_ PKEY \_ Label angegeben.](windowsribbon-reference-properties-uipkey-label.md) Wenn kein ampersand durch *LabelTitle* oder UI PKEY Label angegeben wird, wird keine Tastenkombination oder \_ \_ Tastenkombination verfügbar gemacht.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt ein Manifest von **Command-Elementen** für eine **Registerkarte Start.**


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

* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Nein



 

