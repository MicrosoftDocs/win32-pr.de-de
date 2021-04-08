---
title: Tracelogging-Wrapper Makros
description: Listet die Wrapper Makros für tracelogging-Anbieter auf.
ms.assetid: 806F43F3-D376-4DBD-A4C5-B5F01E5D009D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc28b3a35074089b1f5c613b041534b8b282423
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714153"
---
# <a name="tracelogging-wrapper-macros"></a><span data-ttu-id="3c031-103">Tracelogging-Wrapper Makros</span><span class="sxs-lookup"><span data-stu-id="3c031-103">TraceLogging Wrapper Macros</span></span>

<span data-ttu-id="3c031-104">Listet die Wrapper Makros für tracelogging-Anbieter auf.</span><span class="sxs-lookup"><span data-stu-id="3c031-104">Lists the wrapper macros for TraceLogging providers.</span></span>

<span data-ttu-id="3c031-105">Um Ereignisse mit tracelogging-Anbietern aufzuzeichnen, müssen Sie die tracelogging-Schreib Makros [**traceloggingwrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) oder [**traceloggingschreiteactivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity)verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c031-105">In order to record events using TraceLogging providers, you need to use the TraceLogging write macros [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) or [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity).</span></span> <span data-ttu-id="3c031-106">Beide Makros erfordern, dass Sie alle Ereignisdaten in einem Wrapper Makro umschließen.</span><span class="sxs-lookup"><span data-stu-id="3c031-106">Both of these macros require you to wrap any event data in a wrapper macro.</span></span> <span data-ttu-id="3c031-107">Es gibt mehrere unterschiedliche Wrapper Makros für verschiedene Datentypen.</span><span class="sxs-lookup"><span data-stu-id="3c031-107">There are several different wrapper macros for different data types.</span></span> <span data-ttu-id="3c031-108">Eine komplette Liste der tracelogging-Makros finden Sie unter [tracelogging-Makros](trace-logging-macros.md).</span><span class="sxs-lookup"><span data-stu-id="3c031-108">For a complete list of TraceLogging macros, see [TraceLogging Macros](trace-logging-macros.md).</span></span>

<span data-ttu-id="3c031-109">Zusätzlich zu den obigen Wrapper Makros sind mehrere Makros für einzelne Datentypen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3c031-109">In addition to the wrapper macros above, several macros are available for individual data types.</span></span> <span data-ttu-id="3c031-110">Alle diese Makros haben das gleiche Format wie das [traceloggingvalue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) -Makro.</span><span class="sxs-lookup"><span data-stu-id="3c031-110">All of these macros have the same format as the [TraceLoggingValue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) macro.</span></span> <span data-ttu-id="3c031-111">Sie können das traceloggingvalue-Makro verwenden, um automatisch das entsprechende zu verwendende Wrapper Makro zu erkennen, oder Sie können das spezifische Makro direkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c031-111">You can use the TraceLoggingValue macro to automatically detect the appropriate wrapper macro to use, or use the specific macro directly.</span></span>

-   [<span data-ttu-id="3c031-112">**Traceloggingbinary**</span><span class="sxs-lookup"><span data-stu-id="3c031-112">**TraceLoggingBinary**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingbinary)
-   [<span data-ttu-id="3c031-113">**Traceloggingchannel**</span><span class="sxs-lookup"><span data-stu-id="3c031-113">**TraceLoggingChannel**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingchannel)
-   [<span data-ttu-id="3c031-114">**Traceloggingcustomattribute**</span><span class="sxs-lookup"><span data-stu-id="3c031-114">**TraceLoggingCustomAttribute**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingcustomattribute)
-   [<span data-ttu-id="3c031-115">**Traceloggingdescription**</span><span class="sxs-lookup"><span data-stu-id="3c031-115">**TraceLoggingDescription**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingdescription)
-   [<span data-ttu-id="3c031-116">**Traceloggingeventtag**</span><span class="sxs-lookup"><span data-stu-id="3c031-116">**TraceLoggingEventTag**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingeventtag)
-   [<span data-ttu-id="3c031-117">**Traceloggingschlüsselwort**</span><span class="sxs-lookup"><span data-stu-id="3c031-117">**TraceLoggingKeyword**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingkeyword)
-   [<span data-ttu-id="3c031-118">**Tracelogginglevel**</span><span class="sxs-lookup"><span data-stu-id="3c031-118">**TraceLoggingLevel**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogginglevel)
-   [<span data-ttu-id="3c031-119">**Traceloggingopcode**</span><span class="sxs-lookup"><span data-stu-id="3c031-119">**TraceLoggingOpcode**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingopcode)
-   [<span data-ttu-id="3c031-120">**Traceloggingsocketaddress**</span><span class="sxs-lookup"><span data-stu-id="3c031-120">**TraceLoggingSocketAddress**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingsocketaddress)
-   [<span data-ttu-id="3c031-121">**Traceloggingstruct**</span><span class="sxs-lookup"><span data-stu-id="3c031-121">**TraceLoggingStruct**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingstruct)
-   [<span data-ttu-id="3c031-122">**Traceloggingvalue**</span><span class="sxs-lookup"><span data-stu-id="3c031-122">**TraceLoggingValue**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue)

