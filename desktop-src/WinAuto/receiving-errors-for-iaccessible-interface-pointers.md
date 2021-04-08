---
title: Empfangen von Fehlern für IAccessible-Schnittstellen Zeiger
description: In diesem Thema werden Situationen beschrieben, in denen Sie möglicherweise einen Fehler für einen IAccessible-Schnittstellen Zeiger erhalten.
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d3bd9e39dae9c5de9ad1644e5955bd5fb90d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856547"
---
# <a name="receiving-errors-for-iaccessible-interface-pointers"></a>Empfangen von Fehlern für IAccessible-Schnittstellen Zeiger

In diesem Thema werden Situationen beschrieben, in denen Sie möglicherweise einen Fehler für einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger erhalten. **IAccessible** -Funktionen können Fehler für **IAccessible** -Schnittstellen Zeiger zurückgeben, wenn ein Benutzer eine Anwendung schließt, zu der das Objekt gehört, oder wenn ein Benutzer ein Steuerelement über die Benutzeroberfläche abschließt.

## <a name="user-closes-an-application"></a>Benutzer schließt eine Anwendung.

Wenn ein Benutzer die Anwendung schließt, die ein Objekt enthält, auf das der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger verweist, wird bei allen zukünftigen Aufrufen dieses Objekts ein Fehlercode zurückgegeben. Der Fehler, wie z **. \_ b. Co E \_ objnotconnected**, gibt an, dass das Objekt nicht mehr vorhanden ist. Dies gilt für alle **IAccessible** -Schnittstellen Zeiger.

## <a name="user-dismisses-a-control"></a>Benutzer lehnt ein Steuerelement ab.

Wenn ein Benutzer ein Steuerelement abschließt (z. b. durch Drücken einer Schaltfläche "Push"), können Clients weiterhin [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden und-Eigenschaften für dieses Objekt aufzurufen, da das Objekt nicht freigegeben wurde. Zukünftige Aufrufe empfangen jedoch Fehlermeldungen.

Diese Situation gilt für die folgenden Funktionen und Methoden:

-   [**Accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   [**Accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**Accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**IAccessible:: get- \_ Fokus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**IAccessible:: get- \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)

 

 




