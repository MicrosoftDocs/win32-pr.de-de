---
title: Native IAccessible-Unterstützung
description: Oleacc.dll implementiert iaccidentity im Namen von objID- \_ Client \ 160; IAccessible-Schnittstellen Zeigern und deren unmittelbaren, einfachen untergeordneten Elementen.
ms.assetid: 98c6d68b-b64d-44d4-93c3-6c7c6732d59d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606261a642f57c85f3f23a80257b7cdc498b927b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856428"
---
# <a name="native-iaccessible-support"></a><span data-ttu-id="d41d0-103">Native IAccessible-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="d41d0-103">Native IAccessible Support</span></span>

<span data-ttu-id="d41d0-104">Oleacc.dll implementiert [**iaccidentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) für den [**objID- \_ Client**](object-identifiers.md), der  [**ibarrierefreie**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Schnittstellen Zeiger und seine unmittelbaren einfachen untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="d41d0-104">Oleacc.dll implements [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) on behalf of [**OBJID\_CLIENT**](object-identifiers.md) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers and their immediate simple element children.</span></span> <span data-ttu-id="d41d0-105">Ein **objID- \_ Client**, der  **IAccessible** -Schnittstellen Zeiger ist, wird zurückgegeben, wenn [**WM \_ GetObject**](wm-getobject.md) mit *LPARAM*  =  **objID- \_ Client** an ein **HWND** gesendet wird, das den Client Bereich des Fensters oder das Steuerelement als Ganzes darstellt.</span><span class="sxs-lookup"><span data-stu-id="d41d0-105">An **OBJID\_CLIENT** **IAccessible** interface pointer is returned when [**WM\_GETOBJECT**](wm-getobject.md) with *lParam* = **OBJID\_CLIENT** is sent to an **HWND**, which represents the client area of the window or the control as a whole.</span></span> <span data-ttu-id="d41d0-106">**Das über** geordnete Element eines solchen **IAccessible** -Schnittstellen Zeigers verfügt in der Regel über eine Rolle des [**Rollen \_ System \_ Fensters**](object-roles.md) und ist das Objekt, das zurückgegeben wird, wenn **WM \_ GetObject** mit *LPARAM*  =  [**objID- \_ Fenster**](object-identifiers.md) an ein HWND gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d41d0-106">The parent of such an **IAccessible** interface pointer will typically have a role of [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) and is the **IAccessible** object returned when **WM\_GETOBJECT** with *lParam* = [**OBJID\_WINDOW**](object-identifiers.md) is sent to an hwnd.</span></span>

<span data-ttu-id="d41d0-107">Diese [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger treten in der Regel auf, wenn ein Oleacc.dll Proxy untergeordnet ist oder wenn ein einfaches benutzerdefiniertes  Steuerelement (z. b </span><span class="sxs-lookup"><span data-stu-id="d41d0-107">These [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers typically occur where an Oleacc.dll proxy is subclassed, or where a simple custom control (such as a container **IAccessible** plus one level of simple element children) provides a native **IAccessible** implementation.</span></span>

<span data-ttu-id="d41d0-108">Komplexere systemeigene [**ibarrierefreie**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Implementierungen, wie z. b. das vorhanden sein einer Hierarchie von **IAccessible**-Objekten oder die Verwendung von benutzerdefinierten Objekt-IDs, müssen [**iaccidentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) selbst implementieren</span><span class="sxs-lookup"><span data-stu-id="d41d0-108">More complicated native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementations such as where a hierarchy of **IAccessible** s exists or where custom object IDs are used must implement [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) themselves.</span></span>

 

 