> [!Note]
>
> <span data-ttu-id="3c031-123">**Traceloggingoptiongroup** ist speziell für die Verwendung innerhalb des tracelogging- \_ \_ Anbieters definiert.</span><span class="sxs-lookup"><span data-stu-id="3c031-123">**TraceLoggingOptionGroup** is specifically for use inside of TRACELOGGING\_DEFINE\_PROVIDER.</span></span>
>
> -   [<span data-ttu-id="3c031-124">**Traceloggingoptiongroup**</span><span class="sxs-lookup"><span data-stu-id="3c031-124">**TraceLoggingOptionGroup**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup)

 

<span data-ttu-id="3c031-125">Im folgenden finden Sie die einzelnen Wrapper Makros.</span><span class="sxs-lookup"><span data-stu-id="3c031-125">Here are the individual wrapper macros.</span></span>

-   <span data-ttu-id="3c031-126">TraceLoggingInt8</span><span class="sxs-lookup"><span data-stu-id="3c031-126">TraceLoggingInt8</span></span>

-   <span data-ttu-id="3c031-127">TraceLoggingUInt8</span><span class="sxs-lookup"><span data-stu-id="3c031-127">TraceLoggingUInt8</span></span>

-   <span data-ttu-id="3c031-128">TraceLoggingInt16</span><span class="sxs-lookup"><span data-stu-id="3c031-128">TraceLoggingInt16</span></span>

-   <span data-ttu-id="3c031-129">TraceLoggingUInt16</span><span class="sxs-lookup"><span data-stu-id="3c031-129">TraceLoggingUInt16</span></span>

-   <span data-ttu-id="3c031-130">TraceLoggingInt32</span><span class="sxs-lookup"><span data-stu-id="3c031-130">TraceLoggingInt32</span></span>

-   <span data-ttu-id="3c031-131">TraceLoggingUInt32</span><span class="sxs-lookup"><span data-stu-id="3c031-131">TraceLoggingUInt32</span></span>

-   <span data-ttu-id="3c031-132">TraceLoggingInt64</span><span class="sxs-lookup"><span data-stu-id="3c031-132">TraceLoggingInt64</span></span>

-   <span data-ttu-id="3c031-133">TraceLoggingUInt64</span><span class="sxs-lookup"><span data-stu-id="3c031-133">TraceLoggingUInt64</span></span>

-   <span data-ttu-id="3c031-134">TraceLoggingFloat32</span><span class="sxs-lookup"><span data-stu-id="3c031-134">TraceLoggingFloat32</span></span>

-   <span data-ttu-id="3c031-135">TraceLoggingFloat64</span><span class="sxs-lookup"><span data-stu-id="3c031-135">TraceLoggingFloat64</span></span>

-   <span data-ttu-id="3c031-136">Traceloggingbool</span><span class="sxs-lookup"><span data-stu-id="3c031-136">TraceLoggingBool</span></span>

-   <span data-ttu-id="3c031-137">Traceloggingfiletime</span><span class="sxs-lookup"><span data-stu-id="3c031-137">TraceLoggingFileTime</span></span>

-   <span data-ttu-id="3c031-138">Traceloggingguid</span><span class="sxs-lookup"><span data-stu-id="3c031-138">TraceLoggingGuid</span></span>

-   <span data-ttu-id="3c031-139">Traceloggingpointer</span><span class="sxs-lookup"><span data-stu-id="3c031-139">TraceLoggingPointer</span></span>

-   <span data-ttu-id="3c031-140">Traceloggingsystemtime</span><span class="sxs-lookup"><span data-stu-id="3c031-140">TraceLoggingSystemTime</span></span>

