---
title: Hilfe Schaltfläche
description: Die Schaltfläche Hilfe ist ein Steuerelement, auf das der Benutzer klicken kann, um das Anwendungs Hilfesystem anzuzeigen.
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc44c9f9a03561f1627067849272509838d7a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948759"
---
# <a name="help-button"></a>Hilfe Schaltfläche

Die Schaltfläche Hilfe ist ein Steuerelement, auf das der Benutzer klicken kann, um das Anwendungs Hilfesystem anzuzeigen.

-   [Details](#details)
-   [Hilfe-Schaltflächen Eigenschaften](#help-button-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="details"></a>Details

Der folgende Screenshot veranschaulicht die Menüband-Hilfe Schaltfläche.

![Screenshot mit der Schaltfläche "Hilfe"](images/controls/helpbutton.png)

## <a name="help-button-properties"></a>Hilfe-Schaltflächen Eigenschaften

Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Hilfe Button-Steuerelement.

In der Regel wird eine Hilfe Schaltflächen Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird. Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.

Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird. Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.

 

In der folgenden Tabelle werden die Eigenschaften Schlüssel aufgelistet, die dem Schaltflächen-Steuerelement "Hilfe" zugeordnet sind.



| Eigenschafts Schlüssel                                                                                     | Notizen                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [UI- \_ pkey- \_ KeyTip](windowsribbon-reference-properties-uipkey-keytip.md)                         | Kann nur durch Invalidierung aktualisiert werden. |
| [UI- \_ pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)                           | Kann nur durch Invalidierung aktualisiert werden. |
| [UI- \_ pkey- \_ tooltipdescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Kann nur durch Invalidierung aktualisiert werden. |
| [UI- \_ pkey- \_ ToolTipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Kann nur durch Invalidierung aktualisiert werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Menüband-Steuerelement Bibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**HelpButton-Element**](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 