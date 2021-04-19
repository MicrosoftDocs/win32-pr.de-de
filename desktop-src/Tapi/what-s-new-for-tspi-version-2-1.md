---
description: Beginnend mit TAPI 2,1 können die Benutzeroberflächen-DLLs des Telefoniedienstanbieters zum Verwalten und Anzeigen von Dialogfeldern verwendet werden. TAPI lädt die dll in den Prozess einer Anwendung, die eine beliebige Dienstanbieter Funktion aufruft, die ein Dialogfeld anzeigen kann.
ms.assetid: 0a0320d1-fb75-405e-8074-b37cef956c9f
title: Neuerungen bei TSPI Version 2,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51642fb9ac960732f8e4a56805652333d0c32468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349494"
---
# <a name="whats-new-for-tspi-version-21"></a><span data-ttu-id="1d95a-104">Neuerungen bei TSPI Version 2,1</span><span class="sxs-lookup"><span data-stu-id="1d95a-104">What's New for TSPI Version 2.1</span></span>

<span data-ttu-id="1d95a-105">Beginnend mit TAPI 2,1 können die Benutzeroberflächen-DLLs des Telefoniedienstanbieters zum Verwalten und Anzeigen von Dialogfeldern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d95a-105">Starting with TAPI 2.1, the telephony service provider user interface DLLs can be used to manage and display dialog boxes.</span></span> <span data-ttu-id="1d95a-106">TAPI lädt die dll in den Prozess einer Anwendung, die eine beliebige Dienstanbieter Funktion aufruft, die ein Dialogfeld anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="1d95a-106">TAPI loads the DLL into the process of an application that invokes any of the service provider functions that can display a dialog.</span></span>

<span data-ttu-id="1d95a-107">Ab TAPI 2,1 können Proxy Anforderungs Handler implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="1d95a-107">Starting with TAPI 2.1, proxy request handlers can be implemented.</span></span> <span data-ttu-id="1d95a-108">Ein Handler ist eine vollständige Telefonieanwendung, die normalerweise auf einem Telefonieserver ausgeführt wird und Dienste bereitstellt, die in einer Anwendung besser implementiert sind als ein Treiber.</span><span class="sxs-lookup"><span data-stu-id="1d95a-108">A handler is a full telephony application that normally executes on a telephony server and provides services that are more appropriately implemented in an application than a driver.</span></span>

<span data-ttu-id="1d95a-109">Funktionen und Nachrichten, die für TSPI Version 2,1 neu oder geändert wurden, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1d95a-109">Functions and messages that were new or changed for TSPI version 2.1 are as follows:</span></span>