-   <span data-ttu-id="3c031-141">TraceLoggingHexInt8</span><span class="sxs-lookup"><span data-stu-id="3c031-141">TraceLoggingHexInt8</span></span>

-   <span data-ttu-id="3c031-142">TraceLoggingHexUInt8</span><span class="sxs-lookup"><span data-stu-id="3c031-142">TraceLoggingHexUInt8</span></span>

-   <span data-ttu-id="3c031-143">TraceLoggingHexInt32</span><span class="sxs-lookup"><span data-stu-id="3c031-143">TraceLoggingHexInt32</span></span>

-   <span data-ttu-id="3c031-144">TraceLoggingHexUInt32</span><span class="sxs-lookup"><span data-stu-id="3c031-144">TraceLoggingHexUInt32</span></span>

-   <span data-ttu-id="3c031-145">TraceLoggingHexInt64</span><span class="sxs-lookup"><span data-stu-id="3c031-145">TraceLoggingHexInt64</span></span>

-   <span data-ttu-id="3c031-146">TraceLoggingHexUInt64</span><span class="sxs-lookup"><span data-stu-id="3c031-146">TraceLoggingHexUInt64</span></span>

-   <span data-ttu-id="3c031-147">Traceloggingwchar</span><span class="sxs-lookup"><span data-stu-id="3c031-147">TraceLoggingWchar</span></span>

-   <span data-ttu-id="3c031-148">Traceloggingchar</span><span class="sxs-lookup"><span data-stu-id="3c031-148">TraceLoggingChar</span></span>

-   <span data-ttu-id="3c031-149">Traceloggingintptr</span><span class="sxs-lookup"><span data-stu-id="3c031-149">TraceLoggingIntPtr</span></span>

-   <span data-ttu-id="3c031-150">Tracelogginguintptr</span><span class="sxs-lookup"><span data-stu-id="3c031-150">TraceLoggingUIntPtr</span></span>

-   <span data-ttu-id="3c031-151">Traceloggingboolean</span><span class="sxs-lookup"><span data-stu-id="3c031-151">TraceLoggingBoolean</span></span>

-   <span data-ttu-id="3c031-152">TraceLoggingHexInt16</span><span class="sxs-lookup"><span data-stu-id="3c031-152">TraceLoggingHexInt16</span></span>

-   <span data-ttu-id="3c031-153">TraceLoggingHexUInt16</span><span class="sxs-lookup"><span data-stu-id="3c031-153">TraceLoggingHexUInt16</span></span>

-   <span data-ttu-id="3c031-154">Traceloggingpid</span><span class="sxs-lookup"><span data-stu-id="3c031-154">TraceLoggingPid</span></span>

-   <span data-ttu-id="3c031-155">Traceloggingtid</span><span class="sxs-lookup"><span data-stu-id="3c031-155">TraceLoggingTid</span></span>

-   <span data-ttu-id="3c031-156">Traceloggingport</span><span class="sxs-lookup"><span data-stu-id="3c031-156">TraceLoggingPort</span></span>

-   <span data-ttu-id="3c031-157">Traceloggingwinerror</span><span class="sxs-lookup"><span data-stu-id="3c031-157">TraceLoggingWinError</span></span>

-   <span data-ttu-id="3c031-158">Traceloggingntstatus</span><span class="sxs-lookup"><span data-stu-id="3c031-158">TraceLoggingNTStatus</span></span>

-   <span data-ttu-id="3c031-159">Tracelogginghresult</span><span class="sxs-lookup"><span data-stu-id="3c031-159">TraceLoggingHResult</span></span>

-   <span data-ttu-id="3c031-160">Traceloggingsocketaddress</span><span class="sxs-lookup"><span data-stu-id="3c031-160">TraceLoggingSocketAddress</span></span>

-   <span data-ttu-id="3c031-161">Traceloggingsid</span><span class="sxs-lookup"><span data-stu-id="3c031-161">TraceLoggingSid</span></span>

-   <span data-ttu-id="3c031-162">Traceloggingstring</span><span class="sxs-lookup"><span data-stu-id="3c031-162">TraceLoggingString</span></span>

-   <span data-ttu-id="3c031-163">Traceloggingwidestring</span><span class="sxs-lookup"><span data-stu-id="3c031-163">TraceLoggingWideString</span></span>

-   <span data-ttu-id="3c031-164">Traceloggingzähltedstring</span><span class="sxs-lookup"><span data-stu-id="3c031-164">TraceLoggingCountedString</span></span>

