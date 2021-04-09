---
description: Dieser Abschnitt enthält eine alphabetische Liste der verfügbaren Gerätefunktionen in der telefoniespi.
ms.assetid: 2a27fbb7-93b5-4106-afd3-e63456650fb9
title: TSPI-Line-Gerätefunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea2ca54096ac89b76a4658129362e87d4281fcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865687"
---
# <a name="tspi-line-device-functions"></a><span data-ttu-id="9a9a7-103">TSPI-Line-Gerätefunktionen</span><span class="sxs-lookup"><span data-stu-id="9a9a7-103">TSPI Line Device Functions</span></span>

<span data-ttu-id="9a9a7-104">Dieser Abschnitt enthält eine alphabetische Liste der verfügbaren Gerätefunktionen in der telefoniespi.</span><span class="sxs-lookup"><span data-stu-id="9a9a7-104">This section contains an alphabetic list of the available line device functions in the Telephony SPI.</span></span> <span data-ttu-id="9a9a7-105">Die Informationen zu den einzelnen Funktionen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9a9a7-105">The information for each function includes the following:</span></span>

-   <span data-ttu-id="9a9a7-106">Eine-Anweisung des Zwecks der Funktion.</span><span class="sxs-lookup"><span data-stu-id="9a9a7-106">A statement of the function's purpose.</span></span>
-   <span data-ttu-id="9a9a7-107">Die korrekte Syntax für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="9a9a7-107">The correct syntax for the function.</span></span>
-   <span data-ttu-id="9a9a7-108">Eine Beschreibung der Funktionsparameter, einschließlich gültiger anrufzustände.</span><span class="sxs-lookup"><span data-stu-id="9a9a7-108">A description of the function's parameters, including valid call states.</span></span>
-   <span data-ttu-id="9a9a7-109">Eine Beschreibung des Rückgabewerts der Funktion.</span><span class="sxs-lookup"><span data-stu-id="9a9a7-109">A description of the function's return value.</span></span>
-   <span data-ttu-id="9a9a7-110">Ein Abschnitt "Hinweise", der eine beliebige oder alle der folgenden Optionen enthalten kann: eine Liste der gültigen aufrufzustände für den Eintrag der Funktion und typische Aufrufe von Zustands Übergängen, wenn die Anforderung abgeschlossen ist. eine Beschreibung der Elemente von großen Datenstrukturen, die vom Dienstanbieter ausgefüllt werden müssen und deren Werte intakt bleiben müssen. und im Vergleich mit einer entsprechenden Funktion in TAPI.</span><span class="sxs-lookup"><span data-stu-id="9a9a7-110">A Remarks section that can include any or all of the following: a list of the valid call states on entry of the function and typical call state transitions when the request completes; a description of which members of large data structures must be filled in by the service provider and which members must have their values preserved intact; and comparison with a corresponding function within TAPI.</span></span>
-   <span data-ttu-id="9a9a7-111">Verweise auf andere Funktionen, Nachrichten oder Datenstrukturen.</span><span class="sxs-lookup"><span data-stu-id="9a9a7-111">References to other functions, messages, or data structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="9a9a7-112">Die tatsächlichen Zustände, in denen eine Funktion ausgeführt werden kann, können durch die Funktionen des Dienstanbieters eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="9a9a7-112">The actual states in which a function can be performed may be limited by the capabilities of the service provider.</span></span> <span data-ttu-id="9a9a7-113">Dienstanbieter müssen den **dwcallfeatures** -Member in der [**linecallstatus**](/windows/win32/api/tapi/ns-tapi-linecallstatus) -Struktur, den **dwaddressfeatures** -Member in der [**lineaddressstatus**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) -Struktur und den **dwlinefeatures** -Member in der [**linedevstatus**](/windows/win32/api/tapi/ns-tapi-linedevstatus) -Struktur festlegen, um Anwendungen anzugeben, ob eine Funktion zu diesem Zeitpunkt zulässig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="9a9a7-113">Service providers must set the **dwCallFeatures** member in the [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus) structure, the **dwAddressFeatures** member in the [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) structure, and the **dwLineFeatures** member in the [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) structure to indicate to applications whether or not a function is permitted at that point in time.</span></span>

     

