---
title: Behandeln von WM_GETOBJECT
description: Wenn eine WM- \_ GetObject-Nachricht empfangen wird, die den objID- \_ Client enthält, muss der Server einen Zeiger auf das Objekt zurückgeben, das IAccessible implementiert.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6223d75339f537ccf1939f9c9af46a42aa47bfdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711717"
---
# <a name="how-to-handle-wm_getobject"></a><span data-ttu-id="24a00-103">Behandeln von WM- \_ GetObject</span><span class="sxs-lookup"><span data-stu-id="24a00-103">How to Handle WM\_GETOBJECT</span></span>

<span data-ttu-id="24a00-104">Wenn eine WM- [**\_ GetObject**](wm-getobject.md) -Nachricht empfangen wird, die den [**objID- \_ Client**](object-identifiers.md)enthält, muss der Server einen Zeiger auf das Objekt zurückgeben, das [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)implementiert.</span><span class="sxs-lookup"><span data-stu-id="24a00-104">When it receives a [**WM\_GETOBJECT**](wm-getobject.md) message that contains [**OBJID\_CLIENT**](object-identifiers.md), the server must return a pointer to the object that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="24a00-105">Dieser Zeiger ist ein LRESULT, das durch den Aufruf von [**lresultfro"bject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)" abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="24a00-105">This pointer is an LRESULT that is obtained by calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span></span> <span data-ttu-id="24a00-106">Microsoft Active Accessibility führt in Verbindung mit der Component Object Model (com)-Bibliothek das entsprechende Marshalling durch und übergibt den **IAccessible** -Schnittstellen Zeiger vom Server an den Client.</span><span class="sxs-lookup"><span data-stu-id="24a00-106">Microsoft Active Accessibility, in conjunction with the Component Object Model (COM) library, performs the appropriate marshaling and passes the **IAccessible** interface pointer from the server to the client.</span></span>

<span data-ttu-id="24a00-107">Server müssen die Verweis Zählung für das barrierefreie Objekt ordnungsgemäß behandeln.</span><span class="sxs-lookup"><span data-stu-id="24a00-107">Servers must correctly handle reference counting on the accessible object.</span></span> <span data-ttu-id="24a00-108">Beachten Sie, dass beim Erstellen eines COM-Objekts der Verweis Zähler 1 ist.</span><span class="sxs-lookup"><span data-stu-id="24a00-108">Remember that when you create a COM object, the reference count is 1.</span></span> <span data-ttu-id="24a00-109">[**Lresultfromuject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) erhöht den Verweis Zähler dann mehrmals.</span><span class="sxs-lookup"><span data-stu-id="24a00-109">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) then further increments the reference count several times.</span></span> <span data-ttu-id="24a00-110">Alle von **lresultfropbject** erstellten Verweise werden automatisch freigegeben, wenn das Objekt nicht mehr benötigt wird. der Server ist jedoch für die Freigabe des ersten Verweises verantwortlich. sofern dies nicht der Fall ist, wird das Objekt nie zerstört.</span><span class="sxs-lookup"><span data-stu-id="24a00-110">All the references created by **LresultFromObject** are automatically released when the object is no longer needed, but the server is responsible for releasing the initial reference, and unless it does so, the object will never be destroyed.</span></span> <span data-ttu-id="24a00-111">In den Beispielen in den folgenden Abschnitten wird gezeigt, wie Verweise auf barrierefreie Objekte freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="24a00-111">The examples in the following sections show how to release references to accessible objects.</span></span>

<span data-ttu-id="24a00-112">Server behandeln die [**WM- \_ GetObject**](wm-getobject.md) -Server in der Regel mit einer der folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="24a00-112">Servers typically handle [**WM\_GETOBJECT**](wm-getobject.md) in one of the following ways:</span></span>

-   [<span data-ttu-id="24a00-113">Neue barrierefreie Objekte erstellen</span><span class="sxs-lookup"><span data-stu-id="24a00-113">Create New Accessible Objects</span></span>](create-new-accessible-objects.md)
-   [<span data-ttu-id="24a00-114">Wieder verwenden vorhandener Zeiger auf Objekte</span><span class="sxs-lookup"><span data-stu-id="24a00-114">Reuse Existing Pointers to Objects</span></span>](reuse-existing-pointers-to-objects.md)
-   [<span data-ttu-id="24a00-115">Erstellen neuer Schnittstellen für dasselbe Objekt</span><span class="sxs-lookup"><span data-stu-id="24a00-115">Create New Interfaces to the Same Object</span></span>](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> <span data-ttu-id="24a00-116">Wenn in diesem Abschnitt in der restlichen Dokumentation ein Zeiger auf eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle erläutert wird, ist dieser Zeiger möglicherweise ein Zeiger auf ein Proxy Objekt, das die **IAccessible** -Schnittstelle umschließt.</span><span class="sxs-lookup"><span data-stu-id="24a00-116">In this section as in the rest of the documentation, when a pointer to an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is discussed, this pointer may actually be a pointer to a proxy object that wraps the **IAccessible** interface.</span></span> <span data-ttu-id="24a00-117">Weitere Informationen zu Proxy Objekten finden Sie unter [Erstellen von Proxy Objekten](creating-proxy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="24a00-117">For more information about proxy objects, see [Creating Proxy Objects](creating-proxy-objects.md).</span></span>

 

<span data-ttu-id="24a00-118">Eine Übersicht über [**WM \_ GetObject**](wm-getobject.md)finden Sie unter [Funktionsweise von "WM \_ GetObject](how-wm-getobject-works.md)".</span><span class="sxs-lookup"><span data-stu-id="24a00-118">For an overview of [**WM\_GETOBJECT**](wm-getobject.md), see [How WM\_GETOBJECT Works](how-wm-getobject-works.md).</span></span>

 

 




