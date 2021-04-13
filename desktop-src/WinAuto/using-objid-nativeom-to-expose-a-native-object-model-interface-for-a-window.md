---
title: Verwenden Sie objID \_ nativeom, um eine native Schnittstelle für ein Fenster verfügbar zu machen.
description: Diese Technik ermöglicht es Clients, ein benutzerdefiniertes-Objekt für ein Fenster zu erhalten. -Server können diese verwenden, um einen Zeiger auf ein benutzerdefiniertes Dokument Objekt für ein Fenster verfügbar zu machen.
ms.assetid: 91713fe5-f03f-464e-88ee-9d8d66d5b19d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2c5c6ec194ca643475444feb5839c02d3fa890
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "104389469"
---
# <a name="use-objid_nativeom-to-expose-a-native-interface-for-a-window"></a><span data-ttu-id="54c01-104">Verwenden Sie objID \_ nativeom, um eine native Schnittstelle für ein Fenster verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="54c01-104">Use OBJID\_NATIVEOM to expose a native interface for a window</span></span>

<span data-ttu-id="54c01-105">Diese Technik ermöglicht es Clients, ein benutzerdefiniertes-Objekt für ein Fenster zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="54c01-105">This technique allows clients to get a custom object for a window.</span></span> <span data-ttu-id="54c01-106">-Server können diese verwenden, um einen Zeiger auf ein benutzerdefiniertes Dokument Objekt für ein Fenster verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="54c01-106">Servers can use this to expose a pointer to a custom document object for a window.</span></span>

<span data-ttu-id="54c01-107">**So machen Sie eine systemeigene Objektmodell Schnittstelle für ein Fenster (Server) verfügbar**</span><span class="sxs-lookup"><span data-stu-id="54c01-107">**To expose a native object model interface for a window (servers)**</span></span>

1.  <span data-ttu-id="54c01-108">Behandelt die [**WM- \_ GetObject**](wm-getobject.md) -Nachricht in der Fenster Prozedur.</span><span class="sxs-lookup"><span data-stu-id="54c01-108">Handle the [**WM\_GETOBJECT**](wm-getobject.md) message in the window procedure.</span></span> <span data-ttu-id="54c01-109">Wenn der *LPARAM* -Wert " [**objID \_ nativeom**](object-identifiers.md)" ist, geben Sie einen Schnittstellen Zeiger auf das benutzerdefinierte Objekt mithilfe von " [**lresultfrofubject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)" zurück.</span><span class="sxs-lookup"><span data-stu-id="54c01-109">When the *lParam* value is [**OBJID\_NATIVEOM**](object-identifiers.md), return an interface pointer to the custom object using [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span></span>
2.  <span data-ttu-id="54c01-110">Geben Sie ggf. den Schnittstellen Zeiger nach dem Aufrufen von [**lresultfrobobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)frei.</span><span class="sxs-lookup"><span data-stu-id="54c01-110">Release your interface pointer after calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), if appropriate.</span></span> <span data-ttu-id="54c01-111">Weitere Informationen finden Sie unter **lresultfrobugbject**.</span><span class="sxs-lookup"><span data-stu-id="54c01-111">For more information, see **LresultFromObject**.</span></span>

<span data-ttu-id="54c01-112">Clients können einen Zeiger auf dieses benutzerdefinierte Objekt abrufen.</span><span class="sxs-lookup"><span data-stu-id="54c01-112">Clients can obtain a pointer to this custom object.</span></span>

<span data-ttu-id="54c01-113">**So rufen Sie einen Zeiger für ein benutzerdefiniertes Objekt für ein Fenster (Clients) ab**</span><span class="sxs-lookup"><span data-stu-id="54c01-113">**To obtain a pointer for a custom object for a window (clients)**</span></span>

-   <span data-ttu-id="54c01-114">Aufrufen von [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) und übergeben von [**objID \_ nativeom**](object-identifiers.md) als zweiten Parameter.</span><span class="sxs-lookup"><span data-stu-id="54c01-114">Call [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) and pass [**OBJID\_NATIVEOM**](object-identifiers.md) as the second parameter.</span></span>

<span data-ttu-id="54c01-115">Beachten Sie die folgenden Probleme bei dieser Technik:</span><span class="sxs-lookup"><span data-stu-id="54c01-115">Note the following issues for this technique:</span></span>

-   <span data-ttu-id="54c01-116">Diese Vorgehensweise ähnelt der Rückgabe eines [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeigers, außer der verwendeten Objekt-ID und der Tatsache, dass [**lresultfrobobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) anstelle von **IAccessible** ein benutzerdefiniertes Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="54c01-116">This technique is similar to returning an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer except for the object ID used and the fact that [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) returns a custom object instead of **IAccessible**.</span></span>
-   <span data-ttu-id="54c01-117">Server Entwickler müssen möglicherweise Informationen veröffentlichen, die es Clients ermöglichen, das **HWND** eindeutig zu identifizieren, damit Sie es finden, bevor Sie [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) auf dem zugehörigen Fenster Handle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="54c01-117">Server developers may need to publish information that allows clients to uniquely identify the **HWND** so that they can find it before calling [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) on its window handle.</span></span>
-   <span data-ttu-id="54c01-118">Implementieren Sie die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle nicht für das benutzerdefinierte Objekt, das zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="54c01-118">Do not implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the custom object that is returned.</span></span> <span data-ttu-id="54c01-119">Wenn Sie dies tun, behandelt oleacc es als Standard- **IAccessible** und kann verhindern, dass die benutzerdefinierten Schnittstellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54c01-119">If you do, OLEACC will treat it is as a standard **IAccessible** and may prevent the custom interfaces from being used.</span></span>
-   <span data-ttu-id="54c01-120">Um Prozess übergreifend verwendet zu werden, müssen die Schnittstellen des zurückgegebenen Objekts möglicherweise bei Component Object Model (com) registriert werden.</span><span class="sxs-lookup"><span data-stu-id="54c01-120">In order to be used across processes, the interfaces on the returned object may need to be registered with Component Object Model (COM).</span></span>

<span data-ttu-id="54c01-121">Diese Technik wird von mehreren Microsoft Office Komponenten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="54c01-121">This technique is supported by several Microsoft Office components.</span></span> <span data-ttu-id="54c01-122">Weitere Informationen finden Sie unter [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span><span class="sxs-lookup"><span data-stu-id="54c01-122">For more information, see [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span>

 

 




