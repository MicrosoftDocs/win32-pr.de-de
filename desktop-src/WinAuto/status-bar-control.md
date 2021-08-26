---
title: Statusleisten-Steuerelement (REFERENZ ZUM MSAA-UI-Element)
description: Statusleisten zeigen Statusinformationen in einem horizontalen Fenster am unteren Rand eines Anwendungsfensters an.
ms.assetid: e910a5c6-84d5-4ade-abf5-792ff1915021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6c4955bfe10bc7eb224213a8e2e262179d2b122ca4eae210d0d1e72e4635b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998060"
---
# <a name="status-bar-control-msaa-ui-element-reference"></a>Statusleisten-Steuerelement (REFERENZ ZUM MSAA-UI-Element)

> [!Note]  
> In diesem Thema werden **Statusleisten-Steuerelementobjekte** für die MsAA-Benutzeroberflächenelementreferenz beschrieben. Das Erstellen von **Statusleisten-Steuerelementobjekten** in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenzdokumentation für das benutzeroberflächenframework, das Sie verwenden.

 

Statusleisten zeigen Statusinformationen in einem horizontalen Fenster am unteren Rand eines Anwendungsfensters an. Statusleisten werden häufig in Teile unterteilt, sogenannte Bereiche, und in jedem Bereich werden unterschiedliche Statusinformationen angezeigt. Darüber hinaus können Statusleisten Objekte verschiedener Typen enthalten, einschließlich Schaltflächen und Statusleisten. Der Name der Fensterklasse für ein Statusleisten-Steuerelement ist STATUSCLASSNAME, der in Commctrl.h als "msctls \_ statusbar32" definiert ist.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Statusleisten unterstützen die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Statusleisten unterstützen die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                 | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Die **ChildCount-Eigenschaft** ist die Anzahl der Bereiche in der Statusleiste.                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | Das Statusleistenobjekt selbst verfügt nicht über eine **Name-Eigenschaft.** Die **Name-Eigenschaft** jedes Bereichs in der Statusleiste ist mit dem angezeigten Text identisch.                                                                                                                                                                                                                                                                                                                   |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Die **Parent-Eigenschaft** des Statusleistenobjekts ist ein Fenster ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) ), das das Steuerelement umschließt und den gleichen Fensterklassennamen wie das -Steuerelement hat. Die **Parent-Eigenschaft** der Bereiche in der Statusleiste ist das Statusleistenobjekt.                                                                                                                                                                           |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | Die **Role-Eigenschaft** für das Statusleistenobjekt selbst ist [**ROLE SYSTEM \_ \_ STATUSBAR.**](object-roles.md) Der in einer Statusleiste angezeigte Text hat [**ROLE \_ SYSTEM \_ STATICTEXT**](object-roles.md) als **Role-Eigenschaft.**                                                                                                                                                                                                 |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | Die **State-Eigenschaft** ist eine Kombination aus mindestens einem der folgenden [Werte:](object-state-constants.md)STATE [**SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Hinweise

Da Tastenkombinationen für Statusleisten-Steuerelemente oder Textbereiche auf Statusleisten nicht unterstützt werden, wird [**\_ get accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





