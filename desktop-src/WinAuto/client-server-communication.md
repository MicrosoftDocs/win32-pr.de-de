---
title: Client/Server-Kommunikation
description: Mit dem WinEvents-Mechanismus können Server problemlos mit Microsoft Active Accessibility-Clients kommunizieren.
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95b29170d5a903493977af130ef6d48bb3b896b6
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "106341910"
---
# <a name="clientserver-communication"></a><span data-ttu-id="82f4d-103">Client/Server-Kommunikation</span><span class="sxs-lookup"><span data-stu-id="82f4d-103">Client/Server Communication</span></span>

<span data-ttu-id="82f4d-104">Mit dem [WinEvents](winevents-overview.md) -Mechanismus können Server problemlos mit Microsoft Active Accessibility-Clients kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="82f4d-104">The [WinEvents](winevents-overview.md) mechanism provides a way for servers to communicate easily with Microsoft Active Accessibility clients.</span></span> <span data-ttu-id="82f4d-105">Clients erfassen häufig Informationen, indem Sie auf WinEvents (z. b. den folgenden Fokus) reagieren, aber Sie können jederzeit jederzeit Informationen von einem Server anfordern.</span><span class="sxs-lookup"><span data-stu-id="82f4d-105">Clients often collect information by reacting to WinEvents (for example, following focus), but they are free to request information from a server at any time.</span></span>

<span data-ttu-id="82f4d-106">Um Informationen für ein Barrierefreies Objekt anzufordern, das ein WinEvent generiert, muss ein Client das Ereignis verarbeiten und eine Verbindung mit dem entsprechenden zugänglichen Objekt herstellen.</span><span class="sxs-lookup"><span data-stu-id="82f4d-106">To request information for an accessible object that generates a WinEvent, a client must process the event and establish a connection with the relevant accessible object.</span></span> <span data-ttu-id="82f4d-107">Zu diesem Zweck führt der Client die folgenden sechs Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="82f4d-107">To do this, the client performs the following six steps:</span></span>

-   <span data-ttu-id="82f4d-108">Ein Server ruft [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) auf, um eine WinEvent-Benachrichtigung für jede Änderung an den Benutzeroberflächen Elementen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="82f4d-108">A server calls [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) to generate a WinEvent notification for each change to its user interface elements.</span></span>
-   <span data-ttu-id="82f4d-109">Der WinEvent Management-Code im Benutzer bestimmt, ob Client Anwendungen eine WinEvent- [*Hook-Funktion*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) mithilfe von [**setwineventhook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) registriert haben und die registrierte Rückruffunktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="82f4d-109">The WinEvent management code in USER determines if any client applications have registered a WinEvent [*hook function*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) using [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) and calls the registered callback function.</span></span>
-   <span data-ttu-id="82f4d-110">In der Rückruffunktion fordert der Client den Zugriff auf das Objekt an, das das Ereignis generiert hat, indem er [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) oder andere barrierefreie Objekt Abruf Funktionen aufruft.</span><span class="sxs-lookup"><span data-stu-id="82f4d-110">In its callback function, the client requests access to the object that generated the event by calling [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) or other accessible object retrieval functions.</span></span> <span data-ttu-id="82f4d-111">Weitere Informationen finden Sie unter [Abrufen eines IAccessible-Objekts](retrieving-an-iaccessible-object.md).</span><span class="sxs-lookup"><span data-stu-id="82f4d-111">For more information, see [Retrieving an IAccessible Object](retrieving-an-iaccessible-object.md).</span></span>
-   <span data-ttu-id="82f4d-112">Diese Microsoft Active Accessibility-API sendet der Serveranwendung eine [**WM- \_ GetObject**](wm-getobject.md) -Nachricht, um das barrierefreie Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="82f4d-112">This Microsoft Active Accessibility API sends the server application a [**WM\_GETOBJECT**](wm-getobject.md) message to retrieve the accessible object.</span></span>
-   <span data-ttu-id="82f4d-113">Als Antwort auf [**WM \_ GetObject**](wm-getobject.md)gibt die Serveranwendung entweder NULL zurück oder gibt einen Wert zurück, der als einmalige Referenz zu dem Objekt fungiert, das das Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="82f4d-113">In response to [**WM\_GETOBJECT**](wm-getobject.md), the server application either returns zero or returns a value that acts as a one-time reference to the object that generated the event.</span></span>
-   <span data-ttu-id="82f4d-114">Wenn der Server NULL zurückgibt, erstellt Microsoft Active Accessibility ein Proxy Objekt und übergibt seine Adresse an den Client.</span><span class="sxs-lookup"><span data-stu-id="82f4d-114">If the server returns zero, Microsoft Active Accessibility creates a proxy object and gives its address to the client.</span></span> <span data-ttu-id="82f4d-115">Andernfalls verwendet Microsoft Active Accessibility diese Referenz, um die Adresse einer Objektschnittstelle (z. b. [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) oder [**IDispatch**](idispatch-interface.md)) abzurufen, und gibt diese Adresse an den Client weiter.</span><span class="sxs-lookup"><span data-stu-id="82f4d-115">Otherwise, Microsoft Active Accessibility uses this reference to retrieve the address of an object interface such as [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) or [**IDispatch**](idispatch-interface.md), and gives that address to the client.</span></span>

<span data-ttu-id="82f4d-116">Wenn der Client über eine Schnittstellen Adresse verfügt, kann er die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften und-Methoden des barrierefreien Objekts aufrufen, um Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="82f4d-116">Once the client has an interface address, it can call the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods of the accessible object to retrieve information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="82f4d-117">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="82f4d-117">In this section</span></span>

-   [<span data-ttu-id="82f4d-118">WinEvents und Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="82f4d-118">WinEvents and Active Accessibility</span></span>](winevents-overview.md)
-   [<span data-ttu-id="82f4d-119">Funktionsweise von WM- \_ GetObject</span><span class="sxs-lookup"><span data-stu-id="82f4d-119">How WM\_GETOBJECT Works</span></span>](how-wm-getobject-works.md)
-   [<span data-ttu-id="82f4d-120">Abrufen eines IAccessible-Objekts</span><span class="sxs-lookup"><span data-stu-id="82f4d-120">Retrieving an IAccessible Object</span></span>](retrieving-an-iaccessible-object.md)

 

 




