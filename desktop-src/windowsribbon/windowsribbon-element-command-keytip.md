---
title: Command.Keytip-Eigenschaft
description: Stellt die Keytip für ein -Steuerelement dar.
ms.assetid: 214f69ae-dd35-4abf-b294-d898d7802aa6
keywords:
- Command.Keytip-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- Command.Keytip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d70edeae49a2acbd561bd4d56e32028852993cc524a0df3882e7e0b8a8da18b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964243"
---
# <a name="commandkeytip-property"></a>Command.Keytip-Eigenschaft

Stellt die Keytip für ein -Steuerelement dar.

## <a name="usage"></a>Verwendung

``` syntax
<Command.Keytip>
  child elements
</Command.Keytip>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                   | Beschreibung                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**String**](windowsribbon-element-string.md)<br/> | Kann nur einmal auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                     |
|-------------------------------------------------------------|
| [**Get-Help**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann für jedes [**Command-Element mindestens einmal**](windowsribbon-element-command.md) auftreten.

**Command.Keytip kann** einen Wert vom Typ *xs:string* enthalten, der auf eine beliebige Sequenz von Unicode-Zeichen, einschließlich Leerzeichen, beschränkt ist.

Eine **Command.Keytip kann** nur mit einer Zahl beginnen, wenn sie einem Steuerelement innerhalb einer [Registerkarte](windowsribbon-controls-tab.md) oder der Symbolleiste für den [Schnellzugriff zugeordnet ist.](windowsribbon-controls-quickaccesstoolbar.md)

Drücken Sie die ALT-TASTE, und halten Sie sie gedrückt, um die Für den aktuellen Zustand des Menübands gültigen Tastentips anzuzeigen. Der folgende Screenshot zeigt die KeyTips der anfänglichen oder ersten Ebene, die in Microsoft Paint für Windows 7 angezeigt werden. Nachdem eine Keytip der ersten Ebene ausgewählt wurde, werden nur KeyTips der zweiten Ebene angezeigt.

![Keytips der ersten Ebene in Microsoft Paint für Windows 7](images/properties/ui-pkey-label-keytips.png)

**Command.Keytip fungiert** als Zugriffstaste für einen Befehl, es sei denn, dieser Befehl wird über ein Menüelement verfügbar gemacht. In diesem Fall ignoriert das Framework den **Command.Keytip-Wert** und verwendet stattdessen ein Zeichen, dem ein ampersand voran geht, wie durch [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) oder [UI \_ PKEY \_ Label angegeben.](windowsribbon-reference-properties-uipkey-label.md) Wenn kein ampersand durch **Command.LabelTitle** oder UI PKEY Label angegeben wird, wird keine Tastenkombination oder \_ \_ Tastenkombination verfügbar gemacht.

Wenn für **Command.Keytip** kein Wert angegeben wird, ist das [**untergeordnete String-Element**](windowsribbon-element-string.md) erforderlich.

> [!Note]  
> Wenn **Command.Keytip sowohl** einen Wert als auch ein untergeordnetes [**String-Element**](windowsribbon-element-string.md) enthält, hat **String** Vorrang.

 

Standardmäßig werden die folgenden Buchstaben vom Framework verwendet, um automatisch Keytips zu generieren:

-   **F** wird dem [Anwendungsmenü zugewiesen.](windowsribbon-controls-applicationmenu.md)
-   **Y** wird jedem Befehl zugewiesen, für den von der Anwendung kein Keytip angegeben wurde.
-   **Z** wird jedem [Gruppensteuer steuerelement zugewiesen](windowsribbon-controls-group.md) und kann nicht angepasst werden. Eine Gruppen-Keytip wird nur angezeigt, wenn [**scalingPolicy**](windowsribbon-element-scalingpolicy.md) für das Steuerelement eine **Popupgrößenoption** angibt. Weitere Informationen finden Sie unter [Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien.](windowsribbon-templates.md)

> [!Note]  
> Keiner dieser Buchstaben ist vom Framework reserviert. Jeder kann je nach Bedarf einem oder mehrere Befehle zugewiesen werden.

 

Das Framework löst KeyTip-Konflikte auf folgende Weise:

-   Wenn ein [](windowsribbon-controls-tab.md) oder mehrere Tabstoppsteuerelemente demselben Keytip zugeordnet sind, wird jedem Keytip eine Zahl angefügt, beginnend bei 1, und wird sequenziell (2, 3,...) für jedes Steuerelement in der Reihenfolge der Deklaration erhöht. Wenn einem Tabstoppsteuerelement der Buchstabe F als [](windowsribbon-controls-applicationmenu.md) Keytip zugewiesen wird, wird dem Anwendungsmenü F1 zugewiesen, und die restlichen Keytips werden wie beschrieben angepasst.
-   Wenn sie einem einzelnen Steuerelement innerhalb einer Registerkarte zugeordnet [ist,](windowsribbon-controls-tab.md)ist die Tastentipf F sowohl für das Steuerelement als auch für das [Anwendungsmenü gültig.](windowsribbon-controls-applicationmenu.md) Die Standardtasteninfo des Anwendungsmenüs wird nicht geändert, aber dem Steuerelement auf der aktiven Registerkarte wird Vorrang gegeben.
-   Wenn ein oder mehrere [](windowsribbon-controls-tab.md) Steuerelemente innerhalb einer Registerkarte demselben KeyTip zugeordnet sind, umgestaltiert das Framework automatisch die KeyTips dieser Steuerelemente, wie zuvor beschrieben.

> [!Note]  
> Eine geringfügige Abweichung der Textfarbe wird verwendet, um umgestaltierte Keytips in einer Standard-Menübandimplementierung hervorzuheben. Bei einer nicht standardmäßigen Menübandimplementierung, bei der die Menübandfarbe angepasst wurde, wird dieses Frameworkverhalten überschrieben, und alle Keytips werden mit der gleichen Textfarbe angezeigt. Weitere Informationen finden Sie unter [Anpassen von Menübandfarben.](ribbon-color.md)

 

Die maximale Länge ist ungebunden.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command-Element**](windowsribbon-element-command.md) mit einer **Command.Keytip-Deklaration** veranschaulicht.


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
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[\_ \_ PKEY-Keytip der Benutzeroberfläche](windowsribbon-reference-properties-uipkey-keytip.md)
</dt> </dl>

 

 





