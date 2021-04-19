---
description: Verwenden Sie die folgenden Funktionen, um Leistungsdaten zu nutzen und bereitzustellen.
ms.assetid: a2c97b8b-b1b1-4dd8-8f23-edffaa74d028
title: Funktionen der Leistungsindikatoren
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8ef01ac07ae8507f1005839ab838e2528e76d6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349859"
---
# <a name="performance-counters-functions"></a><span data-ttu-id="32763-103">Funktionen der Leistungsindikatoren</span><span class="sxs-lookup"><span data-stu-id="32763-103">Performance Counters Functions</span></span>

<span data-ttu-id="32763-104">Verwenden Sie die folgenden Funktionen, um Leistungsdaten zu nutzen und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="32763-104">Use the following functions to consume and provide performance data.</span></span>

## <a name="consumer-functions"></a><span data-ttu-id="32763-105">Consumer-Funktionen</span><span class="sxs-lookup"><span data-stu-id="32763-105">Consumer functions</span></span>

### <a name="performance-data-helper-pdh-functions"></a><span data-ttu-id="32763-106">PDH-Funktionen (Performance Data Helper)</span><span class="sxs-lookup"><span data-stu-id="32763-106">Performance Data Helper (PDH) functions</span></span>

<span data-ttu-id="32763-107">Verwenden Sie die Leistungsdaten Hilfsfunktionen (PDH), um Leistungsdaten von v1-und v2-Leistungsdaten Anbietern zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="32763-107">Use the Performance Data Helper (PDH) functions to consume performance data from both V1 and V2 performance data providers.</span></span>

> [!Note]
> <span data-ttu-id="32763-108">Windows onecore-Apps können die PDH-Funktionen nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="32763-108">Windows OneCore apps cannot use the PDH functions.</span></span> <span data-ttu-id="32763-109">Verwenden Sie beim Schreiben von Windows onecore-apps [Perflib v2-consumerfunktionen](using-the-perflib-functions-to-consume-counter-data.md).</span><span class="sxs-lookup"><span data-stu-id="32763-109">If you are writing Windows OneCore apps, use [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md).</span></span>

