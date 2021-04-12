---
title: Cursor (MSAA UI-Element Referenz)
description: Ein Cursor ist ein kleines Bild, dessen Position auf dem Bildschirm von einem Zeigegerät gesteuert wird, z. b. mit einer Maus, einem Stift oder einem Trackball. Wenn der Benutzer das Zeigegerät bewegt, verschiebt das Windows-Betriebssystem den Cursor.
ms.assetid: ff97d474-7c96-4f89-bc34-2cf320381ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff351040d342adccda8cb03d56d91f9dc429074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309467"
---
# <a name="cursor-msaa-ui-element-reference"></a><span data-ttu-id="fbc88-104">Cursor (MSAA UI-Element Referenz)</span><span class="sxs-lookup"><span data-stu-id="fbc88-104">Cursor (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="fbc88-105">In diesem Thema werden die Cursor für den MSAA-Benutzeroberflächen-Element Verweis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fbc88-105">This topic describes cursors for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="fbc88-106">Die Verwendung von Cursorn in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fbc88-106">How to use cursors in various UI frameworks is not described here.</span></span> <span data-ttu-id="fbc88-107">Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.</span><span class="sxs-lookup"><span data-stu-id="fbc88-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="fbc88-108">Ein Cursor ist ein kleines Bild, dessen Position auf dem Bildschirm von einem Zeigegerät gesteuert wird, z. b. mit einer Maus, einem Stift oder einem Trackball.</span><span class="sxs-lookup"><span data-stu-id="fbc88-108">A cursor is a small picture whose location on the screen is controlled by a pointing device, such as a mouse, pen, or trackball.</span></span> <span data-ttu-id="fbc88-109">Wenn der Benutzer das Zeigegerät bewegt, verschiebt das Windows-Betriebssystem den Cursor.</span><span class="sxs-lookup"><span data-stu-id="fbc88-109">When the user moves the pointing device, the Windows operating system moves the cursor.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="fbc88-110">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="fbc88-110">IAccessible Methods</span></span>

<span data-ttu-id="fbc88-111">Ein Cursor unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="fbc88-111">A cursor supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="fbc88-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="fbc88-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="fbc88-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="fbc88-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a><span data-ttu-id="fbc88-114">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fbc88-114">IAccessible Properties</span></span>

