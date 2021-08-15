---
title: Command.LabelDescription-Eigenschaft
description: Stellt eine Bezeichnungsbeschreibung dar.
ms.assetid: 6c683e9e-0742-466e-9fdd-3d29f8ccb9ff
keywords:
- Command.LabelDescription-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- Command.LabelDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9051b4f645744416f290906559e054405726f36f9616e8f38f3cfbae357137dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964209"
---
# <a name="commandlabeldescription-property"></a>Command.LabelDescription-Eigenschaft

Stellt eine Bezeichnungsbeschreibung dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Command.LabelDescription>
  child elements
</Command.LabelDescription>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                   | BESCHREIBUNG                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**String**](windowsribbon-element-string.md)<br/> | Kann höchstens einmal auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                     |
|-------------------------------------------------------------|
| [**Befehl**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann höchstens einmal für jeden [**Befehl**](windowsribbon-element-command.md)auftreten.

**Command.LabelDescription** kann einen Wert vom *Typ xs:string* enthalten, der auf eine beliebige Zeichensequenz beschränkt ist, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.

> [!Note]  
> Verwenden Sie den UCS-XML-Zeichenverweis (Universal Character Set), `&#xA;` um einen Zeilenbreak anzugeben.

 

Die maximale Länge ist ungebunden.

Wenn kein Wert für **Command.LabelDescription** angegeben wird, ist das untergeordnete [**String-Element**](windowsribbon-element-string.md) erforderlich.

> [!Note]  
> Wenn **Command.LabelDescription** sowohl einen Wert als auch ein untergeordnetes [**String-Element**](windowsribbon-element-string.md) enthält, hat **String** Vorrang.

 

**Command.LabelDescription** unterstützt nur die linke Ausrichtung.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt ein Manifest von Zwischenablagebefehlen mit verschiedenen **Command.LabelDescription-Deklarationen.**


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[UI \_ PKEY \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 





