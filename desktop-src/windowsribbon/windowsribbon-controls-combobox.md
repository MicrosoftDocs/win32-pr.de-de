---
title: Kombinationsfeld (Windows Menübandframework)
description: Das Kombinationsfeld besteht aus einem einspaltigen Listenfeld, das eine Sammlung von sich gegenseitig ausschließenden Elementen oder Befehlen in Kombination mit einem statischen Steuerelement oder Bearbeitungssteuerelementen und einem Dropdownpfeil enthält.
ms.assetid: 6b7de2ec-dcb7-44cb-b01f-db1ba0643499
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4b6620e436cfaa1a8ed657c647c6881293b24d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474326"
---
# <a name="combo-box-windows-ribbon-framework"></a>Kombinationsfeld (Windows Menübandframework)

Das Kombinationsfeld besteht aus einem einspaltigen Listenfeld, das eine Sammlung von sich gegenseitig ausschließenden Elementen oder Befehlen in Kombination mit einem statischen Steuerelement oder Bearbeitungssteuerelementen und einem Dropdownpfeil enthält. Der Listenfeldteil des Steuerelements wird angezeigt, wenn der Benutzer auf den Dropdownpfeil klickt.

-   [Details](#details)
-   [Kombinationsfeldeigenschaften](#combo-box-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="details"></a>Details

Das aktuell ausgewählte Element oder der Befehl (sofern verfügbar) im Listenfeld wird im statischen Steuerelement oder im Bearbeitungssteuerelement angezeigt. Wenn der Benutzer bei einem Bearbeitungssteuerelement die Anfangszeichen eines vorhandenen Elements oder Befehls eintippst, wird im Listenfeld das erste Element mit diesen Anfangszeichen angezeigt und der Eintrag im Bearbeitungssteuerelement automatisch vervollständigt.

Unterstützt nur einen vertikalen Strich oder ein Größenverdringen.

Dieses Steuerelement ist nützlich, um einfache, eng verwandte Textelemente verfügbar zu machen.

Der folgende Screenshot veranschaulicht das Menüband-Kombinationsfeld in live Movie Maker.

![Screenshot eines Kombinationsfeld-Steuerelements im Microsoft-Farbband.](images/controls/combobox.png)

## <a name="combo-box-properties"></a>Kombinationsfeldeigenschaften

Das Menübandframework definiert eine Sammlung von [Eigenschaftsschlüsseln](windowsribbon-reference-properties.md) für das Combo Box-Steuerelement.

In der Regel wird eine Combo Box-Eigenschaft in der Menübandbenutzeroberfläche aktualisiert, indem der befehl, der dem Steuerelement zugeordnet ist, durch einen Aufruf der [**IUIFramework::InvalidateUICommand-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ungültig wird. Das Invalidierungsereignis wird von der [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) behandelt und die Eigenschaft aktualisiert.

Die [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) wird nicht ausgeführt, und die Anwendung fragt einen aktualisierten Eigenschaftswert ab, bis die Eigenschaft vom Framework benötigt wird. Beispielsweise, wenn eine Registerkarte aktiviert und ein Steuerelement auf der Menübandbenutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft über die [**IUIFramework::GetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) abgerufen und mit der [**IUIFramework::SetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschaftenschlüssel aufgeführt, die dem Combo Box-Steuerelement zugeordnet sind.




| Eigenschaftsschlüssel | Hinweise | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a> | Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a> | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a> | 
| <a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a> | Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a> | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a> | Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a> | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-stringvalue.md">UI_PKEY_StringValue</a> | Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a><blockquote>[!Note]<br />Wenn der dem Steuerelement zugeordnete Befehl durch einen Aufruf von <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>ungültig gemacht wird, fragt das Framework diese Eigenschaft ab, wenn als Wert von flags übergeben <code>UI_INVALIDATIONS_VALUE</code> <em>wird.</em></blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Menüband-Framework-Steuerelementbibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**ComboBox-Markupelement**](windowsribbon-element-combobox.md)
</dt> <dt>

[Arbeiten mit Katalogen](ribbon-controls-galleries.md)
</dt> <dt>

[Katalogbeispiel](windowsribbon-gallerysample.md)
</dt> </dl>

