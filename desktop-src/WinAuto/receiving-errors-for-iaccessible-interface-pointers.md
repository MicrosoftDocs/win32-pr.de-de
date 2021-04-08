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
# <a name="receiving-errors-for-iaccessible-interface-pointers"></a><span data-ttu-id="61bc1-103">Empfangen von Fehlern für IAccessible-Schnittstellen Zeiger</span><span class="sxs-lookup"><span data-stu-id="61bc1-103">Receiving Errors for IAccessible Interface Pointers</span></span>

<span data-ttu-id="61bc1-104">In diesem Thema werden Situationen beschrieben, in denen Sie möglicherweise einen Fehler für einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger erhalten.</span><span class="sxs-lookup"><span data-stu-id="61bc1-104">This topic describes situations in which you might receive an error for an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span> <span data-ttu-id="61bc1-105">**IAccessible** -Funktionen können Fehler für **IAccessible** -Schnittstellen Zeiger zurückgeben, wenn ein Benutzer eine Anwendung schließt, zu der das Objekt gehört, oder wenn ein Benutzer ein Steuerelement über die Benutzeroberfläche abschließt.</span><span class="sxs-lookup"><span data-stu-id="61bc1-105">**IAccessible** functions can return errors for **IAccessible** interface pointers when a user closes an application that the object belongs to, or if a user dismisses a control through the user interface.</span></span>

## <a name="user-closes-an-application"></a><span data-ttu-id="61bc1-106">Benutzer schließt eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="61bc1-106">User Closes an Application</span></span>

<span data-ttu-id="61bc1-107">Wenn ein Benutzer die Anwendung schließt, die ein Objekt enthält, auf das der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger verweist, wird bei allen zukünftigen Aufrufen dieses Objekts ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="61bc1-107">If a user closes the application that contains an object to which the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer was pointing, then all future calls to that object will return an error code.</span></span> <span data-ttu-id="61bc1-108">Der Fehler, wie z **. \_ b. Co E \_ objnotconnected**, gibt an, dass das Objekt nicht mehr vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="61bc1-108">The error, such as **CO\_E\_OBJNOTCONNECTED**, will indicate that the object does not exist anymore.</span></span> <span data-ttu-id="61bc1-109">Dies gilt für alle **IAccessible** -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="61bc1-109">This applies to all **IAccessible** interface pointers.</span></span>

## <a name="user-dismisses-a-control"></a><span data-ttu-id="61bc1-110">Benutzer lehnt ein Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="61bc1-110">User Dismisses a Control</span></span>

<span data-ttu-id="61bc1-111">Wenn ein Benutzer ein Steuerelement abschließt (z. b. durch Drücken einer Schaltfläche "Push"), können Clients weiterhin [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden und-Eigenschaften für dieses Objekt aufzurufen, da das Objekt nicht freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="61bc1-111">If a user dismisses a control (for example, by pressing a push button), clients can still call [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties on this object because the object has not been released.</span></span> <span data-ttu-id="61bc1-112">Zukünftige Aufrufe empfangen jedoch Fehlermeldungen.</span><span class="sxs-lookup"><span data-stu-id="61bc1-112">However, future calls will receive error messages.</span></span>

<span data-ttu-id="61bc1-113">Diese Situation gilt für die folgenden Funktionen und Methoden:</span><span class="sxs-lookup"><span data-stu-id="61bc1-113">This situation applies to the following functions and methods:</span></span>

-   [<span data-ttu-id="61bc1-114">**Accessibleobjectfromevent**</span><span class="sxs-lookup"><span data-stu-id="61bc1-114">**AccessibleObjectFromEvent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   [<span data-ttu-id="61bc1-115">**Accessibleobjectfrompoint**</span><span class="sxs-lookup"><span data-stu-id="61bc1-115">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [<span data-ttu-id="61bc1-116">**Accessibleobjectfromwindow**</span><span class="sxs-lookup"><span data-stu-id="61bc1-116">**AccessibleObjectFromWindow**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [<span data-ttu-id="61bc1-117">**IAccessible:: accHitTest**</span><span class="sxs-lookup"><span data-stu-id="61bc1-117">**IAccessible::accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="61bc1-118">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="61bc1-118">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="61bc1-119">**IAccessible:: get- \_ Fokus**</span><span class="sxs-lookup"><span data-stu-id="61bc1-119">**IAccessible::get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [<span data-ttu-id="61bc1-120">**IAccessible:: get- \_ accSelection**</span><span class="sxs-lookup"><span data-stu-id="61bc1-120">**IAccessible::get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)

 

 