-   [<span data-ttu-id="1d95a-110">**TSPI_lineConditionalMediaDetection**</span><span class="sxs-lookup"><span data-stu-id="1d95a-110">**TSPI_lineConditionalMediaDetection**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   <span data-ttu-id="1d95a-111">**TSPI_lineDropNoOwner**–**veraltet**</span><span class="sxs-lookup"><span data-stu-id="1d95a-111">**TSPI_lineDropNoOwner**—**obsolete**</span></span>
-   <span data-ttu-id="1d95a-112">**TSPI_lineDropOnClose**–**veraltet**</span><span class="sxs-lookup"><span data-stu-id="1d95a-112">**TSPI_lineDropOnClose**—**obsolete**</span></span>
-   [<span data-ttu-id="1d95a-113">**TSPI_lineGetID**</span><span class="sxs-lookup"><span data-stu-id="1d95a-113">**TSPI_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [<span data-ttu-id="1d95a-114">**TSPI_lineSetCallData**</span><span class="sxs-lookup"><span data-stu-id="1d95a-114">**TSPI_lineSetCallData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [<span data-ttu-id="1d95a-115">**TSPI_lineSetCallQualityOfService**</span><span class="sxs-lookup"><span data-stu-id="1d95a-115">**TSPI_lineSetCallQualityOfService**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [<span data-ttu-id="1d95a-116">**TSPI_lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="1d95a-116">**TSPI_lineSetCallTreatment**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [<span data-ttu-id="1d95a-117">**TSPI_lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="1d95a-117">**TSPI_lineSetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [<span data-ttu-id="1d95a-118">**TSPI_phoneGetID**</span><span class="sxs-lookup"><span data-stu-id="1d95a-118">**TSPI_phoneGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonegetid)
-   [<span data-ttu-id="1d95a-119">**TSPI_providerInit**</span><span class="sxs-lookup"><span data-stu-id="1d95a-119">**TSPI_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)
-   [<span data-ttu-id="1d95a-120">**TSPI_providerShutdown**</span><span class="sxs-lookup"><span data-stu-id="1d95a-120">**TSPI_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)
-   <span data-ttu-id="1d95a-121">[**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d95a-121">[**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))</span></span>
-   <span data-ttu-id="1d95a-122">[**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d95a-122">[**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))</span></span>
-   <span data-ttu-id="1d95a-123">[**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d95a-123">[**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))</span></span>
-   <span data-ttu-id="1d95a-124">[**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d95a-124">[**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))</span></span>
-   <span data-ttu-id="1d95a-125">[**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d95a-125">[**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))</span></span>
-   <span data-ttu-id="1d95a-126">[**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d95a-126">[**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))</span></span>
-   <span data-ttu-id="1d95a-127">[**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d95a-127">[**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))</span></span>

<span data-ttu-id="1d95a-128">Die Benutzeroberflächen-DLL des Telefoniedienstanbieters bietet eine Möglichkeit, Benutzerinteraktionen im Kontext der Anwendung anstelle des Dienstanbieters selbst zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="1d95a-128">The Telephony service provider user interface DLL provides a means of allowing user interaction within the context of the application rather than the service provider itself.</span></span> <span data-ttu-id="1d95a-129">TSPI Version 2,1 hat die folgenden neuen Funktionen, Meldungen und Strukturen für die Implementierung bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="1d95a-129">TSPI version 2.1 delivered the following new functions, messages, and structures for implementation:</span></span>

-   [<span data-ttu-id="1d95a-130">**TSPI_providerFreeDialogInstance**</span><span class="sxs-lookup"><span data-stu-id="1d95a-130">**TSPI_providerFreeDialogInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance)
-   [<span data-ttu-id="1d95a-131">**TSPI_providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="1d95a-131">**TSPI_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata)
-   [<span data-ttu-id="1d95a-132">**TSPI_providerUIIdentify**</span><span class="sxs-lookup"><span data-stu-id="1d95a-132">**TSPI_providerUIIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify)
-   [<span data-ttu-id="1d95a-133">**TUISPI_lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="1d95a-133">**TUISPI_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)
-   [<span data-ttu-id="1d95a-134">**TUISPI_lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="1d95a-134">**TUISPI_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit)
-   [<span data-ttu-id="1d95a-135">**TUISPI_phoneConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="1d95a-135">**TUISPI_phoneConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog)
-   [<span data-ttu-id="1d95a-136">**TUISPI_providerConfig**</span><span class="sxs-lookup"><span data-stu-id="1d95a-136">**TUISPI_providerConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig)
-   [<span data-ttu-id="1d95a-137">**TUISPI_providerGenericDialog**</span><span class="sxs-lookup"><span data-stu-id="1d95a-137">**TUISPI_providerGenericDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog)
-   [<span data-ttu-id="1d95a-138">**TUISPI_providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="1d95a-138">**TUISPI_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
-   [<span data-ttu-id="1d95a-139">**TUISPI_providerInstall**</span><span class="sxs-lookup"><span data-stu-id="1d95a-139">**TUISPI_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)
-   [<span data-ttu-id="1d95a-140">**TUISPI_providerRemove**</span><span class="sxs-lookup"><span data-stu-id="1d95a-140">**TUISPI_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)
-   [<span data-ttu-id="1d95a-141">**"Tuispikreatedialoginstanceparameginstancepara"**</span><span class="sxs-lookup"><span data-stu-id="1d95a-141">**TUISPICREATEDIALOGINSTANCEPARAMS**</span></span>](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
-   [<span data-ttu-id="1d95a-142">**Tuispidllcallback**</span><span class="sxs-lookup"><span data-stu-id="1d95a-142">**TUISPIDLLCALLBACK**</span></span>](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
-   [<span data-ttu-id="1d95a-143">**LINE_CREATEDIALOGINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="1d95a-143">**LINE_CREATEDIALOGINSTANCE**</span></span>](line-createdialoginstance.md)
-   [<span data-ttu-id="1d95a-144">**LINE_SENDDIALOGINSTANCEDATA**</span><span class="sxs-lookup"><span data-stu-id="1d95a-144">**LINE_SENDDIALOGINSTANCEDATA**</span></span>](line-senddialoginstancedata.md)

 

 
