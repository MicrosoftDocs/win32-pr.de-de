---
title: Empfangen von Fehlern für IAccessible-Schnittstellenzeker
description: In diesem Thema werden Situationen beschrieben, in denen sie möglicherweise einen Fehler für einen IAccessible-Schnittstellenzeiger erhalten.
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d36a29c688966526d5431e1fe2f643e39b378779d122d22f38dea2089a5191c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115141"
---
# <a name="receiving-errors-for-iaccessible-interface-pointers"></a>Empfangen von Fehlern für IAccessible-Schnittstellenzeker

In diesem Thema werden Situationen beschrieben, in [](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) denen sie möglicherweise einen Fehler für einen IAccessible-Schnittstellenzeiger erhalten. **IAccessible-Funktionen** können Fehler für **IAccessible-Schnittstellenzeker** zurückgeben, wenn ein Benutzer eine Anwendung schließt, zu der das Objekt gehört, oder wenn ein Benutzer ein Steuerelement über die Benutzeroberfläche verlässt.

## <a name="user-closes-an-application"></a>Benutzer schließt eine Anwendung

Wenn ein Benutzer die Anwendung schließt, die [](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ein Objekt enthält, auf das der IAccessible-Schnittstellenzeiger gezeigert hat, geben alle zukünftigen Aufrufe dieses Objekts einen Fehlercode zurück. Der Fehler, z. **B. CO \_ E \_ OBJNOTCONNECTED,** gibt an, dass das Objekt nicht mehr vorhanden ist. Dies gilt für alle **IAccessible-Schnittstellenzeker.**

## <a name="user-dismisses-a-control"></a>Benutzer verlässt ein Steuerelement

Wenn ein Benutzer ein Steuerelement verlässt (z. B. durch Drücken einer Pushschaltfläche), können Clients weiterhin [**IAccessible-Methoden**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und -Eigenschaften für dieses Objekt aufrufen, da das Objekt nicht freigegeben wurde. Zukünftige Aufrufe erhalten jedoch Fehlermeldungen.

Dies gilt für die folgenden Funktionen und Methoden:

-   [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**IAccessible::get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**IAccessible::get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)

 

 




