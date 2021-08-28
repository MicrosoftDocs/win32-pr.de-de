---
title: Gruppe (Windows Menübandframework)
description: Die Gruppe organisiert verwandte Befehle und Steuerelemente auf einer Registerkarte.
ms.assetid: 5d098d3f-a4ee-4f76-8c81-832d0c49cb80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c153f8cd9d1fc0d2d2bdbaabab0b2e15e099e50d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467417"
---
# <a name="group-windows-ribbon-framework"></a>Gruppe (Windows Menübandframework)

Die Gruppe organisiert verwandte Befehle und Steuerelemente innerhalb einer [Registerkarte](windowsribbon-controls-tab.md).

-   [Details](#details)
-   [Gruppeneigenschaften](#group-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="details"></a>Details

Der folgende Screenshot veranschaulicht das Menübandgruppen-Steuerelement.

![Screenshot mit Callouts, die eine Gruppe anzeigen.](images/controls/group.png)

## <a name="group-properties"></a>Gruppeneigenschaften

Das Menübandframework definiert eine Auflistung von [Eigenschaftsschlüsseln](windowsribbon-reference-properties.md) für das Gruppensteuerelement.

In der Regel wird eine Group-Eigenschaft auf der Menübandbenutzeroberfläche aktualisiert, indem der dem Steuerelement zugeordnete Befehl durch einen Aufruf der [**IUIFramework::InvalidateUICommand-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ungültig wird. Das Invalidierungsereignis wird von der [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) behandelt und die Eigenschaft aktualisiert.

Die [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) wird nicht ausgeführt, und die Anwendung fragt einen aktualisierten Eigenschaftswert ab, bis die Eigenschaft vom Framework benötigt wird. Beispielsweise, wenn eine Registerkarte aktiviert und ein Steuerelement auf der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft über die [**IUIFramework::GetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) abgerufen und mit der [**IUIFramework::SetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschaftenschlüssel aufgeführt, die dem Gruppensteuerelement zugeordnet sind.




| Eigenschaftenschlüssel | Hinweise | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Kann nur durch Invalidierung aktualisiert werden.<blockquote>[!Note]<br />Das Framework erfordert, dass der Wert von <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> für ein Gruppensteuerelement mit dem Großbuchstaben Z beginnt. Wenn der von der Anwendung in der <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler::UpdateProperty-Rückrufmethode</strong></a> angegebene Wert nicht mit dem Buchstaben Z beginnt, wird dieser Wert ignoriert, und stattdessen wird ein Wert vom Framework generiert. Der Frameworkwert ist der Buchstabe Z, gefolgt von einem numerischen Wert, der bei 1 beginnt und nach Bedarf für nachfolgende Gruppensteuerelemente (Z1, Z2, ..., Zx) sequenziell zunimmt.</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Kann nur durch Invalidierung aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Kann nur durch Invalidierung aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Kann nur durch Invalidierung aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Kann nur durch Invalidierung aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Kann nur durch Invalidierung aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Kann nur durch Invalidierung aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Kann nur durch Invalidierung aktualisiert werden. | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Menüband-Framework-Steuerelementbibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**Group-Element**](windowsribbon-element-group.md)
</dt> </dl>

