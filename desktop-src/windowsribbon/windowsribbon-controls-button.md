---
title: Schaltfläche (Windows Menübandframework)
description: Die Schaltfläche ist ein Steuerelement, auf das der Benutzer klicken kann, um eine Eingabe für eine Anwendung bereitzustellen.
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82a1a71181b3478e065922b5a1836f6cd0f47bf9b3f2e497f45564118449b95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707793"
---
# <a name="button-windows-ribbon-framework"></a>Schaltfläche (Windows Menübandframework)

Die Schaltfläche ist ein Steuerelement, auf das der Benutzer klicken kann, um eine Eingabe für eine Anwendung bereitzustellen.

-   [Introduction (Einführung)](#introduction)
-   [Schaltflächeneigenschaften](#button-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Der folgende Screenshot enthält drei Beispiele für das Menüband-Schaltflächenelement.

![Screenshot der Schaltflächensteuerelemente im Microsoft Wordpad-Menüband.](images/controls/button.png)

## <a name="button-properties"></a>Schaltflächeneigenschaften

Das Menübandframework definiert eine Auflistung von [Eigenschaftsschlüsseln](windowsribbon-reference-properties.md) für das Schaltflächen-Steuerelement.

In der Regel wird eine Button-Eigenschaft auf der Menübandbenutzeroberfläche aktualisiert, indem der dem Steuerelement zugeordnete Befehl durch einen Aufruf der [**IUIFramework::InvalidateUICommand-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ungültig wird. Das Invalidierungsereignis wird von der [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) behandelt und die Eigenschaft aktualisiert.

Die [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) wird nicht ausgeführt, und die Anwendung fragt einen aktualisierten Eigenschaftswert ab, bis die Eigenschaft vom Framework benötigt wird. Beispielsweise, wenn eine Registerkarte aktiviert und ein Steuerelement auf der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft über die [**IUIFramework::GetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) abgerufen und mit der [**IUIFramework::SetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschaftenschlüssel aufgeführt, die dem Button-Steuerelement zugeordnet sind.



| Eigenschaftenschlüssel                                                                                             | Hinweise                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_Benutzeroberflächen-PKEY \_ aktiviert](windowsribbon-reference-properties-uipkey-enabled.md)                               | Unterstützt [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) und [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) |
| [\_PKEY-Keytip der Benutzeroberfläche \_](windowsribbon-reference-properties-uipkey-keytip.md)                                 | Kann nur durch Ungültigkeit aktualisiert werden.                                                                                                                                                                                     |
| [\_ \_ UI-PKEY-Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)                                   | Kann nur durch Ungültigkeit aktualisiert werden.                                                                                                                                                                                     |
| [UI \_ PKEY \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)             | Kann nur durch Ungültigkeit aktualisiert werden.                                                                                                                                                                                     |
| [UI \_ PKEY \_ LargeHighContrastImage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md) | Kann nur durch Ungültigkeit aktualisiert werden.                                                                                                                                                                                     |
| [UI \_ PKEY \_ LargeImage](windowsribbon-reference-properties-uipkey-largeimage.md)                         | Kann nur durch Ungültigkeit aktualisiert werden.                                                                                                                                                                                     |
| [UI \_ PKEY \_ SmallHighContrastImage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md) | Kann nur durch Ungültigkeit aktualisiert werden.                                                                                                                                                                                     |
| [UI \_ PKEY \_ SmallImage](windowsribbon-reference-properties-uipkey-smallimage.md)                         | Kann nur durch Ungültigkeit aktualisiert werden.                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)         | Kann nur durch Ungültigkeit aktualisiert werden.                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)                     | Kann nur durch Ungültigkeit aktualisiert werden.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Menüband-Framework-Steuerelementbibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**Markupelement für Schaltflächen**](windowsribbon-element-button.md)
</dt> </dl>

 

 
