---
title: Drop-Down-Schaltfläche
description: Die Drop-Down-Schaltfläche besteht aus einer Schaltfläche, die beim Klicken eine Dropdownliste mit sich gegenseitig ausschließenden Elementen anzeigt.
ms.assetid: 41c5da07-43f7-4544-83be-248941cb8633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887b5979d5536b255526789aa541a6f2d1b67d1b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473516"
---
# <a name="drop-down-button"></a>Drop-Down-Schaltfläche

Die Drop-Down-Schaltfläche besteht aus einer Schaltfläche, die beim Klicken eine Dropdownliste mit sich gegenseitig ausschließenden Elementen anzeigt.

-   [Details](#details)
-   [Eigenschaften der Dropdownschaltfläche](#drop-down-button-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="details"></a>Details

Dieses Steuerelement ist nützlich, um eng verwandte Elemente in Fällen verfügbar zu machen, in denen kein offensichtlicher Standardwert verfügbar ist und die einzelnen Elemente durch ein Bild, Text oder beides dargestellt werden können.

Der folgende Screenshot veranschaulicht das Menüband Drop-Down Schaltfläche in einem Beispielmenüband.

![Screenshot eines Dropdownbutton-Steuerelements in einem Beispielband.](images/controls/dropdownbutton.png)

## <a name="drop-down-button-properties"></a>Drop-Down Schaltflächeneigenschaften

Das Menübandframework definiert eine Auflistung von [Eigenschaftsschlüsseln für](windowsribbon-reference-properties.md) das Drop-Down Schaltflächen-Steuerelement.

In der Regel wird eine Drop-Down Button-Eigenschaft in der Menübandbenutzeroberfläche aktualisiert, indem der befehl, der dem Steuerelement zugeordnet ist, durch einen Aufruf der [**IUIFramework::InvalidateUICommand-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ungültig wird. Das Invalidierungsereignis wird von der [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) behandelt und die Eigenschaft aktualisiert.

Die [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) wird nicht ausgeführt, und die Anwendung fragt einen aktualisierten Eigenschaftswert ab, bis die Eigenschaft vom Framework benötigt wird. Beispielsweise, wenn eine Registerkarte aktiviert und ein Steuerelement auf der Menübandbenutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft über die [**IUIFramework::GetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) abgerufen und mit der [**IUIFramework::SetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschaftsschlüssel aufgeführt, die dem Steuerelement schaltflächenDrop-Down zugeordnet sind.




| Eigenschaftsschlüssel | Hinweise | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a> | Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a> | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a><br /> Wenn alle untergeordneten Elemente deaktiviert sind, legt das Framework <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> false (0) fest. Wenn ein oder mehrere untergeordnete Elemente aktiviert sind, wird andernfalls UI_PKEY_Enabled auf true (-1) festgelegt.<blockquote>[!Important]<br />Die <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled-Eigenschaft</a> für das schaltflächenDrop-Down-Steuerelement sollte ungültig gemacht werden, nachdem ein oder mehrere untergeordnete Elemente aktiviert oder deaktiviert wurden. Dadurch wird sichergestellt, dass das Framework den aktualisierten Eigenschaftswert abfragt und den Zustand des Steuerelements Drop-Down Schaltfläche auf der Menübandbenutzeroberfläche aktualisiert.</blockquote><br /><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a> | Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a> | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a> | Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a><blockquote>[!Note]<br />Wenn der dem Steuerelement zugeordnete Befehl durch einen Aufruf von <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>ungültig gemacht wird, fragt das Framework diese Eigenschaft ab, wenn als Wert von flags übergeben <code>UI_INVALIDATIONS_VALUE</code> <em>wird.</em></blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Menüband-Framework-Steuerelementbibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**DropDownButton-Markupelement**](windowsribbon-element-dropdownbutton.md)
</dt> </dl>