- [<span data-ttu-id="32763-110">*Counterpathcallback*</span><span class="sxs-lookup"><span data-stu-id="32763-110">*CounterPathCallBack*</span></span>](/windows/desktop/api/Pdh/nc-pdh-counterpathcallback)
- [<span data-ttu-id="32763-111">**Pdhaddcounter**</span><span class="sxs-lookup"><span data-stu-id="32763-111">**PdhAddCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera)
- [<span data-ttu-id="32763-112">**Pdhaddenglishcounter**</span><span class="sxs-lookup"><span data-stu-id="32763-112">**PdhAddEnglishCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera)
- [<span data-ttu-id="32763-113">**Pdhbindinputdatasource**</span><span class="sxs-lookup"><span data-stu-id="32763-113">**PdhBindInputDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea)
- [<span data-ttu-id="32763-114">**Pdhbrowpcounters**</span><span class="sxs-lookup"><span data-stu-id="32763-114">**PdhBrowseCounters**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa)
- [<span data-ttu-id="32763-115">**Pdhbrowpcountersh**</span><span class="sxs-lookup"><span data-stu-id="32763-115">**PdhBrowseCountersH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersha)
- [<span data-ttu-id="32763-116">**Pdhcalculatecounterfromrawvalue**</span><span class="sxs-lookup"><span data-stu-id="32763-116">**PdhCalculateCounterFromRawValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue)
- [<span data-ttu-id="32763-117">**Pdhcloselog**</span><span class="sxs-lookup"><span data-stu-id="32763-117">**PdhCloseLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog)
- [<span data-ttu-id="32763-118">**Pdhclosequery**</span><span class="sxs-lookup"><span data-stu-id="32763-118">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [<span data-ttu-id="32763-119">**Pdhcollectquerydata**</span><span class="sxs-lookup"><span data-stu-id="32763-119">**PdhCollectQueryData**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [<span data-ttu-id="32763-120">**Pdhcollectquerydataex**</span><span class="sxs-lookup"><span data-stu-id="32763-120">**PdhCollectQueryDataEx**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex)
- [<span data-ttu-id="32763-121">**Pdhcollectquerydatawithtime**</span><span class="sxs-lookup"><span data-stu-id="32763-121">**PdhCollectQueryDataWithTime**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydatawithtime)
- [<span data-ttu-id="32763-122">**Pdhcomputecounterstatistics**</span><span class="sxs-lookup"><span data-stu-id="32763-122">**PdhComputeCounterStatistics**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics)
- [<span data-ttu-id="32763-123">**Pdhconnectmachine**</span><span class="sxs-lookup"><span data-stu-id="32763-123">**PdhConnectMachine**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhconnectmachinea)
- [<span data-ttu-id="32763-124">**Pdhenumschlag logsetnames**</span><span class="sxs-lookup"><span data-stu-id="32763-124">**PdhEnumLogSetNames**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumlogsetnamesa)
- [<span data-ttu-id="32763-125">**Pdhenumschlag Machines**</span><span class="sxs-lookup"><span data-stu-id="32763-125">**PdhEnumMachines**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesa)
- [<span data-ttu-id="32763-126">**Pdhenumschlag machinesh**</span><span class="sxs-lookup"><span data-stu-id="32763-126">**PdhEnumMachinesH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesha)
- [<span data-ttu-id="32763-127">**Pdhenumubjectitems**</span><span class="sxs-lookup"><span data-stu-id="32763-127">**PdhEnumObjectItems**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa)
- [<span data-ttu-id="32763-128">**Pdhenumubjectitemsh**</span><span class="sxs-lookup"><span data-stu-id="32763-128">**PdhEnumObjectItemsH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsha)
- [<span data-ttu-id="32763-129">**Pdhenumubjects**</span><span class="sxs-lookup"><span data-stu-id="32763-129">**PdhEnumObjects**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa)
- [<span data-ttu-id="32763-130">**Pdhenumubjectsh**</span><span class="sxs-lookup"><span data-stu-id="32763-130">**PdhEnumObjectsH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsha)
- [<span data-ttu-id="32763-131">**Pdhexpandcounterpath**</span><span class="sxs-lookup"><span data-stu-id="32763-131">**PdhExpandCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandcounterpatha)
- [<span data-ttu-id="32763-132">**PdhExpandWildCardPath**</span><span class="sxs-lookup"><span data-stu-id="32763-132">**PdhExpandWildCardPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)
- [<span data-ttu-id="32763-133">**Pdhexpandwildcardpathh**</span><span class="sxs-lookup"><span data-stu-id="32763-133">**PdhExpandWildCardPathH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpathha)
- [<span data-ttu-id="32763-134">**Pdhformatfromrawvalue**</span><span class="sxs-lookup"><span data-stu-id="32763-134">**PdhFormatFromRawValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue)
- [<span data-ttu-id="32763-135">**Pdhgetcounterinfo**</span><span class="sxs-lookup"><span data-stu-id="32763-135">**PdhGetCounterInfo**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetcounterinfoa)
- [<span data-ttu-id="32763-136">**Pdhgetcountertimebase**</span><span class="sxs-lookup"><span data-stu-id="32763-136">**PdhGetCounterTimeBase**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase)
- [<span data-ttu-id="32763-137">**Pdhgetdatasourcetimerange**</span><span class="sxs-lookup"><span data-stu-id="32763-137">**PdhGetDataSourceTimeRange**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea)
- [<span data-ttu-id="32763-138">**PdhGetDataSourceTimeRangeH**</span><span class="sxs-lookup"><span data-stu-id="32763-138">**PdhGetDataSourceTimeRangeH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangeh)
- [<span data-ttu-id="32763-139">**Pdhgetdefaultperfcounter**</span><span class="sxs-lookup"><span data-stu-id="32763-139">**PdhGetDefaultPerfCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcountera)
- [<span data-ttu-id="32763-140">**Pdhgetdefaultperfcounterh**</span><span class="sxs-lookup"><span data-stu-id="32763-140">**PdhGetDefaultPerfCounterH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcounterha)
- [<span data-ttu-id="32763-141">**Pdhgetdefaultperfobject**</span><span class="sxs-lookup"><span data-stu-id="32763-141">**PdhGetDefaultPerfObject**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjecta)
- [<span data-ttu-id="32763-142">**Pdhgetdefaultperfobjecth**</span><span class="sxs-lookup"><span data-stu-id="32763-142">**PdhGetDefaultPerfObjectH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjectha)
- [<span data-ttu-id="32763-143">**Pdhgetdllversion**</span><span class="sxs-lookup"><span data-stu-id="32763-143">**PdhGetDllVersion**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdllversion)
- [<span data-ttu-id="32763-144">**Pdhgetformattedcounterarray**</span><span class="sxs-lookup"><span data-stu-id="32763-144">**PdhGetFormattedCounterArray**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya)
- [<span data-ttu-id="32763-145">**Pdhgetformattedcountervalue**</span><span class="sxs-lookup"><span data-stu-id="32763-145">**PdhGetFormattedCounterValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)
- [<span data-ttu-id="32763-146">**Pdhgetlogfilesize**</span><span class="sxs-lookup"><span data-stu-id="32763-146">**PdhGetLogFileSize**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
- [<span data-ttu-id="32763-147">**Pdhgetrawcounterarray**</span><span class="sxs-lookup"><span data-stu-id="32763-147">**PdhGetRawCounterArray**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya)
- [<span data-ttu-id="32763-148">**Pdhgetrawcountervalue**</span><span class="sxs-lookup"><span data-stu-id="32763-148">**PdhGetRawCounterValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)
- [<span data-ttu-id="32763-149">**Pdhisrealtimequery**</span><span class="sxs-lookup"><span data-stu-id="32763-149">**PdhIsRealTimeQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhisrealtimequery)
- [<span data-ttu-id="32763-150">**Pdhlookupperfindexbyname**</span><span class="sxs-lookup"><span data-stu-id="32763-150">**PdhLookupPerfIndexByName**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfindexbynamea)
- [<span data-ttu-id="32763-151">**Pdhlookupperfnamebyindex**</span><span class="sxs-lookup"><span data-stu-id="32763-151">**PdhLookupPerfNameByIndex**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfnamebyindexa)
- [<span data-ttu-id="32763-152">**Pdhmakecounterpath**</span><span class="sxs-lookup"><span data-stu-id="32763-152">**PdhMakeCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha)
- [<span data-ttu-id="32763-153">**Pdhoptolog**</span><span class="sxs-lookup"><span data-stu-id="32763-153">**PdhOpenLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
- [<span data-ttu-id="32763-154">**Pdhopumquery**</span><span class="sxs-lookup"><span data-stu-id="32763-154">**PdhOpenQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya)
- [<span data-ttu-id="32763-155">**Pdhopenqueryh**</span><span class="sxs-lookup"><span data-stu-id="32763-155">**PdhOpenQueryH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh)
- [<span data-ttu-id="32763-156">**Pdhparser-counterpath**</span><span class="sxs-lookup"><span data-stu-id="32763-156">**PdhParseCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha)
- [<span data-ttu-id="32763-157">**Pdhparameseinstancename**</span><span class="sxs-lookup"><span data-stu-id="32763-157">**PdhParseInstanceName**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea)
- [<span data-ttu-id="32763-158">**Pdhleserrawlogrecord**</span><span class="sxs-lookup"><span data-stu-id="32763-158">**PdhReadRawLogRecord**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhreadrawlogrecord)
- [<span data-ttu-id="32763-159">**PdhRemoveCounter**</span><span class="sxs-lookup"><span data-stu-id="32763-159">**PdhRemoveCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [<span data-ttu-id="32763-160">**Pdhselectdatasource**</span><span class="sxs-lookup"><span data-stu-id="32763-160">**PdhSelectDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea)
- [<span data-ttu-id="32763-161">**Pdhsetcounterscalefactor**</span><span class="sxs-lookup"><span data-stu-id="32763-161">**PdhSetCounterScaleFactor**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor)
- [<span data-ttu-id="32763-162">**Pdhsetdefaultrealtimedatasource**</span><span class="sxs-lookup"><span data-stu-id="32763-162">**PdhSetDefaultRealTimeDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetdefaultrealtimedatasource)
- [<span data-ttu-id="32763-163">**Pdhsetquerytimerange**</span><span class="sxs-lookup"><span data-stu-id="32763-163">**PdhSetQueryTimeRange**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange)
- [<span data-ttu-id="32763-164">**Pdhupdatelog**</span><span class="sxs-lookup"><span data-stu-id="32763-164">**PdhUpdateLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
- [<span data-ttu-id="32763-165">**Pdhupdatelogfilecatalog**</span><span class="sxs-lookup"><span data-stu-id="32763-165">**PdhUpdateLogFileCatalog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdatelogfilecatalog)
- [<span data-ttu-id="32763-166">**Pdhvalidatepath**</span><span class="sxs-lookup"><span data-stu-id="32763-166">**PdhValidatePath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha)
- [<span data-ttu-id="32763-167">**Pdhvalidatepathex**</span><span class="sxs-lookup"><span data-stu-id="32763-167">**PdhValidatePathEx**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepathexa)

### <a name="perflib-v2-consumer-functions"></a><span data-ttu-id="32763-168">Perflib v2-consumerfunktionen</span><span class="sxs-lookup"><span data-stu-id="32763-168">PerfLib V2 Consumer functions</span></span>

<span data-ttu-id="32763-169">Verwenden Sie die Perflib v2-consumerfunktionen, um Leistungsdaten von V2-Leistungsdaten Anbietern zu nutzen, wenn Sie die PDH-Funktionen (Performance Data Helper) nicht verwenden können.</span><span class="sxs-lookup"><span data-stu-id="32763-169">Use the PerfLib V2 Consumer functions to consume performance data from V2 performance data providers if you cannot use the Performance Data Helper (PDH) functions.</span></span> <span data-ttu-id="32763-170">Diese Funktionen können verwendet werden, wenn Sie onecore-Anwendungen schreiben, um v2-Gegensätze zu erfassen, oder wenn Sie bestimmte v2-Gegensätze mit minimalen Abhängigkeiten und mehr Aufwand erfassen müssen.</span><span class="sxs-lookup"><span data-stu-id="32763-170">These functions might be used when writing OneCore applications to collect V2 countersets or when you need to collect specific V2 countersets with minimal dependencies and overhead.</span></span>

> [!TIP]
> <span data-ttu-id="32763-171">Die Perflib v2-consumerfunktionen sind schwieriger zu verwenden als die PDH-Funktionen (Performance Data Helper) und unterstützen nur das Sammeln von Daten von V2-Anbietern.</span><span class="sxs-lookup"><span data-stu-id="32763-171">The PerfLib V2 Consumer functions are harder to use than the Performance Data Helper (PDH) functions and only support collecting data from V2 providers.</span></span> <span data-ttu-id="32763-172">Die PDH-Funktionen sollten für die meisten Anwendungen bevorzugt werden.</span><span class="sxs-lookup"><span data-stu-id="32763-172">The PDH functions should be preferred for most applications.</span></span>

- [<span data-ttu-id="32763-173">**Perfaddcounters**</span><span class="sxs-lookup"><span data-stu-id="32763-173">**PerfAddCounters**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters)
- [<span data-ttu-id="32763-174">**Perfclosequeryhandle**</span><span class="sxs-lookup"><span data-stu-id="32763-174">**PerfCloseQueryHandle**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle)
- [<span data-ttu-id="32763-175">**Perfdeletecounters**</span><span class="sxs-lookup"><span data-stu-id="32763-175">**PerfDeleteCounters**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters)
- [<span data-ttu-id="32763-176">**Perfenumeratecounterset**</span><span class="sxs-lookup"><span data-stu-id="32763-176">**PerfEnumerateCounterSet**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset)
- [<span data-ttu-id="32763-177">**Perfenumeratecounterset-Funktion**</span><span class="sxs-lookup"><span data-stu-id="32763-177">**PerfEnumerateCounterSetInstances**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances)
- [<span data-ttu-id="32763-178">**Perfopenqueryhandle**</span><span class="sxs-lookup"><span data-stu-id="32763-178">**PerfOpenQueryHandle**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle)
- [<span data-ttu-id="32763-179">**Perfquerycounterdata**</span><span class="sxs-lookup"><span data-stu-id="32763-179">**PerfQueryCounterData**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata)
- [<span data-ttu-id="32763-180">**Perfquerycounterinfo**</span><span class="sxs-lookup"><span data-stu-id="32763-180">**PerfQueryCounterInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo)
- [<span data-ttu-id="32763-181">**Perfquerycounterset tregistrationinfo**</span><span class="sxs-lookup"><span data-stu-id="32763-181">**PerfQueryCounterSetRegistrationInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo)

## <a name="provider-functions"></a><span data-ttu-id="32763-182">Anbieter Funktionen</span><span class="sxs-lookup"><span data-stu-id="32763-182">Provider functions</span></span>

### <a name="perflib-v2-provider-functions"></a><span data-ttu-id="32763-183">Perflib v2-Anbieter Funktionen</span><span class="sxs-lookup"><span data-stu-id="32763-183">PerfLib V2 Provider functions</span></span>

<span data-ttu-id="32763-184">[V2-Leistungsdaten Anbieter](providing-counter-data-using-version-2-0.md) verwenden die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="32763-184">[V2 performance data providers](providing-counter-data-using-version-2-0.md) use the following functions:</span></span>

- [<span data-ttu-id="32763-185">*"Belegcatememory"*</span><span class="sxs-lookup"><span data-stu-id="32763-185">*AllocateMemory*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)
- [<span data-ttu-id="32763-186">*Controlcallback*</span><span class="sxs-lookup"><span data-stu-id="32763-186">*ControlCallback*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [<span data-ttu-id="32763-187">**Gegen Cleanup**</span><span class="sxs-lookup"><span data-stu-id="32763-187">**CounterCleanup**</span></span>](countercleanup.md)
- [<span data-ttu-id="32763-188">**Gegen initialisieren**</span><span class="sxs-lookup"><span data-stu-id="32763-188">**CounterInitialize**</span></span>](counterinitialize.md)
- [<span data-ttu-id="32763-189">*FreeMemory*</span><span class="sxs-lookup"><span data-stu-id="32763-189">*FreeMemory*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free)
- [<span data-ttu-id="32763-190">**Perfkreateingestance**</span><span class="sxs-lookup"><span data-stu-id="32763-190">**PerfCreateInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [<span data-ttu-id="32763-191">**Perfdecrementulongcountervalue**</span><span class="sxs-lookup"><span data-stu-id="32763-191">**PerfDecrementULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
- [<span data-ttu-id="32763-192">**Perfdecrementulonglongcountervalue**</span><span class="sxs-lookup"><span data-stu-id="32763-192">**PerfDecrementULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
- [<span data-ttu-id="32763-193">**Perfdelta eteinstance**</span><span class="sxs-lookup"><span data-stu-id="32763-193">**PerfDeleteInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [<span data-ttu-id="32763-194">**Perfinkrementulongcountervalue**</span><span class="sxs-lookup"><span data-stu-id="32763-194">**PerfIncrementULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
- [<span data-ttu-id="32763-195">**Perfinkrementulonglongcountervalue**</span><span class="sxs-lookup"><span data-stu-id="32763-195">**PerfIncrementULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)
- [<span data-ttu-id="32763-196">**Perfqueryinstance**</span><span class="sxs-lookup"><span data-stu-id="32763-196">**PerfQueryInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [<span data-ttu-id="32763-197">**Perfsetcountersetinfo**</span><span class="sxs-lookup"><span data-stu-id="32763-197">**PerfSetCounterSetInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [<span data-ttu-id="32763-198">**Perfsetulongcountervalue**</span><span class="sxs-lookup"><span data-stu-id="32763-198">**PerfSetULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [<span data-ttu-id="32763-199">**Perfsetulonglongcountervalue**</span><span class="sxs-lookup"><span data-stu-id="32763-199">**PerfSetULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [<span data-ttu-id="32763-200">**Perfsetcounterref-Wert**</span><span class="sxs-lookup"><span data-stu-id="32763-200">**PerfSetCounterRefValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [<span data-ttu-id="32763-201">**Perfstartprovider**</span><span class="sxs-lookup"><span data-stu-id="32763-201">**PerfStartProvider**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [<span data-ttu-id="32763-202">**Perfstartproviderex**</span><span class="sxs-lookup"><span data-stu-id="32763-202">**PerfStartProviderEx**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartproviderex)
- [<span data-ttu-id="32763-203">**Perfstopprovider**</span><span class="sxs-lookup"><span data-stu-id="32763-203">**PerfStopProvider**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

> [!Note]
> <span data-ttu-id="32763-204">Verwenden Sie zum Installieren und Deinstallieren von V2-Anbietern die Tools **Lodctr** und **unlodctr** .</span><span class="sxs-lookup"><span data-stu-id="32763-204">To install and uninstall V2 providers, use the **lodctr** and **unlodctr** tools.</span></span> <span data-ttu-id="32763-205">Die Funktionen **LoadPerfCounterTextStrings** und **unloadperfcountertextstrings** können nicht zum Installieren und Deinstallieren von V2-Anbietern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32763-205">The **LoadPerfCounterTextStrings** and **UnloadPerfCounterTextStrings** functions cannot be used to install and uninstall V2 providers.</span></span>

### <a name="performance-dll-functions"></a><span data-ttu-id="32763-206">Leistungs-DLL-Funktionen</span><span class="sxs-lookup"><span data-stu-id="32763-206">Performance DLL functions</span></span>

<span data-ttu-id="32763-207">[V1-Leistungsdaten Anbieter](providing-counter-data-using-a-performance-dll.md) implementieren eine DLL, die die folgenden Funktionen bereitstellt:</span><span class="sxs-lookup"><span data-stu-id="32763-207">[V1 performance data providers](providing-counter-data-using-a-performance-dll.md) implement a DLL that provides the following functions:</span></span>

- [<span data-ttu-id="32763-208">*ClosePerformanceData*</span><span class="sxs-lookup"><span data-stu-id="32763-208">*ClosePerformanceData*</span></span>](/windows/win32/api/winperf/nc-winperf-pm_close_proc)
- [<span data-ttu-id="32763-209">*CollectPerformanceData*</span><span class="sxs-lookup"><span data-stu-id="32763-209">*CollectPerformanceData*</span></span>](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)
- <span data-ttu-id="32763-210">[*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="32763-210">[*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))</span></span>

> [!Note]
> <span data-ttu-id="32763-211">Aufgrund erheblicher Leistungs-und Zuverlässigkeitsprobleme sind v1-Leistungsdaten Anbieter veraltet.</span><span class="sxs-lookup"><span data-stu-id="32763-211">Due to significant performance and reliability issues, V1 performance data providers are deprecated.</span></span> <span data-ttu-id="32763-212">Obwohl Sie weiterhin eine Leistungs Erweiterungs-DLL zum Bereitstellen von Leistungsdaten verwenden können, wird empfohlen, stattdessen [einen v2-Anbieter zu erstellen](providing-counter-data-using-version-2-0.md) .</span><span class="sxs-lookup"><span data-stu-id="32763-212">Although you still can use a performance extension DLL to provide counter data, you are encouraged to [create a V2 provider](providing-counter-data-using-version-2-0.md) instead.</span></span> <span data-ttu-id="32763-213">Außerdem wird empfohlen, vorhandene v1-Anbieter durch v2-Anbieter zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="32763-213">You also are encouraged to replace existing V1 providers with V2 providers.</span></span>

<span data-ttu-id="32763-214">V1-Anbieter können mithilfe der Tools **Lodctr** und **unlodctr** oder durch Aufrufen der folgenden Funktionen installiert und deinstalliert werden:</span><span class="sxs-lookup"><span data-stu-id="32763-214">V1 providers can be installed and uninstalled using the **lodctr** and **unlodctr** tools or by calling the following functions:</span></span>

- [<span data-ttu-id="32763-215">**LoadPerfCounterTextStrings**</span><span class="sxs-lookup"><span data-stu-id="32763-215">**LoadPerfCounterTextStrings**</span></span>](/windows/desktop/api/Loadperf/nf-loadperf-loadperfcountertextstringsa)
- [<span data-ttu-id="32763-216">**Unloadperfcountertextstrings**</span><span class="sxs-lookup"><span data-stu-id="32763-216">**UnloadPerfCounterTextStrings**</span></span>](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)
