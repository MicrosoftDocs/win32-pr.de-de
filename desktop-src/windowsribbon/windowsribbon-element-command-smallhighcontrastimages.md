---
title: Command.SmallHighContrastImages (Eigenschaft)
description: Stellt einen Container von Images dar. in diesem Fall kleine Bilder für die Verwendung mit Systemeinstellungen mit hohem Kontrast.
ms.assetid: d1c441eb-885a-4dc1-b98d-5a36cab2f837
keywords:
- Command.SmallHighContrastImages-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- Command.SmallHighContrastImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ddee0ccadc966b89d381e02cca5ac1ae336c98671c82a3e4f39f8ebdd6cbeb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329290"
---
# <a name="commandsmallhighcontrastimages-property"></a>Command.SmallHighContrastImages (Eigenschaft)

Stellt einen Container von Images dar. in diesem Fall kleine Bilder für die Verwendung mit Systemeinstellungen mit hohem Kontrast.

## <a name="usage"></a>Verbrauch

``` syntax
<Command.SmallHighContrastImages>
  child elements
</Command.SmallHighContrastImages>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                 | BESCHREIBUNG                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [**Image**](windowsribbon-element-image.md)<br/> | Kann ein oder mehrere Male auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                     |
|-------------------------------------------------------------|
| [**Befehl**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann für jeden Befehl mindestens einmal [**auftreten.**](windowsribbon-element-command.md)

Bildressourcen müssen dem standarden Bitmap-Grafikformat (BMP) entsprechen, das in der Windows.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für [**splitButton mit**](windowsribbon-element-splitbutton.md) einem [**MenuGroup-Element**](windowsribbon-element-menugroup.md) veranschaulicht.

Dieser Codeabschnitt zeigt die [**SplitButton-**](windowsribbon-element-splitbutton.md) und [**MenuGroup-Befehlsdeklarationen**](windowsribbon-element-menugroup.md) mit großen und kleinen Bildressourcen mit hohem Kontrast. Eine [**zugeordnete Gruppe,**](windowsribbon-element-group.md) die als übergeordneter Container für das **SplitButton-Element** fungiert, wird ebenfalls deklariert.


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Angeben von Menübandbildressourcen](windowsribbon-imageformats.md)
</dt> <dt>

[UI \_ PKEY \_ SmallHighContrastImage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> </dl>

 

 





