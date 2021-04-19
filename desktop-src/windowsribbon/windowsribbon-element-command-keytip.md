---
title: Command. KeyTip (Eigenschaft)
description: Stellt den KeyTip für ein-Steuerelement dar.
ms.assetid: 214f69ae-dd35-4abf-b294-d898d7802aa6
keywords:
- Command. KeyTip-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Command.Keytip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab16b9b8e52094d6cdc85890dfc1cf8af63942c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343049"
---
# <a name="commandkeytip-property"></a>Command. KeyTip (Eigenschaft)

Stellt den KeyTip für ein-Steuerelement dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Command.Keytip>
  child elements
</Command.Keytip>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                   | BESCHREIBUNG                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**Schnür**](windowsribbon-element-string.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                     |
|-------------------------------------------------------------|
| [**Get-Help**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jedes [**Befehls**](windowsribbon-element-command.md) Element auftreten.

**Command. KeyTip** kann einen Wert vom Typ *xs: String* enthalten, der auf eine beliebige Unicode-Zeichenfolge (einschließlich Leerzeichen) beschränkt ist.

Eine " **Command. KeyTip** " kann nur mit einer Zahl beginnen, wenn Sie einem Steuerelement in einer [Registerkarte](windowsribbon-controls-tab.md) oder der [Symbolleiste für den schnell Zugriff](windowsribbon-controls-quickaccesstoolbar.md)zugeordnet ist.

Drücken Sie die Alt-Taste, um die KeyTips anzuzeigen, die für den aktuellen Status des Menübands gültig sind. Der folgende Screenshot zeigt die Ausgangs-oder erste Ebene der KeyTips, die in Microsoft Paint für Windows 7 angezeigt werden. Nachdem Sie einen KeyTip der ersten Ebene ausgewählt haben, werden nur KeyTips der zweiten Ebene angezeigt.

![KeyTips der ersten Ebene in Microsoft Paint für Windows 7](images/properties/ui-pkey-label-keytips.png)

**Command. KeyTip** fungiert als Tastaturbeschleuniger für einen Befehl, es sei denn, dieser Befehl wird über ein Menü Element verfügbar gemacht. In diesem Fall ignoriert das Framework den **Command. KeyTip** -Wert und verwendet stattdessen ein Zeichen, dem ein kaufmännisches und-Zeichen vorangestellt ist, wie durch [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) oder [UI \_ pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)angegeben. Wenn kein kaufmännisches und von der Bezeichnung " **Command. labeltitle** " oder "UI pkey" angegeben wird \_ \_ , wird kein KeyTip oder keine Tastatur Beschleunigung bereitgestellt.

Wenn für **Command. KeyTip** kein Wert angegeben wird, ist das untergeordnete [**Zeichen**](windowsribbon-element-string.md) folgen Element erforderlich.

> [!Note]  
> Wenn **Command. KeyTip** sowohl einen Wert als auch ein untergeordnetes [**Zeichen**](windowsribbon-element-string.md) folgen Element enthält, hat die **Zeichenfolge** Vorrang.

 

Standardmäßig werden die folgenden Buchstaben vom Framework verwendet, um KeyTips automatisch zu generieren:

-   **F** wird dem [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)zugewiesen.
-   **Y** wird einem Befehl zugewiesen, der keinen KeyTip hat, der von der Anwendung angegeben wird.
-   **Z** wird jedem [Gruppen](windowsribbon-controls-group.md) Steuerelement zugewiesen und kann nicht angepasst werden. Ein gruppenkeytip wird nur angezeigt, wenn die [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) für das-Steuerelement eine **Popup** Größen Option angibt. Weitere Informationen finden Sie unter [Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md).

> [!Note]  
> Keiner dieser Buchstaben wird vom Framework reserviert. Jeder kann einem oder mehreren Befehlen nach Bedarf zugewiesen werden.

 

Das Framework löst KeyTip-Konflikte wie folgt auf:

-   Wenn ein oder mehrere [Register](windowsribbon-controls-tab.md) Karten-Steuerelemente demselben KeyTip zugeordnet sind, wird eine Zahl an jeden KeyTip angehängt, beginnend bei 1 und erhöht sequenziell (2, 3,...) für jedes Steuerelement in der Reihenfolge der Deklaration. Wenn einem Tabstopp Steuerelement der Buchstabe F als KeyTip zugewiesen ist, wird dem [Anwendungsmenü](windowsribbon-controls-applicationmenu.md) F1 mit den restlichen KeyTips zugewiesen, wie beschrieben.
-   Wenn ein einzelnes Steuerelement innerhalb einer [Registerkarte](windowsribbon-controls-tab.md)zugeordnet ist, ist der KeyTip F sowohl für das Steuerelement als auch für das [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)gültig. Der standardmäßige Anwendungsmenü-KeyTip wird nicht geändert, aber dem Steuerelement auf der aktiven Registerkarte wird eine Rangfolge zugewiesen.
-   Wenn ein oder mehrere Steuerelemente innerhalb einer [Registerkarte](windowsribbon-controls-tab.md) demselben KeyTip zugeordnet sind, werden die KeyTips dieser Steuerelemente vom Framework automatisch neu erstellt, wie zuvor beschrieben.

> [!Note]  
> Eine geringfügige Variation der Textfarbe wird verwendet, um umgestaltete KeyTips in einer Standard-Multifunktionsleisten-Implementierung hervorzuheben. Bei einer nicht standardmäßigen Multifunktionsleisten-Implementierung, bei der die Multifunktionsleisten Farbe angepasst wurde, wird dieses frameworkverhalten außer Kraft gesetzt, und alle KeyTips werden mit der gleichen Textfarbe angezeigt. Weitere Informationen finden Sie unter [Anpassen von Menüband-Farben](ribbon-color.md).

 

Die maximale Länge ist unbegrenzt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command**](windowsribbon-element-command.md) -Element mit der **Command. KeyTip** -Deklaration veranschaulicht.


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[UI- \_ pkey- \_ KeyTip](windowsribbon-reference-properties-uipkey-keytip.md)
</dt> </dl>

 

 





