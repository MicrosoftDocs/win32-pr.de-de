---
title: Schaltfläche (Windows-Menü Band Framework)
description: Die Schaltfläche ist ein Steuerelement, auf das der Benutzer klicken kann, um Eingaben für eine Anwendung bereitzustellen.
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1514a1ae66e383d18f81d1ca0ee1a5a8e453335d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102646"
---
# <a name="button-windows-ribbon-framework"></a>Schaltfläche (Windows-Menü Band Framework)

Die Schaltfläche ist ein Steuerelement, auf das der Benutzer klicken kann, um Eingaben für eine Anwendung bereitzustellen.

-   [Introduction (Einführung)](#introduction)
-   [Schaltflächen Eigenschaften](#button-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Der folgende Screenshot enthält drei Beispiele für das Menüband-Schaltflächen Element.

![Screenshot der Schaltflächen-Steuerelemente im Microsoft WordPad-Menüband.](images/controls/button.png)

## <a name="button-properties"></a>Schaltflächen Eigenschaften

Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Schaltflächen-Steuerelement.

In der Regel wird eine Schaltflächen Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird. Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.

Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird. Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschafts Schlüssel aufgelistet, die dem Schaltflächen-Steuerelement zugeordnet sind.



| Eigenschafts Schlüssel                                                                                             | Notizen                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [UI- \_ pkey \_ aktiviert](windowsribbon-reference-properties-uipkey-enabled.md)                               | Unterstützt [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) und [**iuiframework:: abtuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [UI- \_ pkey- \_ KeyTip](windowsribbon-reference-properties-uipkey-keytip.md)                                 | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |
| [UI- \_ pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)                                   | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |
| [UI \_ pkey \_ labeldescription](windowsribbon-reference-properties-uipkey-labeldescription.md)             | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |
| [UI \_ pkey \_ largehighkontra stimage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md) | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |
| [UI \_ pkey \_ largeimage](windowsribbon-reference-properties-uipkey-largeimage.md)                         | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |
| [UI \_ pkey \_ smallhighkontra stimage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md) | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |
| [UI \_ pkey \_ smallImage](windowsribbon-reference-properties-uipkey-smallimage.md)                         | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |
| [UI- \_ pkey- \_ tooltipdescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)         | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |
| [UI- \_ pkey- \_ ToolTipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)                     | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Menüband-Steuerelement Bibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**Button-Markup Element**](windowsribbon-element-button.md)
</dt> </dl>

 

 
