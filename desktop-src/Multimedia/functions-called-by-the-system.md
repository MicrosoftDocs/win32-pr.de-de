---
title: Vom System aufgerufene Funktionen
description: Vom System aufgerufene Funktionen
ms.assetid: 006ac524-d456-44e9-957b-42a85dc92519
keywords:
- Multimedia-Audiofunktionen, ACM-Funktionen
- Audiofunktionen, ACM-Funktionen
- Audiokomprimierungs-Manager (ACM), Funktionen
- ACM (Audiokomprimierungs-Manager), Funktionen
- ACM-Funktionen
- Rückruffunktionen
- Audiokomprimierungs-Manager (ACM), Rückruf Funktionen
- ACM (Audiokomprimierungs-Manager), Rückruf Funktionen
- Hook-Verfahren
- Treiber Prozeduren
- Audiokomprimierungs-Manager (ACM), Hook-Prozeduren
- ACM (Audiokomprimierungs-Manager), Hook-Prozeduren
- Audiokomprimierungs-Manager (ACM), Treiber Prozeduren
- ACM (Audiokomprimierungs-Manager), Treiber Prozeduren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1324ea168892d54f21754658607476c35075910
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337841"
---
# <a name="functions-called-by-the-system"></a><span data-ttu-id="8c0a5-117">Vom System aufgerufene Funktionen</span><span class="sxs-lookup"><span data-stu-id="8c0a5-117">Functions Called by the System</span></span>

<span data-ttu-id="8c0a5-118">Das System ruft drei verschiedene Arten von Anwendungs definierten Funktionen auf.</span><span class="sxs-lookup"><span data-stu-id="8c0a5-118">The system calls three different kinds of application-defined functions.</span></span> <span data-ttu-id="8c0a5-119">Rückruf Funktionen sind Funktionen in der Anwendung, die vom System als Antwort auf eine Anforderung einer Anwendung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8c0a5-119">Callback functions are functions in your application that the system calls in response to a request made by an application.</span></span> <span data-ttu-id="8c0a5-120">Mithilfe von Hook-Prozeduren wird die Anpassung von Dialogfeldern von der Anwendung behandelt.</span><span class="sxs-lookup"><span data-stu-id="8c0a5-120">Hook procedures help an application handle the customization of dialog boxes.</span></span> <span data-ttu-id="8c0a5-121">Eine Treiber Prozedur ist die Implementierung eines eigenen Codecs, Konverters oder Filters einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="8c0a5-121">A driver procedure is an application's implementation of its own codec, converter, or filter.</span></span>

<span data-ttu-id="8c0a5-122">Die Rückruf Funktionen haben die folgenden Namen:</span><span class="sxs-lookup"><span data-stu-id="8c0a5-122">The callback functions have the following names:</span></span>

-   [<span data-ttu-id="8c0a5-123">**acmdriverenumcallback**</span><span class="sxs-lookup"><span data-stu-id="8c0a5-123">**acmDriverEnumCallback**</span></span>](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [<span data-ttu-id="8c0a5-124">**acmfilterenumcallback**</span><span class="sxs-lookup"><span data-stu-id="8c0a5-124">**acmFilterEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [<span data-ttu-id="8c0a5-125">**acmfiltertagenumschlag**</span><span class="sxs-lookup"><span data-stu-id="8c0a5-125">**acmFilterTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [<span data-ttu-id="8c0a5-126">**acmformatenumcallback**</span><span class="sxs-lookup"><span data-stu-id="8c0a5-126">**acmFormatEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [<span data-ttu-id="8c0a5-127">**acmformattagenumschlag**</span><span class="sxs-lookup"><span data-stu-id="8c0a5-127">**acmFormatTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   <span data-ttu-id="8c0a5-128">[**acmstreamconvertcallback**](/previous-versions//dd742925(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c0a5-128">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span></span>

<span data-ttu-id="8c0a5-129">Die meisten Enumerationsfunktionen im ACM verwenden Rückruf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="8c0a5-129">Most of the enumeration functions in the ACM use callback functions.</span></span> <span data-ttu-id="8c0a5-130">Wenn Sie z. b. eine Enumerationsfunktion aufrufen, listet das ACM die Elemente auf, indem die Anwendung wiederholt über die Rückruffunktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8c0a5-130">For example, when you call an enumeration function, the ACM enumerates the items by repeatedly calling the application through the callback function.</span></span>

<span data-ttu-id="8c0a5-131">Einige Funktionen können nicht in diesen Rückruf Funktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8c0a5-131">Some functions cannot be called from within these callback functions.</span></span> <span data-ttu-id="8c0a5-132">Funktionen, die nicht aufgerufen werden können, bearbeiten interne ACM-Strukturen, die von den-Enumerationsfunktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c0a5-132">Functions that cannot be called manipulate internal ACM structures that are used by the enumeration functions.</span></span> <span data-ttu-id="8c0a5-133">Die folgenden Funktionen sollten nicht innerhalb einer Rückruffunktion aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="8c0a5-133">The following functions should not be called from within a callback function:</span></span>

-   [<span data-ttu-id="8c0a5-134">**acmdriveradd**</span><span class="sxs-lookup"><span data-stu-id="8c0a5-134">**acmDriverAdd**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [<span data-ttu-id="8c0a5-135">**acmdriverpriority**</span><span class="sxs-lookup"><span data-stu-id="8c0a5-135">**acmDriverPriority**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [<span data-ttu-id="8c0a5-136">**acmdriverremove**</span><span class="sxs-lookup"><span data-stu-id="8c0a5-136">**acmDriverRemove**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

<span data-ttu-id="8c0a5-137">Das System ruft die folgenden Funktionen auf, um einer Anwendung zu helfen, die Anpassung von Dialogfeldern zu handhaben:</span><span class="sxs-lookup"><span data-stu-id="8c0a5-137">The system calls the following functions to help an application handle the customization of dialog boxes:</span></span>

-   [<span data-ttu-id="8c0a5-138">**acmfilterchooabhuokproc**</span><span class="sxs-lookup"><span data-stu-id="8c0a5-138">**acmFilterChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [<span data-ttu-id="8c0a5-139">**acmformatchooabhuokproc**</span><span class="sxs-lookup"><span data-stu-id="8c0a5-139">**acmFormatChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)

<span data-ttu-id="8c0a5-140">Die folgende Funktion wird als Prototyp angegeben, der es einer Anwendung ermöglicht, einen angepassten Codec, Konverter oder Filter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c0a5-140">The following function is specified as a prototype that allows an application to use a customized codec, converter, or filter.</span></span> <span data-ttu-id="8c0a5-141">Eine Funktion, die diesem Prototyp entspricht, kann als Argument an die [**acmdriveradd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) -Funktion übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="8c0a5-141">A function conforming to this prototype may be passed as an argument to the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function.</span></span>

-   [<span data-ttu-id="8c0a5-142">**acmdriverproc**</span><span class="sxs-lookup"><span data-stu-id="8c0a5-142">**acmDriverProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)

 

 