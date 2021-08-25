---
title: Popupmenü (MSAA UI-Elementreferenz)
description: In einem Popupmenü wird eine Liste mit Menübefehlen angezeigt.
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b578a6af66585e06c4d9392f7051a8ebf14c8c24865bac59bf0c4fa43c7deaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861390"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a>Popupmenü (MSAA UI-Elementreferenz)

> [!Note]  
> In diesem Thema werden **Popupmenüobjekte** für Die MSAA UI-Elementreferenz beschrieben. Das Erstellen von **Popupmenüobjekten** in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Informationen zum verwendeten BENUTZERoberflächenframework finden Sie in der API-Referenzdokumentation.

 

In einem Popupmenü wird eine Liste mit Menübefehlen angezeigt. Microsoft Active Accessibility erstellt ein Popupobjekt im Menü, wenn ein Menüelement in einer Menüleiste geöffnet wird. Microsoft Active Accessibility erstellt auch Popupobjekte für Kontextmenüs, die angezeigt werden, wenn der Benutzer mit der rechten Maustaste auf ein Benutzeroberflächenelement klickt.

Der Name der Fensterklasse für ein Popupmenü lautet " \# 32768".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein Popupmenü unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Popupmenü unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                 | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | Ruft den [**IDispatch**](idispatch-interface.md) für das angegebene Menüelement ab. Die untergeordneten IDs für die Menüelemente werden sequenziell von oben nach unten nummeriert, beginnend mit 1.                                                                                                                                                                                                                                                                                      |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Die **ChildCount-Eigenschaft** ist die Anzahl der Menüelemente im Menü, einschließlich Menütrennzeichen.                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | Die **Name-Eigenschaft** für ein Popupmenü entspricht dem Namen des Menüs. Die **Name-Eigenschaft** für ein Kontextmenü lautet "Context".                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Die **Parent-Eigenschaft** ist ein Fenster ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) ), das das Popupmenü umschließt und über die gleiche **Name-Eigenschaft** und den gleichen Fensterklassennamen wie das Popupmenü verfügt.                                                                                                                                                                                                                                                      |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ MENUPOPUP.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | Die **State-Eigenschaft** ist eine Kombination aus einem oder mehreren der folgenden [Werte:](object-state-constants.md) [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Hinweise

-   Popupmenüobjekte lösen keine [**EVENT \_ OBJECT \_ CREATE-**](event-constants.md) und [**EVENT OBJECT \_ \_ DESTROY-Ereignisse**](event-constants.md) aus.
-   Menüs mit mehreren Spalten unterstützen nicht die [**Flags NAVDIR \_ LEFT**](navigation-constants.md) oder [**NAVDIR \_ RIGHT**](navigation-constants.md) der [**accNavigate-Methode.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   Die Ereignisse [**EVENT \_ SYSTEM \_ MENUPOPUPSTART**](event-constants.md) und [**EVENT SYSTEM \_ \_ MENUPOPUPEND**](event-constants.md) werden nicht konsistent gesendet. Dies ist ein bekanntes Problem, das behoben wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Menüleiste**](menu-bar.md)
</dt> <dt>

[**Menüelement**](menu-item.md)
</dt> </dl>

 

 