<span data-ttu-id="9a9a7-114">Dieser Abschnitt enthält die folgenden TSPI-Gerätefunktionen:</span><span class="sxs-lookup"><span data-stu-id="9a9a7-114">This section contains the following TSPI line device functions:</span></span>

-   [<span data-ttu-id="9a9a7-115">**TSPI- \_ lineaccept**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-115">**TSPI\_lineAccept**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept)
-   [<span data-ttu-id="9a9a7-116">**TSPI \_ lineaddtconference**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-116">**TSPI\_lineAddToConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineaddtoconference)
-   [<span data-ttu-id="9a9a7-117">**TSPI- \_ lineanswer**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-117">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer)
-   [<span data-ttu-id="9a9a7-118">**TSPI \_ lineblintransfer**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-118">**TSPI\_lineBlindTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineblindtransfer)
-   [<span data-ttu-id="9a9a7-119">**TSPI- \_ lineclose**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-119">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose)
-   [<span data-ttu-id="9a9a7-120">**TSPI \_ lineclosecall**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-120">**TSPI\_lineCloseCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)
-   [<span data-ttu-id="9a9a7-121">**TSPI \_ lineclosemspinstance**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-121">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [<span data-ttu-id="9a9a7-122">**TSPI \_ linecompletecall**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-122">**TSPI\_lineCompleteCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecompletecall)
-   [<span data-ttu-id="9a9a7-123">**TSPI \_ linecompletetransfer**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-123">**TSPI\_lineCompleteTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [<span data-ttu-id="9a9a7-124">**TSPI \_ lineconditionalmediadetection**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-124">**TSPI\_lineConditionalMediaDetection**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   [<span data-ttu-id="9a9a7-125">**TSPI \_ lineconfigdialog**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-125">**TSPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)
-   [<span data-ttu-id="9a9a7-126">**TSPI \_ lineconfigdialogedit**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-126">**TSPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit)
-   [<span data-ttu-id="9a9a7-127">**TSPI \_ linecreatemspinstance**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-127">**TSPI\_lineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [<span data-ttu-id="9a9a7-128">**TSPI \_ linedevspecific**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-128">**TSPI\_lineDevSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
-   [<span data-ttu-id="9a9a7-129">**TSPI \_ linedevspecificfeature**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-129">**TSPI\_lineDevSpecificFeature**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
-   [<span data-ttu-id="9a9a7-130">**TSPI- \_ linedial**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-130">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)
-   [<span data-ttu-id="9a9a7-131">**TSPI- \_ linedrop**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-131">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)
-   [<span data-ttu-id="9a9a7-132">TSPI \_ linedropnoowner</span><span class="sxs-lookup"><span data-stu-id="9a9a7-132">TSPI\_lineDropNoOwner</span></span>](tspi-linedropnoowner.md)
-   [<span data-ttu-id="9a9a7-133">TSPI \_ linedroponclose</span><span class="sxs-lookup"><span data-stu-id="9a9a7-133">TSPI\_lineDropOnClose</span></span>](tspi-linedroponclose.md)
-   [<span data-ttu-id="9a9a7-134">**TSPI ( \_ lineforward)**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-134">**TSPI\_lineForward**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [<span data-ttu-id="9a9a7-135">**TSPI- \_ linegather-Ziffern**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-135">**TSPI\_lineGatherDigits**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegatherdigits)
-   [<span data-ttu-id="9a9a7-136">**TSPI \_ linegeneratedigits**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-136">**TSPI\_lineGenerateDigits**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits)
-   [<span data-ttu-id="9a9a7-137">**TSPI \_ linegeneratetone**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-137">**TSPI\_lineGenerateTone**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratetone)
-   [<span data-ttu-id="9a9a7-138">**TSPI \_ linegetaddresscaps**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-138">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)
-   [<span data-ttu-id="9a9a7-139">**TSPI \_ linegetadressssid**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-139">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)
-   [<span data-ttu-id="9a9a7-140">**TSPI \_ linegetaddressstatus**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-140">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus)
-   [<span data-ttu-id="9a9a7-141">**TSPI \_ linegetcalladressssid**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-141">**TSPI\_lineGetCallAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid)
-   [<span data-ttu-id="9a9a7-142">**TSPI \_ linegetcallhubtracking**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-142">**TSPI\_lineGetCallHubTracking**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallhubtracking)
-   [<span data-ttu-id="9a9a7-143">**TSPI \_ linegetkallids**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-143">**TSPI\_lineGetCallIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallids)
-   [<span data-ttu-id="9a9a7-144">**TSPI \_ linegetcallinfo**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-144">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)
-   [<span data-ttu-id="9a9a7-145">**TSPI \_ linegetcallstatus**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-145">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)
-   [<span data-ttu-id="9a9a7-146">**TSPI \_ linegetdevcaps**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-146">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)
-   [<span data-ttu-id="9a9a7-147">**TSPI \_ linegetdevconfig**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-147">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)
-   [<span data-ttu-id="9a9a7-148">**TSPI \_ linegetextensionid**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-148">**TSPI\_lineGetExtensionID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetextensionid)
-   [<span data-ttu-id="9a9a7-149">**TSPI- \_ linegeticon**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-149">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)
-   [<span data-ttu-id="9a9a7-150">**TSPI- \_ lineGetID**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-150">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [<span data-ttu-id="9a9a7-151">**TSPI \_ linegetlinedevstatus**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-151">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)
-   [<span data-ttu-id="9a9a7-152">**TSPI \_ linegetnumaddressids**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-152">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids)
-   [<span data-ttu-id="9a9a7-153">**TSPI- \_ linehold**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-153">**TSPI\_lineHold**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linehold)
-   [<span data-ttu-id="9a9a7-154">**TSPI \_ linemakecall**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-154">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [<span data-ttu-id="9a9a7-155">**TSPI \_ linemonitordigits**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-155">**TSPI\_lineMonitorDigits**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)
-   [<span data-ttu-id="9a9a7-156">**TSPI \_ linemonitormedia**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-156">**TSPI\_lineMonitorMedia**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemonitormedia)
-   [<span data-ttu-id="9a9a7-157">**TSPI- \_ linemonitortones**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-157">**TSPI\_lineMonitorTones**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemonitortones)
-   [<span data-ttu-id="9a9a7-158">**TSPI \_ linemspidentify**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-158">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [<span data-ttu-id="9a9a7-159">**TSPI \_ linenegotiateextversion**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-159">**TSPI\_lineNegotiateExtVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion)
-   [<span data-ttu-id="9a9a7-160">**TSPI \_ linenegotiatetspiversion**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-160">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion)
-   [<span data-ttu-id="9a9a7-161">**TSPI ( \_ lineOpen)**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-161">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)
-   [<span data-ttu-id="9a9a7-162">**TSPI- \_ linepark**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-162">**TSPI\_linePark**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linepark)
-   [<span data-ttu-id="9a9a7-163">**TSPI- \_ linepickup**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-163">**TSPI\_linePickup**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [<span data-ttu-id="9a9a7-164">**TSPI \_ lineprepareaddumconference**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-164">**TSPI\_linePrepareAddToConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [<span data-ttu-id="9a9a7-165">**TSPI \_ linereceivemspdata**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-165">**TSPI\_lineReceiveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [<span data-ttu-id="9a9a7-166">**TSPI \_ lineredirect**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-166">**TSPI\_lineRedirect**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineredirect)
-   [<span data-ttu-id="9a9a7-167">**TSPI \_ linereleaseuseruserinfo**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-167">**TSPI\_lineReleaseUserUserInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereleaseuseruserinfo)
-   [<span data-ttu-id="9a9a7-168">**TSPI \_ lineremovefromconference**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-168">**TSPI\_lineRemoveFromConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineremovefromconference)
-   [<span data-ttu-id="9a9a7-169">**TSPI \_ linesecurecall**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-169">**TSPI\_lineSecureCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesecurecall)
-   [<span data-ttu-id="9a9a7-170">**TSPI \_ lineselectextversion**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-170">**TSPI\_lineSelectExtVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion)
-   [<span data-ttu-id="9a9a7-171">**TSPI \_ linesenduseruserinfo**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-171">**TSPI\_lineSendUserUserInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesenduseruserinfo)
-   [<span data-ttu-id="9a9a7-172">**TSPI \_ linesetappspecific**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-172">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific)
-   [<span data-ttu-id="9a9a7-173">**TSPI \_ linesetcalldata**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-173">**TSPI\_lineSetCallData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [<span data-ttu-id="9a9a7-174">**TSPI \_ linesetcallhubtracking**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-174">**TSPI\_lineSetCallHubTracking**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallhubtracking)
-   [<span data-ttu-id="9a9a7-175">**TSPI \_ linesetcallparametriams**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-175">**TSPI\_lineSetCallParams**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallparams)
-   [<span data-ttu-id="9a9a7-176">**TSPI \_ linesetcallqualityofservice**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-176">**TSPI\_lineSetCallQualityOfService**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [<span data-ttu-id="9a9a7-177">**TSPI \_ linesetcalltreatment**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-177">**TSPI\_lineSetCallTreatment**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [<span data-ttu-id="9a9a7-178">TSPI \_ linesetcurrentlocation</span><span class="sxs-lookup"><span data-stu-id="9a9a7-178">TSPI\_lineSetCurrentLocation</span></span>](tspi-linesetcurrentlocation.md)
-   [<span data-ttu-id="9a9a7-179">**TSPI \_ linesetdefaultmediadetection**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-179">**TSPI\_lineSetDefaultMediaDetection**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection)
-   [<span data-ttu-id="9a9a7-180">**TSPI \_ linesetdevconfig**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-180">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)
-   [<span data-ttu-id="9a9a7-181">**TSPI \_ linesetlinedevstatus**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-181">**TSPI\_lineSetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [<span data-ttu-id="9a9a7-182">**TSPI \_ linesetmediacontrol**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-182">**TSPI\_lineSetMediaControl**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediacontrol)
-   [<span data-ttu-id="9a9a7-183">**TSPI \_ linesetmediamode**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-183">**TSPI\_lineSetMediaMode**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediamode)
-   [<span data-ttu-id="9a9a7-184">**TSPI- \_ linesetstatus-Meldungen**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-184">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)
-   [<span data-ttu-id="9a9a7-185">**TSPI \_ linesetterminal**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-185">**TSPI\_lineSetTerminal**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal)
-   [<span data-ttu-id="9a9a7-186">**TSPI \_ linesetupconference**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-186">**TSPI\_lineSetupConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [<span data-ttu-id="9a9a7-187">**TSPI \_ lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-187">**TSPI\_lineSetupTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [<span data-ttu-id="9a9a7-188">**TSPI \_ lineswaphold**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-188">**TSPI\_lineSwapHold**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineswaphold)
-   [<span data-ttu-id="9a9a7-189">**TSPI \_ lineuncompletecall**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-189">**TSPI\_lineUncompleteCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineuncompletecall)
-   [<span data-ttu-id="9a9a7-190">**TSPI \_ lineunhold**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-190">**TSPI\_lineUnhold**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineunhold)
-   [<span data-ttu-id="9a9a7-191">**TSPI \_ lineunpark**</span><span class="sxs-lookup"><span data-stu-id="9a9a7-191">**TSPI\_lineUnpark**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
