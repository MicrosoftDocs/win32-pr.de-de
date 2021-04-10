---
title: ADSI-Funktionen
description: Active Directory Dienst Schnittstellen machen Clients die folgenden Hilfsfunktionen verfügbar, die keine Automatisierung verwenden.
ms.assetid: 4f0e90e2-afcc-4cf7-a731-9b38a83ca229
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Reference, Functions
- Funktions-ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c814cf4f59a391a3242fa748856eaacb35dbcc53
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309263"
---
# <a name="adsi-functions"></a><span data-ttu-id="126a1-105">ADSI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="126a1-105">ADSI Functions</span></span>

<span data-ttu-id="126a1-106">Active Directory Dienst Schnittstellen machen Clients die folgenden Hilfsfunktionen verfügbar, die keine Automatisierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="126a1-106">Active Directory Service Interfaces expose the following helper functions to clients that do not use Automation.</span></span>



| <span data-ttu-id="126a1-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="126a1-107">Function</span></span>                                           | <span data-ttu-id="126a1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="126a1-108">Description</span></span>                                                                                        |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="126a1-109">**Adsbuildenzuerator**</span><span class="sxs-lookup"><span data-stu-id="126a1-109">**ADsBuildEnumerator**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)   | <span data-ttu-id="126a1-110">Erstellt ein Enumeratorobjekt für das angegebene ADSI-Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="126a1-110">Creates an enumerator object for the specified ADSI container object.</span></span>                              |
| [<span data-ttu-id="126a1-111">**Adsbuildvararrayint**</span><span class="sxs-lookup"><span data-stu-id="126a1-111">**ADsBuildVarArrayInt**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararrayint) | <span data-ttu-id="126a1-112">Erstellt ein Variant-Array aus einem Array von **DWORD** s.</span><span class="sxs-lookup"><span data-stu-id="126a1-112">Builds a variant array from an array of **DWORD** s.</span></span>                                                |
| [<span data-ttu-id="126a1-113">**Adsbuildvararraystr**</span><span class="sxs-lookup"><span data-stu-id="126a1-113">**ADsBuildVarArrayStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararraystr) | <span data-ttu-id="126a1-114">Erstellt ein Variant-Array aus einem Array von Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="126a1-114">Builds a variant array from an array of Unicode strings.</span></span>                                           |
| [<span data-ttu-id="126a1-115">**ADsEncodeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="126a1-115">**ADsEncodeBinaryData**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) | <span data-ttu-id="126a1-116">Konvertiert ein BLOB von Binärdaten in das Format, das für einen Suchfilter geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="126a1-116">Converts a blob of binary data to the format suitable for a search filter.</span></span>                         |
| [<span data-ttu-id="126a1-117">**Adsenzueratenext**</span><span class="sxs-lookup"><span data-stu-id="126a1-117">**ADsEnumerateNext**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)       | <span data-ttu-id="126a1-118">Füllt ein Variant-Array mit Elementen, die aus dem angegebenen Enumeratorobjekt abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="126a1-118">Populates a variant array with elements retrieved from the specified enumerator object.</span></span>            |
| [<span data-ttu-id="126a1-119">**Adsfreenumerator**</span><span class="sxs-lookup"><span data-stu-id="126a1-119">**ADsFreeEnumerator**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)     | <span data-ttu-id="126a1-120">Gibt ein zuvor von [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)erstelltes Enumeratorobjekt frei.</span><span class="sxs-lookup"><span data-stu-id="126a1-120">Frees an enumerator object previously created by [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator).</span></span> |
| [<span data-ttu-id="126a1-121">**Adsgetlasterror**</span><span class="sxs-lookup"><span data-stu-id="126a1-121">**ADsGetLastError**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror)         | <span data-ttu-id="126a1-122">Ruft den letzten Fehler Codewert des aufrufenden Threads ab.</span><span class="sxs-lookup"><span data-stu-id="126a1-122">Retrieves the last error code value of the calling thread.</span></span>                                         |
| [<span data-ttu-id="126a1-123">**ADsGetObject**</span><span class="sxs-lookup"><span data-stu-id="126a1-123">**ADsGetObject**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)               | <span data-ttu-id="126a1-124">Bindet mithilfe der aktuellen Anmelde Informationen an ein ADSI-Objekt.</span><span class="sxs-lookup"><span data-stu-id="126a1-124">Binds to an ADSI object using the current credentials.</span></span>                                             |
| [<span data-ttu-id="126a1-125">**ADsOpenObject**</span><span class="sxs-lookup"><span data-stu-id="126a1-125">**ADsOpenObject**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)             | <span data-ttu-id="126a1-126">Bindet mithilfe der angegebenen Anmelde Informationen an ein ADSI-Objekt.</span><span class="sxs-lookup"><span data-stu-id="126a1-126">Binds to an ADSI object using specified credentials</span></span>                                                |
| [<span data-ttu-id="126a1-127">**Adssetlasterror**</span><span class="sxs-lookup"><span data-stu-id="126a1-127">**ADsSetLastError**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adssetlasterror)         | <span data-ttu-id="126a1-128">Legt den Fehler Codewert des aufrufenden Threads fest.</span><span class="sxs-lookup"><span data-stu-id="126a1-128">Sets the error code value of the calling thread.</span></span>                                                   |
| [<span data-ttu-id="126a1-129">**Zuordnung**</span><span class="sxs-lookup"><span data-stu-id="126a1-129">**AllocADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)                 | <span data-ttu-id="126a1-130">Belegt einen Speicherblock.</span><span class="sxs-lookup"><span data-stu-id="126a1-130">Allocates a block of memory.</span></span>                                                                       |
| [<span data-ttu-id="126a1-131">**Zuordnung**</span><span class="sxs-lookup"><span data-stu-id="126a1-131">**AllocADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-allocadsstr)                 | <span data-ttu-id="126a1-132">Ordnet Speicher für eine angegebene Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="126a1-132">Allocates memory for a given string.</span></span>                                                               |
| [<span data-ttu-id="126a1-133">**Freiadsmem**</span><span class="sxs-lookup"><span data-stu-id="126a1-133">**FreeADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)                   | <span data-ttu-id="126a1-134">Gibt den von " [**zuordneter**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)" zugewiesenen Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="126a1-134">Frees the memory allocated by [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).</span></span>                                  |
| [<span data-ttu-id="126a1-135">**Freiadsstr**</span><span class="sxs-lookup"><span data-stu-id="126a1-135">**FreeADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-freeadsstr)                   | <span data-ttu-id="126a1-136">Gibt den für die angegebene Zeichenfolge zugeordneten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="126a1-136">Frees the memory allocated for the given string.</span></span>                                                   |
| [<span data-ttu-id="126a1-137">**Rezuweisung**</span><span class="sxs-lookup"><span data-stu-id="126a1-137">**ReallocADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsmem)             | <span data-ttu-id="126a1-138">Weist den vorhandenen Speicherinhalt einem neu erstellten Speicherort zu.</span><span class="sxs-lookup"><span data-stu-id="126a1-138">Assigns the existing memory content to a newly created memory location.</span></span>                            |
| [<span data-ttu-id="126a1-139">**Rezuweisung**</span><span class="sxs-lookup"><span data-stu-id="126a1-139">**ReallocADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsstr)             | <span data-ttu-id="126a1-140">Ersetzt eine vorhandene Zeichenfolge durch eine neue.</span><span class="sxs-lookup"><span data-stu-id="126a1-140">Replaces an existing string with a new one.</span></span>                                                        |



 