-   <span data-ttu-id="3c031-165">Traceloggingzähltedwientstring</span><span class="sxs-lookup"><span data-stu-id="3c031-165">TraceLoggingCountedWideString</span></span>

-   <span data-ttu-id="3c031-166">Traceloggingansistring</span><span class="sxs-lookup"><span data-stu-id="3c031-166">TraceLoggingAnsiString</span></span>

-   <span data-ttu-id="3c031-167">Traceloggingunicodestring</span><span class="sxs-lookup"><span data-stu-id="3c031-167">TraceLoggingUnicodeString</span></span>

-   <span data-ttu-id="3c031-168">Traceloggingbinary (void- \* Daten, Größe der Daten in Bytes, \[ Optionaler \] Name) die Parameter für dieses Makro unterscheiden sich von den oben genannten.</span><span class="sxs-lookup"><span data-stu-id="3c031-168">TraceLoggingBinary(void \*data, size of the data in bytes, \[optional\] name ) The parameters to this macro differ from those above.</span></span> <span data-ttu-id="3c031-169">Wenn der *Name* -Parameter angegeben wird, muss es sich um ein Zeichenfolgenliteral (keine Variable) handeln, und es darf keine eingebetteten NULL-Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="3c031-169">If the *name* parameter is specified, it must be a string literal (not a variable) and may not contain any embedded null characters.</span></span> <span data-ttu-id="3c031-170">Wenn der *Name* -Parameter nicht angegeben wird, wird automatisch ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="3c031-170">If the *name* parameter is not provided, a name is generated automatically.</span></span>

<span data-ttu-id="3c031-171">Die tracelogging-API stellt auch mehrere Makros für Arrays zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3c031-171">The TraceLogging API also makes several macros available for arrays.</span></span> <span data-ttu-id="3c031-172">Diese Arrays können abhängig vom Wrapper Makro, das Sie verwenden möchten, entweder eine Fixed-Länge aufweisen oder eine Variable Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3c031-172">These arrays can either have a fixed length or be of a variable length, depending on the wrapper macro you choose to use.</span></span> <span data-ttu-id="3c031-173">Alle diese Wrapper Makros folgen diesem Format.</span><span class="sxs-lookup"><span data-stu-id="3c031-173">All of these wrapper macros follow this format.</span></span>

`TraceLoggingBooleanArray(pVals, cVals, name, desc, tags)`

<span data-ttu-id="3c031-174">Der Parameter *pvals* verweist auf das Daten *Array und gibt* die Anzahl der Elemente im Array an.</span><span class="sxs-lookup"><span data-stu-id="3c031-174">The parameter *pVals* points to the array of data and *cVals* indicates the number of elements in the array.</span></span> <span data-ttu-id="3c031-175">*cvals* müssen eine Konstante sein und dürfen keine Variable sein.</span><span class="sxs-lookup"><span data-stu-id="3c031-175">*cVals* must be a constant and cannot be a variable.</span></span> <span data-ttu-id="3c031-176">Wie bei den Einzelwert-Wrapper Makros sind *Name*, **DESC** und *Tags* optionale Parameter und müssen dieselben Einschränkungen einhalten wie das **traceloggingvalue** -Makro.</span><span class="sxs-lookup"><span data-stu-id="3c031-176">As with the single value wrapper macros, *name*, **desc**, and *tags* are optional parameters and must follow the same restrictions as explained with the **TraceLoggingValue** macro.</span></span>

-   <span data-ttu-id="3c031-177">TraceLoggingInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-177">TraceLoggingInt8FixedArray</span></span>

-   <span data-ttu-id="3c031-178">TraceLoggingUInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-178">TraceLoggingUInt8FixedArray</span></span>

-   <span data-ttu-id="3c031-179">TraceLoggingInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-179">TraceLoggingInt16FixedArray</span></span>

-   <span data-ttu-id="3c031-180">TraceLoggingUInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-180">TraceLoggingUInt16FixedArray</span></span>

-   <span data-ttu-id="3c031-181">TraceLoggingInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-181">TraceLoggingInt32FixedArray</span></span>

-   <span data-ttu-id="3c031-182">TraceLoggingUInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-182">TraceLoggingUInt32FixedArray</span></span>

-   <span data-ttu-id="3c031-183">TraceLoggingInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-183">TraceLoggingInt64FixedArray</span></span>

-   <span data-ttu-id="3c031-184">TraceLoggingUInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-184">TraceLoggingUInt64FixedArray</span></span>

-   <span data-ttu-id="3c031-185">TraceLoggingFloat32FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-185">TraceLoggingFloat32FixedArray</span></span>

