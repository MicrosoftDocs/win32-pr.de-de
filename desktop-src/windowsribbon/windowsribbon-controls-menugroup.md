---
title: Menü Gruppe
description: Die Menü Gruppe organisiert verwandte Befehle und Steuerelemente in einem Menü oder einer Symbolleiste.
ms.assetid: 5454f2a3-275b-47f4-ae97-d10dd12da5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9862e78cbedf84b92c7540bec4de58288af5c9ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949008"
---
# <a name="menu-group"></a>Menü Gruppe

Die Menü Gruppe organisiert verwandte Befehle und Steuerelemente in einem Menü oder einer Symbolleiste.

-   [Introduction (Einführung)](#introduction)
-   [Menü Gruppen Eigenschaften](#menu-group-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Das Menü Gruppen Steuerelement, das über das [**MenuGroup**](windowsribbon-element-menugroup.md) -Markup Element verfügbar gemacht wird, ist ein logischer Container für Gruppen von Elementen oder Befehlen in menübasierten Steuerelementen, einschließlich der [Kontext-Popup](windowsribbon-controls-contextpopup.md) -Mini Symbolleiste.

Eine Bezeichnung kann für eine Menü Gruppe über das Attribut " *labeltitle* " oder die Eigenschaft " [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) " einer zugeordneten Befehls Deklaration angegeben werden. Der *labeltitle* zugewiesene Wert wird als Kategorieheader gerendert.

Das folgende Beispiel veranschaulicht das Befehls Markup für ein Steuerelement unter [teilte Schalt](windowsribbon-controls-splitbutton.md) Flächen, das zwei Menü Gruppen-Befehls Deklarationen enthält.


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



Das folgende Beispiel zeigt das Markup, das für ein [**SplitButton**](windowsribbon-element-splitbutton.md) -Element mit drei [**MenuGroup**](windowsribbon-element-menugroup.md) -Element Deklarationen erforderlich ist, von denen zwei mit den Menü Gruppen Befehlen aus dem vorherigen Beispiel verknüpft sind. Das *Class* -Attribut des **MenuGroup** -Elements wird verwendet, um die Größe der Menü Elemente anzugeben.


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



Der folgende Screenshot veranschaulicht das Menü (mit drei Menü Gruppen-Steuerelementen), das aus dem Markup in den vorherigen Beispielen generiert wird.

![Screenshot eines Menüs mit drei Menü Gruppen-Steuerelementen.](images/controls/menugroup.png)

## <a name="menu-group-properties"></a>Menü Gruppen Eigenschaften

Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Menü Gruppen-Steuerelement.

In der Regel wird eine Menü Gruppen Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird. Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.

Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird. Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.

 

In der folgenden Tabelle werden die Eigenschaften Schlüssel aufgelistet, die dem Menü Gruppen-Steuerelement zugeordnet sind.



| Eigenschafts Schlüssel                                                                                     | Notizen                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [UI- \_ pkey \_ aktiviert](windowsribbon-reference-properties-uipkey-enabled.md)                       | Unterstützt [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) und [**iuiframework:: abtuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [UI- \_ pkey- \_ KeyTip](windowsribbon-reference-properties-uipkey-keytip.md)                         | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |
| [UI- \_ pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)                           | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |
| [UI- \_ pkey- \_ tooltipdescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |
| [UI- \_ pkey- \_ ToolTipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Menüband-Steuerelement Bibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**MenuGroup-Markup Element**](windowsribbon-element-menugroup.md)
</dt> </dl>

 

 