<span data-ttu-id="126a1-141">Die folgenden ADSI-Funktionen sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="126a1-141">The following ADSI functions are obsolete.</span></span>



| <span data-ttu-id="126a1-142">Funktion</span><span class="sxs-lookup"><span data-stu-id="126a1-142">Function</span></span>                                                  | <span data-ttu-id="126a1-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="126a1-143">Description</span></span> |
|-----------------------------------------------------------|-------------|
| [<span data-ttu-id="126a1-144">**Adsfreallerrorrecords**</span><span class="sxs-lookup"><span data-stu-id="126a1-144">**AdsFreeAllErrorRecords**</span></span>](obsolete-adsi-functions.md) | <span data-ttu-id="126a1-145">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="126a1-145">Obsolete.</span></span>   |
| [<span data-ttu-id="126a1-146">**Adsdecodebinarydata**</span><span class="sxs-lookup"><span data-stu-id="126a1-146">**AdsDecodeBinaryData**</span></span>](obsolete-adsi-functions.md)    | <span data-ttu-id="126a1-147">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="126a1-147">Obsolete.</span></span>   |
| [<span data-ttu-id="126a1-148">**Propvarianttadstype**</span><span class="sxs-lookup"><span data-stu-id="126a1-148">**PropVariantToAdsType**</span></span>](obsolete-adsi-functions.md)   | <span data-ttu-id="126a1-149">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="126a1-149">Obsolete.</span></span>   |
| [<span data-ttu-id="126a1-150">**Adstypintopropvariant**</span><span class="sxs-lookup"><span data-stu-id="126a1-150">**AdsTypeToPropVariant**</span></span>](obsolete-adsi-functions.md)   | <span data-ttu-id="126a1-151">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="126a1-151">Obsolete.</span></span>   |
| [<span data-ttu-id="126a1-152">**Adsfreadsvalues**</span><span class="sxs-lookup"><span data-stu-id="126a1-152">**AdsFreeAdsValues**</span></span>](obsolete-adsi-functions.md)       | <span data-ttu-id="126a1-153">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="126a1-153">Obsolete.</span></span>   |
| [<span data-ttu-id="126a1-154">**Initadsmem**</span><span class="sxs-lookup"><span data-stu-id="126a1-154">**InitAdsMem**</span></span>](obsolete-adsi-functions.md)             | <span data-ttu-id="126a1-155">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="126a1-155">Obsolete.</span></span>   |
| [<span data-ttu-id="126a1-156">**Assertadsmemlecks**</span><span class="sxs-lookup"><span data-stu-id="126a1-156">**AssertAdsmemLeaks**</span></span>](obsolete-adsi-functions.md)      | <span data-ttu-id="126a1-157">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="126a1-157">Obsolete.</span></span>   |
| [<span data-ttu-id="126a1-158">**Dumpmemorytracker**</span><span class="sxs-lookup"><span data-stu-id="126a1-158">**DumpMemorytracker**</span></span>](obsolete-adsi-functions.md)      | <span data-ttu-id="126a1-159">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="126a1-159">Obsolete.</span></span>   |



 

 

 




