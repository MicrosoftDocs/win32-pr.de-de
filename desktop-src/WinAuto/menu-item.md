---
title: Menüelement (REFERENZ ZUM MSAA-UI-Element)
description: Ein Menüelement stellt ein bestimmtes Element in einer Menüleiste oder einem Popupmenü dar.
ms.assetid: 330782d6-4293-4e65-ab49-a616d133d273
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1b90162f386314ac495ed138ccf4d180d2f53b8b1e6126287c79a1d75d40be2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644500"
---
# <a name="menu-item-msaa-ui-element-reference"></a>Menüelement (REFERENZ ZUM MSAA-UI-Element)

> [!Note]  
> In diesem Thema werden **Menüelementobjekte für** die MsAA-Benutzeroberflächenelementreferenz beschrieben. Das Erstellen von **Menüelementobjekten** in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenzdokumentation für das benutzeroberflächenframework, das Sie verwenden.

 

Ein Menüelement stellt ein bestimmtes Element in einer Menüleiste oder einem Popupmenü dar. Beispielsweise erstellt Microsoft Active Accessibility ein Menüelementobjekt für das Menü **Datei** in der Menüleiste. Ebenso wird Microsoft Active Accessibility Menüelementobjekt für das  Menüelement Öffnen aus dem **Popupmenü** Datei erstellt.

Der Name der Fensterklasse für ein Menüelement ist \# "32768".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein Menüelement unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Methode                                                                    | Kommentare                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Für Menüelemente in der Menüleiste zeigt [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) das Menü je nach Status des Menüs entweder an oder schließt es. Für Menüelemente aus einem Popupmenü **klickt accDoDefaultAction** auf das Menüelement, um den Menübefehl auszuführen. |
| [**acchittest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                                |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                                |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                                |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                                |



 

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Menüelement unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Ruft die [**IDispatch-Schnittstelle**](idispatch-interface.md) für das Popupmenüobjekt für dieses Element ab.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **ChildCount-Eigenschaft** ist eine Eigenschaft für Menüelemente, die ein Menü oder Untermenü anzeigen. Andernfalls **ist die ChildCount-Eigenschaft** 0 (null).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Die **DefaultAction-Eigenschaft** für Menüelemente, die ein Menü oder Untermenü anzeigen, ist abhängig vom Status des Menüs entweder "Öffnen" oder "Schließen". Die **DefaultAction-Eigenschaft** für alle anderen Menüelemente ist "Execute".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut-Eigenschaft** ist die Zugriffsschlüssel des Menüelements. Dies ist das unterstrichene Zeichen im Text des Namens des Menüelements. Die **KeyboardShortcut-Eigenschaft** für das Menüelement Datei ist beispielsweise "f".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name-Eigenschaft** ist identisch mit dem Namen des Menüelements.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die **Parent-Eigenschaft** ist die Menüleiste oder das Popupmenü, die das Menüelement enthält.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ MENUITEM.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State-Eigenschaft** ist entweder STATE SYSTEM INVISIBLE oder eine Kombination aus mindestens einem der folgenden Werte: [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM [**\_ \_**](object-state-constants.md) \| [**\_ \_ CHECKED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ DEFAULT**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ HOTTRACKED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE \_ SYSTEM \_ HASPOPUP**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Hinweise

-   Bei Verwendung in einem Menüelement gibt [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) S OK zurück, kann die Aktion jedoch nicht ausführen, wenn das im Zugriffsschlüssel verwendete Zeichen ?, !, @ oder ein anderes Zeichen ist, das die UMSCHALTTASTE oder einen anderen Modifiziererschlüssel \_ erfordert. Dies geschieht auch auf internationalen Tastaturen mit einem Zugriffstastenzeichen, bei dem die ALT GR-Taste gedrückt werden muss.
-   Die [**accSelect-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) [**mit SELFLAG \_ TAKEFOCUS**](selflag.md) führt nicht dazu, dass ein Menüelement ein Popupmenü öffnet oder schließt. Clients verwenden die [**accDoDefaultAction-Methode,**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) um ein Popupmenü zu öffnen oder zu schließen.
-   Ein Menüleistenelement, in dem kein Popupmenü angezeigt wird, gibt "Anwendung" für die **Name-Eigenschaft** anstelle des Namens des Menüelements zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Menüleiste**](menu-bar.md)
</dt> <dt>

[**Popupmenü**](pop-up-menu.md)
</dt> </dl>

 

 