-   <span data-ttu-id="3c031-186">TraceLoggingFloat64FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-186">TraceLoggingFloat64FixedArray</span></span>

-   <span data-ttu-id="3c031-187">Traceloggingboolfixedarray</span><span class="sxs-lookup"><span data-stu-id="3c031-187">TraceLoggingBoolFixedArray</span></span>

-   <span data-ttu-id="3c031-188">Traceloggingguidfixedarray</span><span class="sxs-lookup"><span data-stu-id="3c031-188">TraceLoggingGuidFixedArray</span></span>

-   <span data-ttu-id="3c031-189">Traceloggingpointerfixedarray</span><span class="sxs-lookup"><span data-stu-id="3c031-189">TraceLoggingPointerFixedArray</span></span>

-   <span data-ttu-id="3c031-190">Traceloggingfiletimefixedarray</span><span class="sxs-lookup"><span data-stu-id="3c031-190">TraceLoggingFileTimeFixedArray</span></span>

-   <span data-ttu-id="3c031-191">Traceloggingsystemtimefixedarray</span><span class="sxs-lookup"><span data-stu-id="3c031-191">TraceLoggingSystemTimeFixedArray</span></span>

-   <span data-ttu-id="3c031-192">TraceLoggingHexInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-192">TraceLoggingHexInt8FixedArray</span></span>

-   <span data-ttu-id="3c031-193">TraceLoggingHexUInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-193">TraceLoggingHexUInt8FixedArray</span></span>

-   <span data-ttu-id="3c031-194">TraceLoggingHexInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-194">TraceLoggingHexInt32FixedArray</span></span>

-   <span data-ttu-id="3c031-195">TraceLoggingHexUInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-195">TraceLoggingHexUInt32FixedArray</span></span>

-   <span data-ttu-id="3c031-196">TraceLoggingHexInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-196">TraceLoggingHexInt64FixedArray</span></span>

-   <span data-ttu-id="3c031-197">TraceLoggingHexUInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-197">TraceLoggingHexUInt64FixedArray</span></span>

-   <span data-ttu-id="3c031-198">Traceloggingwcharfixedarray</span><span class="sxs-lookup"><span data-stu-id="3c031-198">TraceLoggingWcharFixedArray</span></span>

-   <span data-ttu-id="3c031-199">Traceloggingcharfixedarray</span><span class="sxs-lookup"><span data-stu-id="3c031-199">TraceLoggingCharFixedArray</span></span>

-   <span data-ttu-id="3c031-200">Traceloggingintptrfixedarray</span><span class="sxs-lookup"><span data-stu-id="3c031-200">TraceLoggingIntPtrFixedArray</span></span>

-   <span data-ttu-id="3c031-201">Tracelogginguintptrfixedarray</span><span class="sxs-lookup"><span data-stu-id="3c031-201">TraceLoggingUIntPtrFixedArray</span></span>

-   <span data-ttu-id="3c031-202">Traceloggingbooleanfixedarray</span><span class="sxs-lookup"><span data-stu-id="3c031-202">TraceLoggingBooleanFixedArray</span></span>

-   <span data-ttu-id="3c031-203">TraceLoggingHexInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-203">TraceLoggingHexInt16FixedArray</span></span>

-   <span data-ttu-id="3c031-204">TraceLoggingHexUInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="3c031-204">TraceLoggingHexUInt16FixedArray</span></span>

-   <span data-ttu-id="3c031-205">TraceLoggingInt8Array</span><span class="sxs-lookup"><span data-stu-id="3c031-205">TraceLoggingInt8Array</span></span>

-   <span data-ttu-id="3c031-206">TraceLoggingUInt8Array</span><span class="sxs-lookup"><span data-stu-id="3c031-206">TraceLoggingUInt8Array</span></span>

-   <span data-ttu-id="3c031-207">TraceLoggingInt16Array</span><span class="sxs-lookup"><span data-stu-id="3c031-207">TraceLoggingInt16Array</span></span>

-   <span data-ttu-id="3c031-208">TraceLoggingUInt16Array</span><span class="sxs-lookup"><span data-stu-id="3c031-208">TraceLoggingUInt16Array</span></span>

-   <span data-ttu-id="3c031-209">TraceLoggingInt32Array</span><span class="sxs-lookup"><span data-stu-id="3c031-209">TraceLoggingInt32Array</span></span>

