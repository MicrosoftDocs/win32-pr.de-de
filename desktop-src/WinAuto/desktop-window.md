---
title: Desktop Fenster (MSAA UI-Element Referenz)
description: Das Desktop Fenster zeigt die Desktop Listenansicht an (die Symbole wie Arbeitsplatz enthält) und die Taskleiste, die die Schaltfläche Start enthält.
ms.assetid: 3668c26e-6462-4219-95d3-507811ed7f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58208b3993964a367d093174d58d705beda23d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388063"
---
# <a name="desktop-window-msaa-ui-element-reference"></a>Desktop Fenster (MSAA UI-Element Referenz)

Das Desktop Fenster zeigt die Desktop Listenansicht an (die Symbole wie Arbeitsplatz enthält) und die Taskleiste, die die Schaltfläche **Start** enthält.

Dieses Objekt wird nur selten von Clients abgefragt, weil die Listenansicht und die Taskleiste den gesamten Desktop abdecken. Das Desktop Objekt wird abgerufen, wenn Sie sich anmelden, bevor die Betriebssystem-Shell die Listenansicht und die Taskleiste anzeigt. In einigen Fällen wird der Desktop beim Navigieren von anderen Objekten abgerufen.

Der Fenster Klassenname für das Desktop Fenster lautet " \# 32769".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Das Desktop Fenster unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Das Desktop Fenster unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                 | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | Die Name-Eigenschaft ist "Desktop".                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | Die **Role** -Eigenschaft ist [**role \_ System \_ Client**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                |
| [**\_Zugriffs Auswahl**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





