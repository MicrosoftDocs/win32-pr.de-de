---
title: Command. smallimages (Eigenschaft)
description: Stellt einen Container von Bildern dar. in diesem Fall kleine Bilder.
ms.assetid: 15c00e61-543a-4cc8-b329-516985d02359
keywords:
- Command. smallimages-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Command.SmallImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b18556cf519c21b01c3e80b63cbfc9cdf9d7d153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478624"
---
# <a name="commandsmallimages-property"></a>Command. smallimages (Eigenschaft)

Stellt einen Container von Bildern dar. in diesem Fall kleine Bilder.

## <a name="usage"></a>Verbrauch

``` syntax
<Command.SmallImages>
  child elements
</Command.SmallImages>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                 | BESCHREIBUNG                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [**Image**](windowsribbon-element-image.md)<br/> | Kann ein-oder mehrmals vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                     |
|-------------------------------------------------------------|
| [**Get-Help**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jeden [**Befehl**](windowsribbon-element-command.md)auftreten.

Bild Ressourcen müssen dem standardmäßigen BMP-Grafikformat (Bitmap) entsprechen, das in Windows verwendet wird.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für das [**SplitButton**](windowsribbon-element-splitbutton.md) -Element mit einem [**MenuGroup**](windowsribbon-element-menugroup.md) -Element veranschaulicht.

In diesem Code Abschnitt werden die Befehls Deklarationen [**SplitButton**](windowsribbon-element-splitbutton.md) und [**MenuGroup**](windowsribbon-element-menugroup.md) mit einer großen und kleinen Bildressource angezeigt. Eine zugeordnete [**Gruppe**](windowsribbon-element-group.md) , die als übergeordneter Container für das **SplitButton** -Element fungiert, wird ebenfalls deklariert.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Angeben von Menüband-Bild Ressourcen](windowsribbon-imageformats.md)
</dt> <dt>

[UI \_ pkey \_ smallImage](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> </dl>

 

 





