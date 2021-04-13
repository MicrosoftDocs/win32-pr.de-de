---
title: Mauseingabe Benachrichtigungen
description: .
ms.assetid: bf010650-4117-4ea5-8563-ca067d48f9cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9b8d7794d2122e89dc558331ac487e54b91e05
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388329"
---
# <a name="mouse-input-notifications"></a><span data-ttu-id="62723-103">Mauseingabe Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="62723-103">Mouse Input Notifications</span></span>

## <a name="in-this-section"></a><span data-ttu-id="62723-104">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="62723-104">In This Section</span></span>

-   [<span data-ttu-id="62723-105">**WM- \_ capturechanged**</span><span class="sxs-lookup"><span data-stu-id="62723-105">**WM\_CAPTURECHANGED**</span></span>](wm-capturechanged.md)
-   [<span data-ttu-id="62723-106">**WM \_ lbuttondblclk**</span><span class="sxs-lookup"><span data-stu-id="62723-106">**WM\_LBUTTONDBLCLK**</span></span>](wm-lbuttondblclk.md)
-   [<span data-ttu-id="62723-107">**WM \_ lbuttondown**</span><span class="sxs-lookup"><span data-stu-id="62723-107">**WM\_LBUTTONDOWN**</span></span>](wm-lbuttondown.md)
-   [<span data-ttu-id="62723-108">**WM- \_ lbuttonup**</span><span class="sxs-lookup"><span data-stu-id="62723-108">**WM\_LBUTTONUP**</span></span>](wm-lbuttonup.md)
-   [<span data-ttu-id="62723-109">**WM- \_ mbuttondblclk**</span><span class="sxs-lookup"><span data-stu-id="62723-109">**WM\_MBUTTONDBLCLK**</span></span>](wm-mbuttondblclk.md)
-   [<span data-ttu-id="62723-110">**WM- \_ mbuttondown**</span><span class="sxs-lookup"><span data-stu-id="62723-110">**WM\_MBUTTONDOWN**</span></span>](wm-mbuttondown.md)
-   [<span data-ttu-id="62723-111">**WM- \_ mbuttonup**</span><span class="sxs-lookup"><span data-stu-id="62723-111">**WM\_MBUTTONUP**</span></span>](wm-mbuttonup.md)
-   [<span data-ttu-id="62723-112">**WM- \_ moueinaktivierung**</span><span class="sxs-lookup"><span data-stu-id="62723-112">**WM\_MOUSEACTIVATE**</span></span>](wm-mouseactivate.md)
-   [<span data-ttu-id="62723-113">**WM- \_ moupagehover**</span><span class="sxs-lookup"><span data-stu-id="62723-113">**WM\_MOUSEHOVER**</span></span>](wm-mousehover.md)
-   [<span data-ttu-id="62723-114">**WM \_ mousehwheel**</span><span class="sxs-lookup"><span data-stu-id="62723-114">**WM\_MOUSEHWHEEL**</span></span>](wm-mousehwheel.md)
-   [<span data-ttu-id="62723-115">**WM- \_ MouseLeave**</span><span class="sxs-lookup"><span data-stu-id="62723-115">**WM\_MOUSELEAVE**</span></span>](wm-mouseleave.md)
-   [<span data-ttu-id="62723-116">**WM- \_ mouseelmove**</span><span class="sxs-lookup"><span data-stu-id="62723-116">**WM\_MOUSEMOVE**</span></span>](wm-mousemove.md)
-   [<span data-ttu-id="62723-117">**WM- \_ Mausrad**</span><span class="sxs-lookup"><span data-stu-id="62723-117">**WM\_MOUSEWHEEL**</span></span>](wm-mousewheel.md)
-   [<span data-ttu-id="62723-118">**WM- \_ nchittest**</span><span class="sxs-lookup"><span data-stu-id="62723-118">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
-   [<span data-ttu-id="62723-119">**WM \_ nclbuttondblclk**</span><span class="sxs-lookup"><span data-stu-id="62723-119">**WM\_NCLBUTTONDBLCLK**</span></span>](wm-nclbuttondblclk.md)
-   [<span data-ttu-id="62723-120">**WM- \_ nclbuttondown**</span><span class="sxs-lookup"><span data-stu-id="62723-120">**WM\_NCLBUTTONDOWN**</span></span>](wm-nclbuttondown.md)
-   [<span data-ttu-id="62723-121">**WM- \_ nclbuttonup**</span><span class="sxs-lookup"><span data-stu-id="62723-121">**WM\_NCLBUTTONUP**</span></span>](wm-nclbuttonup.md)
-   [<span data-ttu-id="62723-122">**WM \_ ncmbuttondblclk**</span><span class="sxs-lookup"><span data-stu-id="62723-122">**WM\_NCMBUTTONDBLCLK**</span></span>](wm-ncmbuttondblclk.md)
-   [<span data-ttu-id="62723-123">**WM \_ ncmbuttondown**</span><span class="sxs-lookup"><span data-stu-id="62723-123">**WM\_NCMBUTTONDOWN**</span></span>](wm-ncmbuttondown.md)
-   [<span data-ttu-id="62723-124">**WM \_ ncmbuttonup**</span><span class="sxs-lookup"><span data-stu-id="62723-124">**WM\_NCMBUTTONUP**</span></span>](wm-ncmbuttonup.md)
-   [<span data-ttu-id="62723-125">**WM \_ ncmoupagehover**</span><span class="sxs-lookup"><span data-stu-id="62723-125">**WM\_NCMOUSEHOVER**</span></span>](wm-ncmousehover.md)
-   [<span data-ttu-id="62723-126">**WM- \_ ncmouseleave**</span><span class="sxs-lookup"><span data-stu-id="62723-126">**WM\_NCMOUSELEAVE**</span></span>](wm-ncmouseleave.md)
-   [<span data-ttu-id="62723-127">**WM- \_ ncmouummove**</span><span class="sxs-lookup"><span data-stu-id="62723-127">**WM\_NCMOUSEMOVE**</span></span>](wm-ncmousemove.md)
-   [<span data-ttu-id="62723-128">**WM \_ ncrbuttondblclk**</span><span class="sxs-lookup"><span data-stu-id="62723-128">**WM\_NCRBUTTONDBLCLK**</span></span>](wm-ncrbuttondblclk.md)
-   [<span data-ttu-id="62723-129">**WM- \_ ncrbuttondown**</span><span class="sxs-lookup"><span data-stu-id="62723-129">**WM\_NCRBUTTONDOWN**</span></span>](wm-ncrbuttondown.md)
-   [<span data-ttu-id="62723-130">**WM- \_ ncrbuttonup**</span><span class="sxs-lookup"><span data-stu-id="62723-130">**WM\_NCRBUTTONUP**</span></span>](wm-ncrbuttonup.md)
-   [<span data-ttu-id="62723-131">**WM \_ ncxbuttondblclk**</span><span class="sxs-lookup"><span data-stu-id="62723-131">**WM\_NCXBUTTONDBLCLK**</span></span>](wm-ncxbuttondblclk.md)
-   [<span data-ttu-id="62723-132">**WM- \_ ncxbuttondown**</span><span class="sxs-lookup"><span data-stu-id="62723-132">**WM\_NCXBUTTONDOWN**</span></span>](wm-ncxbuttondown.md)
-   [<span data-ttu-id="62723-133">**WM- \_ ncxbuttonup**</span><span class="sxs-lookup"><span data-stu-id="62723-133">**WM\_NCXBUTTONUP**</span></span>](wm-ncxbuttonup.md)
-   [<span data-ttu-id="62723-134">**WM- \_ rbuttondblclk**</span><span class="sxs-lookup"><span data-stu-id="62723-134">**WM\_RBUTTONDBLCLK**</span></span>](wm-rbuttondblclk.md)
-   [<span data-ttu-id="62723-135">**WM- \_ rbuttondown**</span><span class="sxs-lookup"><span data-stu-id="62723-135">**WM\_RBUTTONDOWN**</span></span>](wm-rbuttondown.md)
-   [<span data-ttu-id="62723-136">**WM- \_ rbuttonup**</span><span class="sxs-lookup"><span data-stu-id="62723-136">**WM\_RBUTTONUP**</span></span>](wm-rbuttonup.md)
-   [<span data-ttu-id="62723-137">**WM- \_ xbuttondblclk**</span><span class="sxs-lookup"><span data-stu-id="62723-137">**WM\_XBUTTONDBLCLK**</span></span>](wm-xbuttondblclk.md)
-   [<span data-ttu-id="62723-138">**WM- \_ xbuttondown**</span><span class="sxs-lookup"><span data-stu-id="62723-138">**WM\_XBUTTONDOWN**</span></span>](wm-xbuttondown.md)
-   [<span data-ttu-id="62723-139">**WM- \_ xbuttonup**</span><span class="sxs-lookup"><span data-stu-id="62723-139">**WM\_XBUTTONUP**</span></span>](wm-xbuttonup.md)

 

 