<span data-ttu-id="fbc88-115">Ein Cursor unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fbc88-115">A cursor supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   <span data-ttu-id="fbc88-116">[**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)– die **childCount** -Eigenschaft ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fbc88-116">[**get\_accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)—The **ChildCount** property is zero.</span></span>
-   <span data-ttu-id="fbc88-117">[**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)– Entwickler können benutzerdefinierte Cursor erstellen oder die vordefinierten Cursor verwenden, die mit ihrer Cursor-ID identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="fbc88-117">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—Developers can create custom cursors or use the predefined cursors that are identified by their cursor ID.</span></span> <span data-ttu-id="fbc88-118">Die **Name** -Eigenschaft des Cursors hängt von ihrer Form ab und ist einer der folgenden:</span><span class="sxs-lookup"><span data-stu-id="fbc88-118">The **Name** property of the cursor depends on its shape and is one of the following:</span></span> 

    | <span data-ttu-id="fbc88-119">Cursorform</span><span class="sxs-lookup"><span data-stu-id="fbc88-119">Cursor shape</span></span>     | <span data-ttu-id="fbc88-120">Name</span><span class="sxs-lookup"><span data-stu-id="fbc88-120">Name</span></span>              |
    |------------------|-------------------|
    | <span data-ttu-id="fbc88-121">Benutzerdefinierter Cursor</span><span class="sxs-lookup"><span data-stu-id="fbc88-121">Custom cursor</span></span>    | <span data-ttu-id="fbc88-122">Unbekannter</span><span class="sxs-lookup"><span data-stu-id="fbc88-122">"Unknown"</span></span>         |
    | <span data-ttu-id="fbc88-123">IDC- \_ Pfeil</span><span class="sxs-lookup"><span data-stu-id="fbc88-123">IDC\_ARROW</span></span>       | <span data-ttu-id="fbc88-124">"Normal"</span><span class="sxs-lookup"><span data-stu-id="fbc88-124">"Normal"</span></span>          |
    | <span data-ttu-id="fbc88-125">IDC- \_ IBeam</span><span class="sxs-lookup"><span data-stu-id="fbc88-125">IDC\_IBEAM</span></span>       | <span data-ttu-id="fbc88-126">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="fbc88-126">"Edit"</span></span>            |
    | <span data-ttu-id="fbc88-127">IDC- \_ Wartezeit</span><span class="sxs-lookup"><span data-stu-id="fbc88-127">IDC\_WAIT</span></span>        | <span data-ttu-id="fbc88-128">Warten</span><span class="sxs-lookup"><span data-stu-id="fbc88-128">"Wait"</span></span>            |
    | <span data-ttu-id="fbc88-129">IDC- \_ Kreuz</span><span class="sxs-lookup"><span data-stu-id="fbc88-129">IDC\_CROSS</span></span>       | <span data-ttu-id="fbc88-130">Biografischen</span><span class="sxs-lookup"><span data-stu-id="fbc88-130">"Graphic"</span></span>         |
    | <span data-ttu-id="fbc88-131">IDC- \_ upartrow</span><span class="sxs-lookup"><span data-stu-id="fbc88-131">IDC\_UPARROW</span></span>     | <span data-ttu-id="fbc88-132">Gegründet</span><span class="sxs-lookup"><span data-stu-id="fbc88-132">"Up"</span></span>              |
    | <span data-ttu-id="fbc88-133">IDC \_ sizenwse</span><span class="sxs-lookup"><span data-stu-id="fbc88-133">IDC\_SIZENWSE</span></span>    | <span data-ttu-id="fbc88-134">"NWSE size"</span><span class="sxs-lookup"><span data-stu-id="fbc88-134">"NWSE size"</span></span>       |
    | <span data-ttu-id="fbc88-135">IDC \_ sizenesw</span><span class="sxs-lookup"><span data-stu-id="fbc88-135">IDC\_SIZENESW</span></span>    | <span data-ttu-id="fbc88-136">"Größe der Größe"</span><span class="sxs-lookup"><span data-stu-id="fbc88-136">"NESW size"</span></span>       |
    | <span data-ttu-id="fbc88-137">IDC \_ SizeWE</span><span class="sxs-lookup"><span data-stu-id="fbc88-137">IDC\_SIZEWE</span></span>      | <span data-ttu-id="fbc88-138">"Horizontale Größe"</span><span class="sxs-lookup"><span data-stu-id="fbc88-138">"Horizontal size"</span></span> |
    | <span data-ttu-id="fbc88-139">IDC- \_ SizeNS</span><span class="sxs-lookup"><span data-stu-id="fbc88-139">IDC\_SIZENS</span></span>      | <span data-ttu-id="fbc88-140">"Vertikale Größe"</span><span class="sxs-lookup"><span data-stu-id="fbc88-140">"Vertical size"</span></span>   |
    | <span data-ttu-id="fbc88-141">IDC \_ SizeAll</span><span class="sxs-lookup"><span data-stu-id="fbc88-141">IDC\_SIZEALL</span></span>     | <span data-ttu-id="fbc88-142">Voranschreiten</span><span class="sxs-lookup"><span data-stu-id="fbc88-142">"Move"</span></span>            |
    | <span data-ttu-id="fbc88-143">IDC- \_ Nr.</span><span class="sxs-lookup"><span data-stu-id="fbc88-143">IDC\_NO</span></span>          | <span data-ttu-id="fbc88-144">Tener</span><span class="sxs-lookup"><span data-stu-id="fbc88-144">"Forbidden"</span></span>       |
    | <span data-ttu-id="fbc88-145">IDC- \_ AppStarting</span><span class="sxs-lookup"><span data-stu-id="fbc88-145">IDC\_APPSTARTING</span></span> | <span data-ttu-id="fbc88-146">"App-Start"</span><span class="sxs-lookup"><span data-stu-id="fbc88-146">"App start"</span></span>       |
    | <span data-ttu-id="fbc88-147">IDC- \_ Hilfe</span><span class="sxs-lookup"><span data-stu-id="fbc88-147">IDC\_HELP</span></span>        | <span data-ttu-id="fbc88-148">Hilft</span><span class="sxs-lookup"><span data-stu-id="fbc88-148">"Help"</span></span>            |

    

     

-   <span data-ttu-id="fbc88-149">[**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)– die **Role** -Eigenschaft ist ein [**Rollen System- \_ \_ Cursor**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fbc88-149">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property is [**ROLE\_SYSTEM\_CURSOR**](object-roles.md).</span></span>
-   <span data-ttu-id="fbc88-150">[**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)– die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md):</span><span class="sxs-lookup"><span data-stu-id="fbc88-150">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—The **State** property is a combination of one or more of the following [values](object-state-constants.md):</span></span>

    <span data-ttu-id="fbc88-151">[**Status \_ System \_ unsichtbar**](object-state-constants.md) - \| [ **Zustands \_ System \_** ist nicht verankert](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="fbc88-151">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FLOATING**](object-state-constants.md)</span></span>

## <a name="notes"></a><span data-ttu-id="fbc88-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="fbc88-152">Notes</span></span>

-   <span data-ttu-id="fbc88-153">Anders als andere Elemente der Benutzeroberfläche verfügt das Cursor Objekt nicht über ein zugeordnetes Fenster handle.</span><span class="sxs-lookup"><span data-stu-id="fbc88-153">Unlike other UI elements, the cursor object does not have an associated window handle.</span></span> <span data-ttu-id="fbc88-154">Um Zugriff auf das Cursor Objekt zu erhalten, müssen Clients ein [*wineventproc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) festlegen und darauf warten, dass das Cursor Objekt Ereignisse generiert.</span><span class="sxs-lookup"><span data-stu-id="fbc88-154">To obtain access to the cursor object, clients must set a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) and wait for the cursor object to generate events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbc88-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fbc88-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbc88-156">IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="fbc88-156">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




