---
title: Bearbeiten von Steuerelement Meldungen
description: Bearbeiten von Steuerelement Meldungen
ms.assetid: b5c12b71-b7c3-4331-a656-15718121ddf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d57fcf4077b74217140b201cf3ac95bfc620912
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869867"
---
# <a name="edit-control-messages"></a><span data-ttu-id="37c5d-103">Bearbeiten von Steuerelement Meldungen</span><span class="sxs-lookup"><span data-stu-id="37c5d-103">Edit Control Messages</span></span>

## <a name="in-this-section"></a><span data-ttu-id="37c5d-104">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="37c5d-104">In this section</span></span>

-   [<span data-ttu-id="37c5d-105">**EM \_ CanUndo**</span><span class="sxs-lookup"><span data-stu-id="37c5d-105">**EM\_CANUNDO**</span></span>](em-canundo.md)
-   [<span data-ttu-id="37c5d-106">**EM \_ charfrompos**</span><span class="sxs-lookup"><span data-stu-id="37c5d-106">**EM\_CHARFROMPOS**</span></span>](em-charfrompos.md)
-   [<span data-ttu-id="37c5d-107">**EM \_ emptyundobuffer**</span><span class="sxs-lookup"><span data-stu-id="37c5d-107">**EM\_EMPTYUNDOBUFFER**</span></span>](em-emptyundobuffer.md)
-   [<span data-ttu-id="37c5d-108">**EM- \_ Zeilen Trennlinien**</span><span class="sxs-lookup"><span data-stu-id="37c5d-108">**EM\_FMTLINES**</span></span>](em-fmtlines.md)
-   [<span data-ttu-id="37c5d-109">**EM \_ getcuebanner**</span><span class="sxs-lookup"><span data-stu-id="37c5d-109">**EM\_GETCUEBANNER**</span></span>](em-getcuebanner.md)
-   [<span data-ttu-id="37c5d-110">**EM \_ getfirstvisibleline**</span><span class="sxs-lookup"><span data-stu-id="37c5d-110">**EM\_GETFIRSTVISIBLELINE**</span></span>](em-getfirstvisibleline.md)
-   [<span data-ttu-id="37c5d-111">**EM \_ GetHandle**</span><span class="sxs-lookup"><span data-stu-id="37c5d-111">**EM\_GETHANDLE**</span></span>](em-gethandle.md)
-   [<span data-ttu-id="37c5d-112">**\_gethilite EM**</span><span class="sxs-lookup"><span data-stu-id="37c5d-112">**EM\_GETHILITE**</span></span>](em-gethilite.md)
-   [<span data-ttu-id="37c5d-113">**EM \_ getimestatus**</span><span class="sxs-lookup"><span data-stu-id="37c5d-113">**EM\_GETIMESTATUS**</span></span>](em-getimestatus.md)
-   [<span data-ttu-id="37c5d-114">**EM \_ getlimittext**</span><span class="sxs-lookup"><span data-stu-id="37c5d-114">**EM\_GETLIMITTEXT**</span></span>](em-getlimittext.md)
-   [<span data-ttu-id="37c5d-115">**EM \_ getline**</span><span class="sxs-lookup"><span data-stu-id="37c5d-115">**EM\_GETLINE**</span></span>](em-getline.md)
-   [<span data-ttu-id="37c5d-116">**EM \_ getLineCount**</span><span class="sxs-lookup"><span data-stu-id="37c5d-116">**EM\_GETLINECOUNT**</span></span>](em-getlinecount.md)
-   [<span data-ttu-id="37c5d-117">**EM- \_ getMargin**</span><span class="sxs-lookup"><span data-stu-id="37c5d-117">**EM\_GETMARGINS**</span></span>](em-getmargins.md)
-   [<span data-ttu-id="37c5d-118">**EM \_ getmodify**</span><span class="sxs-lookup"><span data-stu-id="37c5d-118">**EM\_GETMODIFY**</span></span>](em-getmodify.md)
-   [<span data-ttu-id="37c5d-119">**EM \_ getpasswordchar**</span><span class="sxs-lookup"><span data-stu-id="37c5d-119">**EM\_GETPASSWORDCHAR**</span></span>](em-getpasswordchar.md)
-   [<span data-ttu-id="37c5d-120">**EM \_ GetRect**</span><span class="sxs-lookup"><span data-stu-id="37c5d-120">**EM\_GETRECT**</span></span>](em-getrect.md)
-   [<span data-ttu-id="37c5d-121">**EM- \_ GetSEL**</span><span class="sxs-lookup"><span data-stu-id="37c5d-121">**EM\_GETSEL**</span></span>](em-getsel.md)
-   [<span data-ttu-id="37c5d-122">**EM \_ getthumb**</span><span class="sxs-lookup"><span data-stu-id="37c5d-122">**EM\_GETTHUMB**</span></span>](em-getthumb.md)
-   [<span data-ttu-id="37c5d-123">**EM \_ getwordbreakproc**</span><span class="sxs-lookup"><span data-stu-id="37c5d-123">**EM\_GETWORDBREAKPROC**</span></span>](em-getwordbreakproc.md)
-   [<span data-ttu-id="37c5d-124">**EM \_ hideballontip**</span><span class="sxs-lookup"><span data-stu-id="37c5d-124">**EM\_HIDEBALLOONTIP**</span></span>](em-hideballoontip.md)
-   [<span data-ttu-id="37c5d-125">**EM- \_ limittext**</span><span class="sxs-lookup"><span data-stu-id="37c5d-125">**EM\_LIMITTEXT**</span></span>](em-limittext.md)
-   [<span data-ttu-id="37c5d-126">**EM \_ linefromchar**</span><span class="sxs-lookup"><span data-stu-id="37c5d-126">**EM\_LINEFROMCHAR**</span></span>](em-linefromchar.md)
-   [<span data-ttu-id="37c5d-127">**EM \_ Linan DEX**</span><span class="sxs-lookup"><span data-stu-id="37c5d-127">**EM\_LINEINDEX**</span></span>](em-lineindex.md)
-   [<span data-ttu-id="37c5d-128">**EM- \_ LineLength**</span><span class="sxs-lookup"><span data-stu-id="37c5d-128">**EM\_LINELENGTH**</span></span>](em-linelength.md)
-   [<span data-ttu-id="37c5d-129">**EM- \_ linescroll**</span><span class="sxs-lookup"><span data-stu-id="37c5d-129">**EM\_LINESCROLL**</span></span>](em-linescroll.md)
-   [<span data-ttu-id="37c5d-130">**EM \_ nosetfocus**</span><span class="sxs-lookup"><span data-stu-id="37c5d-130">**EM\_NOSETFOCUS**</span></span>](em-nosetfocus.md)
-   [<span data-ttu-id="37c5d-131">**EM \_ posfromchar**</span><span class="sxs-lookup"><span data-stu-id="37c5d-131">**EM\_POSFROMCHAR**</span></span>](em-posfromchar.md)
-   [<span data-ttu-id="37c5d-132">**EM \_ replacesel**</span><span class="sxs-lookup"><span data-stu-id="37c5d-132">**EM\_REPLACESEL**</span></span>](em-replacesel.md)
-   [<span data-ttu-id="37c5d-133">**EM- \_ Scroll**</span><span class="sxs-lookup"><span data-stu-id="37c5d-133">**EM\_SCROLL**</span></span>](em-scroll.md)
-   [<span data-ttu-id="37c5d-134">**EM \_ scrollcaret**</span><span class="sxs-lookup"><span data-stu-id="37c5d-134">**EM\_SCROLLCARET**</span></span>](em-scrollcaret.md)
-   [<span data-ttu-id="37c5d-135">**EM \_ setcuebanner**</span><span class="sxs-lookup"><span data-stu-id="37c5d-135">**EM\_SETCUEBANNER**</span></span>](em-setcuebanner.md)
-   [<span data-ttu-id="37c5d-136">**EM- \_ andle**</span><span class="sxs-lookup"><span data-stu-id="37c5d-136">**EM\_SETHANDLE**</span></span>](em-sethandle.md)
-   [<span data-ttu-id="37c5d-137">**EM \_ -Server**</span><span class="sxs-lookup"><span data-stu-id="37c5d-137">**EM\_SETHILITE**</span></span>](em-sethilite.md)
-   [<span data-ttu-id="37c5d-138">**EM- \_ Zeit Status**</span><span class="sxs-lookup"><span data-stu-id="37c5d-138">**EM\_SETIMESTATUS**</span></span>](em-setimestatus.md)
-   [<span data-ttu-id="37c5d-139">**EM \_ SetLimitText**</span><span class="sxs-lookup"><span data-stu-id="37c5d-139">**EM\_SETLIMITTEXT**</span></span>](em-setlimittext.md)
-   [<span data-ttu-id="37c5d-140">**EM- \_ setMargin**</span><span class="sxs-lookup"><span data-stu-id="37c5d-140">**EM\_SETMARGINS**</span></span>](em-setmargins.md)
-   [<span data-ttu-id="37c5d-141">**EM \_ setmodify**</span><span class="sxs-lookup"><span data-stu-id="37c5d-141">**EM\_SETMODIFY**</span></span>](em-setmodify.md)
-   [<span data-ttu-id="37c5d-142">**EM \_ setpasswordchar**</span><span class="sxs-lookup"><span data-stu-id="37c5d-142">**EM\_SETPASSWORDCHAR**</span></span>](em-setpasswordchar.md)
-   [<span data-ttu-id="37c5d-143">**EM- \_ treadonly**</span><span class="sxs-lookup"><span data-stu-id="37c5d-143">**EM\_SETREADONLY**</span></span>](em-setreadonly.md)
-   [<span data-ttu-id="37c5d-144">**EM \_ SetRect**</span><span class="sxs-lookup"><span data-stu-id="37c5d-144">**EM\_SETRECT**</span></span>](em-setrect.md)
-   [<span data-ttu-id="37c5d-145">**EM \_ setrectnp**</span><span class="sxs-lookup"><span data-stu-id="37c5d-145">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
-   [<span data-ttu-id="37c5d-146">**EM- \_ tsel**</span><span class="sxs-lookup"><span data-stu-id="37c5d-146">**EM\_SETSEL**</span></span>](em-setsel.md)
-   [<span data-ttu-id="37c5d-147">**EM- \_ settabstopps**</span><span class="sxs-lookup"><span data-stu-id="37c5d-147">**EM\_SETTABSTOPS**</span></span>](em-settabstops.md)
-   [<span data-ttu-id="37c5d-148">**EM \_ setwordbreakproc**</span><span class="sxs-lookup"><span data-stu-id="37c5d-148">**EM\_SETWORDBREAKPROC**</span></span>](em-setwordbreakproc.md)
-   [<span data-ttu-id="37c5d-149">**EM \_ ShowBalloonTip**</span><span class="sxs-lookup"><span data-stu-id="37c5d-149">**EM\_SHOWBALLOONTIP**</span></span>](em-showballoontip.md)
-   [<span data-ttu-id="37c5d-150">**EM- \_ Fokus**</span><span class="sxs-lookup"><span data-stu-id="37c5d-150">**EM\_TAKEFOCUS**</span></span>](em-takefocus.md)
-   [<span data-ttu-id="37c5d-151">**EM \_ rückgängig machen**</span><span class="sxs-lookup"><span data-stu-id="37c5d-151">**EM\_UNDO**</span></span>](em-undo.md)
-   [<span data-ttu-id="37c5d-152">**WM \_ rückgängig machen**</span><span class="sxs-lookup"><span data-stu-id="37c5d-152">**WM\_UNDO**</span></span>](wm-undo.md)

 

 




