---
title: Hilfeschaltfläche
description: Die Hilfeschaltfläche ist ein Steuerelement, auf das der Benutzer klicken kann, um das Hilfesystem der Anwendung anzuzeigen.
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 295b3c7feae2aecada128dadbccd093f654c6a6660a68f4790975aee060aaf61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933384"
---
# <a name="help-button"></a>Hilfeschaltfläche

Die Hilfeschaltfläche ist ein Steuerelement, auf das der Benutzer klicken kann, um das Hilfesystem der Anwendung anzuzeigen.

-   [Details](#details)
-   [Eigenschaften der Hilfeschaltfläche](#help-button-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="details"></a>Details

Der folgende Screenshot veranschaulicht die Menüband-Hilfeschaltfläche.

![Screenshot der Hilfeschaltfläche.](images/controls/helpbutton.png)

## <a name="help-button-properties"></a>Eigenschaften der Hilfeschaltfläche

Das Menübandframework definiert eine Auflistung von [Eigenschaftsschlüsseln](windowsribbon-reference-properties.md) für das Steuerelement "Hilfeschaltfläche".

In der Regel wird eine Hilfeschaltfläche-Eigenschaft auf der Menübandbenutzeroberfläche aktualisiert, indem der dem Steuerelement zugeordnete Befehl durch einen Aufruf der [**IUIFramework::InvalidateUICommand-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ungültig wird. Das Invalidierungsereignis wird von der [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) behandelt und die Eigenschaft aktualisiert.

Die [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) wird nicht ausgeführt, und die Anwendung fragt einen aktualisierten Eigenschaftswert ab, bis die Eigenschaft vom Framework benötigt wird. Beispielsweise, wenn eine Registerkarte aktiviert und ein Steuerelement auf der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft über die [**IUIFramework::GetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) abgerufen und mit der [**IUIFramework::SetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschaftenschlüssel aufgeführt, die dem Steuerelement "Hilfeschaltfläche" zugeordnet sind.



| Eigenschaftenschlüssel                                                                                     | Hinweise                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [\_PKEY-Keytip der Benutzeroberfläche \_](windowsribbon-reference-properties-uipkey-keytip.md)                         | Kann nur durch Ungültigkeit aktualisiert werden. |
| [\_ \_ UI-PKEY-Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)                           | Kann nur durch Ungültigkeit aktualisiert werden. |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Kann nur durch Ungültigkeit aktualisiert werden. |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Kann nur durch Ungültigkeit aktualisiert werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Menüband-Framework-Steuerelementbibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**HelpButton-Element**](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 