-   <span data-ttu-id="3c031-210">TraceLoggingUInt32Array</span><span class="sxs-lookup"><span data-stu-id="3c031-210">TraceLoggingUInt32Array</span></span>

-   <span data-ttu-id="3c031-211">TraceLoggingInt64Array</span><span class="sxs-lookup"><span data-stu-id="3c031-211">TraceLoggingInt64Array</span></span>

-   <span data-ttu-id="3c031-212">TraceLoggingUInt64Array</span><span class="sxs-lookup"><span data-stu-id="3c031-212">TraceLoggingUInt64Array</span></span>

-   <span data-ttu-id="3c031-213">TraceLoggingFloat32Array</span><span class="sxs-lookup"><span data-stu-id="3c031-213">TraceLoggingFloat32Array</span></span>

-   <span data-ttu-id="3c031-214">TraceLoggingFloat64Array</span><span class="sxs-lookup"><span data-stu-id="3c031-214">TraceLoggingFloat64Array</span></span>

-   <span data-ttu-id="3c031-215">Traceloggingboolarray</span><span class="sxs-lookup"><span data-stu-id="3c031-215">TraceLoggingBoolArray</span></span>

-   <span data-ttu-id="3c031-216">Traceloggingguidarray</span><span class="sxs-lookup"><span data-stu-id="3c031-216">TraceLoggingGuidArray</span></span>

-   <span data-ttu-id="3c031-217">Traceloggingpointerarray</span><span class="sxs-lookup"><span data-stu-id="3c031-217">TraceLoggingPointerArray</span></span>

-   <span data-ttu-id="3c031-218">Traceloggingfiletimearray</span><span class="sxs-lookup"><span data-stu-id="3c031-218">TraceLoggingFileTimeArray</span></span>

-   <span data-ttu-id="3c031-219">Traceloggingsystemtimearray</span><span class="sxs-lookup"><span data-stu-id="3c031-219">TraceLoggingSystemTimeArray</span></span>

-   <span data-ttu-id="3c031-220">TraceLoggingHexInt8Array</span><span class="sxs-lookup"><span data-stu-id="3c031-220">TraceLoggingHexInt8Array</span></span>

-   <span data-ttu-id="3c031-221">TraceLoggingHexUInt8Array</span><span class="sxs-lookup"><span data-stu-id="3c031-221">TraceLoggingHexUInt8Array</span></span>

-   <span data-ttu-id="3c031-222">TraceLoggingHexInt32Array</span><span class="sxs-lookup"><span data-stu-id="3c031-222">TraceLoggingHexInt32Array</span></span>

-   <span data-ttu-id="3c031-223">TraceLoggingHexUInt32Array</span><span class="sxs-lookup"><span data-stu-id="3c031-223">TraceLoggingHexUInt32Array</span></span>

-   <span data-ttu-id="3c031-224">TraceLoggingHexInt64Array</span><span class="sxs-lookup"><span data-stu-id="3c031-224">TraceLoggingHexInt64Array</span></span>

-   <span data-ttu-id="3c031-225">TraceLoggingHexUInt64Array</span><span class="sxs-lookup"><span data-stu-id="3c031-225">TraceLoggingHexUInt64Array</span></span>

-   <span data-ttu-id="3c031-226">Traceloggingwchararray</span><span class="sxs-lookup"><span data-stu-id="3c031-226">TraceLoggingWcharArray</span></span>

-   <span data-ttu-id="3c031-227">Traceloggingchararray</span><span class="sxs-lookup"><span data-stu-id="3c031-227">TraceLoggingCharArray</span></span>

-   <span data-ttu-id="3c031-228">Traceloggingintptrarray</span><span class="sxs-lookup"><span data-stu-id="3c031-228">TraceLoggingIntPtrArray</span></span>

-   <span data-ttu-id="3c031-229">Tracelogginguintptrarray</span><span class="sxs-lookup"><span data-stu-id="3c031-229">TraceLoggingUIntPtrArray</span></span>

-   <span data-ttu-id="3c031-230">Traceloggingbooleanarray</span><span class="sxs-lookup"><span data-stu-id="3c031-230">TraceLoggingBooleanArray</span></span>

-   <span data-ttu-id="3c031-231">TraceLoggingHexInt16Array</span><span class="sxs-lookup"><span data-stu-id="3c031-231">TraceLoggingHexInt16Array</span></span>

-   <span data-ttu-id="3c031-232">TraceLoggingHexUInt16Array</span><span class="sxs-lookup"><span data-stu-id="3c031-232">TraceLoggingHexUInt16Array</span></span>

 

 




