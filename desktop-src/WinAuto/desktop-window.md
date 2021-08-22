---
title: Desktopfenster (REFERENZ ZUM MSAA-UI-Element)
description: Im Desktopfenster werden die Desktoplistenansicht (die Symbole wie Arbeitsplatz enthält) und die Taskleiste angezeigt, die die Schaltfläche "Start".
ms.assetid: 3668c26e-6462-4219-95d3-507811ed7f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a1c096ea759f9df2115a35e79e72fe7257e93b9d9a21d9f596b890644a6a67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994220"
---
# <a name="desktop-window-msaa-ui-element-reference"></a>Desktopfenster (REFERENZ ZUM MSAA-UI-Element)

Im Desktopfenster werden die Desktoplistenansicht (mit Symbolen wie Arbeitsplatz) und die Taskleiste mit der **Schaltfläche Start** angezeigt.

Dieses Objekt wird selten von Clients abgefragt, da die Listenansicht und die Taskleiste den gesamten Desktop abdecken. Das Desktopobjekt wird abgerufen, wenn Sie sich anmelden, bevor die Betriebssystemshell die Listenansicht und Taskleiste anzeigt. In einigen Fällen wird der Desktop beim Navigieren von anderen Objekten aus erhalten.

Der Name der Fensterklasse für das Desktopfenster ist \# "32769".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Das Desktopfenster unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Das Desktopfenster unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                 | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | Die Name-Eigenschaft ist "Desktop".                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ CLIENT.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | Die **State-Eigenschaft** ist eine Kombination aus mindestens einem der folgenden [Werte:](object-state-constants.md)STATE [**SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





