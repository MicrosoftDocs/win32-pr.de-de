---
title: Menu Item (MSAA UI-Element Referenz)
description: Ein Menü Element stellt ein bestimmtes Element in einer Menüleiste oder in einem Popupmenü dar.
ms.assetid: 330782d6-4293-4e65-ab49-a616d133d273
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cb6621a14927cc4dc9af9f3384157e60ce6570d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037164"
---
# <a name="menu-item-msaa-ui-element-reference"></a>Menu Item (MSAA UI-Element Referenz)

> [!Note]  
> In diesem Thema werden **Menü Element** Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben. Das Erstellen von **Menü Element** Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Ein Menü Element stellt ein bestimmtes Element in einer Menüleiste oder in einem Popupmenü dar. Beispielsweise erstellt Microsoft Active Accessibility ein Menü Element Objekt für das Menü **Datei** in der Menüleiste. Auf ähnliche Weise erstellt Microsoft Active Accessibility ein Menü Element Objekt für das Menü Element **Öffnen** im Popup Menü **Datei** .

Der Fenster Klassenname für ein Menü Element ist " \# 32768".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein Menü Element unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:



| Methode                                                                    | Kommentare                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Für Menü Elemente in der Menüleiste zeigt [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) das Menü abhängig vom Zustand des Menüs an oder schließt es. Für Menü Elemente in einem Popup Menü klickt " **accDoDefaultAction** " auf das Menü Element, um den Menübefehl auszuführen. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                                |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                                |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                                |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                                |



 

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Menü Element unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_accChild erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Ruft die [**IDispatch**](idispatch-interface.md) -Schnittstelle zum Popup-Menü Objekt für dieses Element ab.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **childCount** -Eigenschaft ist eine für Menü Elemente, die ein Menü oder ein Untermenü anzeigen. Andernfalls ist die **childCount** -Eigenschaft 0 (null).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accdefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Die **DEFAULTACTION** -Eigenschaft für Menü Elemente, die ein Menü oder ein Untermenü anzeigen, ist abhängig vom Zustand des Menüs entweder "Öffnen" oder "Schließen". Die **DEFAULTACTION** -Eigenschaft für alle anderen Menü Elemente ist "Execute".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_accKeyboardShortcut erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut** -Eigenschaft ist die Zugriffstaste des Menü Elements, bei der es sich um das unterstrichene Zeichen im Text des Menü Element namens handelt. Die **KeyboardShortcut** -Eigenschaft für das Menü Element "file" lautet beispielsweise "f".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name** -Eigenschaft entspricht dem Namen des Menü Elements.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die über **geordnete** Eigenschaft ist die Menüleiste oder das Popup Menü, das das Menü Element enthält.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role** -Eigenschaft ist " [**role \_ System \_ MenuItem**](object-roles.md)".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State** -Eigenschaft ist entweder [**Zustands \_ System \_ unsichtbar**](object-state-constants.md) oder eine Kombination aus einem oder mehreren der folgenden Werte: Zustands System-nicht [**\_ \_ verfüg**](object-state-constants.md) Bare Zustands System-Integritäts Integritäts Integritäts Status System mit System \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ integriertem**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) Zustands System<br/> |



 

## <a name="notes"></a>Notizen

-   Bei Verwendung in einem Menü Element gibt " [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) " den Wert "S OK" zurück, kann \_ die Aktion jedoch nicht ausführen, wenn das in der Zugriffstaste verwendete Zeichen?,!, @ ist, oder ein beliebiges anderes Zeichen, das die UMSCHALTTASTE oder einen anderen modifiziererschlüssel erfordert. Dies geschieht auch bei internationalen Tastaturen mit einem Zugriffsschlüssel Zeichen, für das die Alt-Gr-Taste gedrückt werden muss.
-   Die Methode [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) mit [**selflag \_ TakeFocus**](selflag.md) bewirkt nicht, dass ein Menü Element ein Popup Menü öffnet oder schließt. Clients verwenden die [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) -Methode, um ein Popupmenü zu öffnen oder zu schließen.
-   Ein Menüleisten Element, das kein Popup Menü anzeigt, gibt "Application" anstelle des Namens des Menü Elements für die Eigenschaft " **Name** " zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Menüleiste**](menu-bar.md)
</dt> <dt>

[**Popup Menü**](pop-up-menu.md)
</dt> </dl>

 

 





