---
title: Abrufen eines IAccessible-Objekts
description: Microsoft Active Accessibility bietet Funktionen wie accessibleobjectfromwindow und accessibleobjectfrompoint, mit denen Clients barrierefreie Objekte abrufen können.
ms.assetid: 971cbead-128b-465a-8e77-2a20217f8d0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89237916597f27c7179fce9516df1e0ecf43a6db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309436"
---
# <a name="retrieving-an-iaccessible-object"></a><span data-ttu-id="bfee2-103">Abrufen eines IAccessible-Objekts</span><span class="sxs-lookup"><span data-stu-id="bfee2-103">Retrieving an IAccessible Object</span></span>

<span data-ttu-id="bfee2-104">Microsoft Active Accessibility bietet Funktionen wie [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) und [**accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) , mit denen Clients barrierefreie Objekte abrufen können.</span><span class="sxs-lookup"><span data-stu-id="bfee2-104">Microsoft Active Accessibility provides functions such as [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) and [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) that allow clients to retrieve accessible objects.</span></span> <span data-ttu-id="bfee2-105">Diese Funktionen geben entweder einen [**IDispatch**](idispatch-interface.md) -oder [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger zurück, über den Clients Informationen über das barrierefreie Objekt erhalten.</span><span class="sxs-lookup"><span data-stu-id="bfee2-105">These functions return either an [**IDispatch**](idispatch-interface.md) or [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer through which clients get information about the accessible object.</span></span>

<span data-ttu-id="bfee2-106">Wenn ein Client [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) oder eine der anderen \**accessibleobjectfrom \* \* \* X* -Funktionen aufruft, die eine Schnittstelle zu einem Objekt abrufen, sendet Microsoft Active Accessibility die [**WM- \_ GetObject**](wm-getobject.md) -Fenster Meldung an die entsprechende Fenster Prozedur innerhalb der entsprechenden Anwendung.</span><span class="sxs-lookup"><span data-stu-id="bfee2-106">When a client calls [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) or any of the other \**AccessibleObjectFrom\*\*\*X* functions that retrieve an interface to an object, Microsoft Active Accessibility sends the [**WM\_GETOBJECT**](wm-getobject.md) window message to the applicable window procedure within the appropriate application.</span></span> <span data-ttu-id="bfee2-107">Zum Bereitstellen von Informationen für Clients müssen Server auf die **WM- \_ GetObject** -Nachricht antworten.</span><span class="sxs-lookup"><span data-stu-id="bfee2-107">To provide information to clients, servers must respond to the **WM\_GETOBJECT** message.</span></span>

<span data-ttu-id="bfee2-108">Um bestimmte Informationen über ein UI-Element zu erfassen, müssen Clients zuerst eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle für das Element abrufen.</span><span class="sxs-lookup"><span data-stu-id="bfee2-108">To collect specific information about a UI element, clients must first retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element.</span></span> <span data-ttu-id="bfee2-109">Um das **IAccessible** -Objekt eines Elements abzurufen, können Clients eine der folgenden Funktionen verwenden:</span><span class="sxs-lookup"><span data-stu-id="bfee2-109">To retrieve an element's **IAccessible** object, clients can use one of the following functions:</span></span>

-   [<span data-ttu-id="bfee2-110">**Accessibleobjectfrompoint**</span><span class="sxs-lookup"><span data-stu-id="bfee2-110">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [<span data-ttu-id="bfee2-111">**Accessibleobjectfromwindow**</span><span class="sxs-lookup"><span data-stu-id="bfee2-111">**AccessibleObjectFromWindow**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [<span data-ttu-id="bfee2-112">**Accessibleobjectfromevent**</span><span class="sxs-lookup"><span data-stu-id="bfee2-112">**AccessibleObjectFromEvent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

<span data-ttu-id="bfee2-113">**So rufen Sie einen IAccessible-Schnittstellen Zeiger ab**</span><span class="sxs-lookup"><span data-stu-id="bfee2-113">**To retrieve an IAccessible Interface Pointer**</span></span>

1.  <span data-ttu-id="bfee2-114">Client ruft eine der \**accessibleobjectfrom \* \* \* X* -Funktionen auf.</span><span class="sxs-lookup"><span data-stu-id="bfee2-114">Client calls one of the \**AccessibleObjectFrom\*\*\*X* functions.</span></span>
2.  <span data-ttu-id="bfee2-115">Oleacc.dll sendet eine [**WM- \_ GetObject**](wm-getobject.md) -Nachricht an den Server.</span><span class="sxs-lookup"><span data-stu-id="bfee2-115">Oleacc.dll sends a [**WM\_GETOBJECT**](wm-getobject.md) message to server.</span></span>
3.  <span data-ttu-id="bfee2-116">Der Server bestimmt, welches Benutzeroberflächen Element der Anforderung entspricht.</span><span class="sxs-lookup"><span data-stu-id="bfee2-116">The server determines which UI element corresponds to the request.</span></span>
4.  <span data-ttu-id="bfee2-117">Der Server gibt entweder 0 (null) zurück, um einen Oleacc.dll Proxy anzufordern.</span><span class="sxs-lookup"><span data-stu-id="bfee2-117">The server either returns zero to request an Oleacc.dll proxy,</span></span>

    <span data-ttu-id="bfee2-118">oder</span><span class="sxs-lookup"><span data-stu-id="bfee2-118">Or</span></span>

    <span data-ttu-id="bfee2-119">Gibt ein [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt (Native Implementierung) zurück.</span><span class="sxs-lookup"><span data-stu-id="bfee2-119">Returns an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object (native implementation).</span></span> <span data-ttu-id="bfee2-120">Gehen Sie dazu wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="bfee2-120">To do this, it:</span></span>

    -   <span data-ttu-id="bfee2-121">Erstellt ein [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt für das-Element.</span><span class="sxs-lookup"><span data-stu-id="bfee2-121">Constructs an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for the element.</span></span>
    -   <span data-ttu-id="bfee2-122">Ruft [**lresultfromujekt**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) auf, um den Zeiger des Objekts zu Mars Hallen.</span><span class="sxs-lookup"><span data-stu-id="bfee2-122">Calls [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) to marshal the object's pointer.</span></span>
    -   <span data-ttu-id="bfee2-123">Gibt das LRESULT an Oleacc.dll zurück.</span><span class="sxs-lookup"><span data-stu-id="bfee2-123">Returns the LRESULT to Oleacc.dll.</span></span>

5.  <span data-ttu-id="bfee2-124">Oleacc.dll überprüft den Rückgabewert von [**WM \_ GetObject**](wm-getobject.md).</span><span class="sxs-lookup"><span data-stu-id="bfee2-124">Oleacc.dll examines the return value from [**WM\_GETOBJECT**](wm-getobject.md).</span></span>

    <span data-ttu-id="bfee2-125">Wenn Sie 0 (null) ist, wird Oleacc.dll ein Proxy Objekt erstellt und an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bfee2-125">If it is zero, Oleacc.dll constructs a proxy object and returns it to the client.</span></span>

    <span data-ttu-id="bfee2-126">oder</span><span class="sxs-lookup"><span data-stu-id="bfee2-126">Or</span></span>

    <span data-ttu-id="bfee2-127">Wenn der Wert ungleich NULL ist, wird von Oleacc.dll [**objectfromlresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) aufgerufen, um das Marshalling des systemeigenen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt Zeigers aufzurufen und an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bfee2-127">If it is nonzero, Oleacc.dll calls [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) to unmarshal the native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object pointer and returns it to the client.</span></span>

 

 




