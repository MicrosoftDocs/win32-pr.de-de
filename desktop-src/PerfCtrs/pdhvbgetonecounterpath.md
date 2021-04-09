---
description: Die pdhvbgetonecounterpath-Funktion zeigt ein Dialogfeld an, in dem der Benutzer die verfügbaren Leistungsindikatoren durchsuchen und einen Indikator auswählen kann.
ms.assetid: a42406ef-70e0-464d-90f8-fef9e1c3471d
title: Pdhvbgetonecounterpath-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetOneCounterPath
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 980665372d49f483e3fb59b7571ec38fa9c2851a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865112"
---
# <a name="pdhvbgetonecounterpath-function"></a><span data-ttu-id="850da-103">Pdhvbgetonecounterpath-Funktion</span><span class="sxs-lookup"><span data-stu-id="850da-103">PdhVbGetOneCounterPath function</span></span>

<span data-ttu-id="850da-104">Die **pdhvbgetonecounterpath** -Funktion zeigt ein Dialogfeld an, in dem der Benutzer die verfügbaren Leistungsindikatoren durchsuchen und einen Indikator auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="850da-104">The **PdhVbGetOneCounterPath** function displays a dialog box that lets the user browse the available performance counters and select one counter.</span></span> <span data-ttu-id="850da-105">Der ausgewählte Wert wird in der *PathString* -Variablen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="850da-105">The counter selected is returned in the *PathString* variable.</span></span> <span data-ttu-id="850da-106">Die *PathString* -Variable muss dimensioniert und initialisiert werden, bevor diese Funktion aufgerufen wird, und die dimensionierte Größe muss von der *pathLength* -Variablen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="850da-106">The *PathString* variable must be dimensioned and initialized before this function is called, and the dimensioned size must be indicated by the *PathLength* variable.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="850da-107">Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="850da-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="850da-108">Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="850da-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="850da-109">Funktion pdhvbgetonecounterpath ( \_ ByVal PathString As String, \_ ByVal pathLength As Long, \_ ByVal DetailLevel As Long, \_ ByVal captionstring As String \_ ) so lange</span><span class="sxs-lookup"><span data-stu-id="850da-109">Function PdhVbGetOneCounterPath( \_ ByVal PathString As String, \_ ByVal PathLength As Long, \_ ByVal DetailLevel As Long, \_ ByVal CaptionString As String \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="850da-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="850da-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="850da-111">*PathString*</span><span class="sxs-lookup"><span data-stu-id="850da-111">*PathString*</span></span> 
</dt> <dd>

<span data-ttu-id="850da-112">Initialisierte Zeichen folgen Variable, die verwendet wird, um den vom Benutzer ausgewählten Counter-Pfad zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="850da-112">Initialized string variable used to receive the counter path selected by the user.</span></span>

</dd> <dt>

<span data-ttu-id="850da-113">*PathLength*</span><span class="sxs-lookup"><span data-stu-id="850da-113">*PathLength*</span></span> 
</dt> <dd>

<span data-ttu-id="850da-114">Länge der initialisierten PathString.</span><span class="sxs-lookup"><span data-stu-id="850da-114">Length of the initialized PathString.</span></span>

</dd> <dt>

<span data-ttu-id="850da-115">*Detail Level*</span><span class="sxs-lookup"><span data-stu-id="850da-115">*DetailLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="850da-116">Typen von Leistungsindikatoren, die im Dialogfeld angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="850da-116">Types of counters to be displayed in the dialog box.</span></span> <span data-ttu-id="850da-117">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="850da-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="850da-118">Wert</span><span class="sxs-lookup"><span data-stu-id="850da-118">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="850da-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="850da-119">Meaning</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <span data-ttu-id="850da-120"><dt>**Leistungs \_ Details \_ erweitert**</dt></span><span class="sxs-lookup"><span data-stu-id="850da-120"><dt>**PERF\_DETAIL\_ADVANCED**</dt></span></span> </dl> | <span data-ttu-id="850da-121">Leistungsindikatoren, die der Erweiterte Benutzer wahrscheinlich versteht, zusätzlich zu den Endbenutzer-Leistungsindikatoren.</span><span class="sxs-lookup"><span data-stu-id="850da-121">Counters that the advanced user is likely to understand, in addition to the novice-user counters.</span></span><br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <span data-ttu-id="850da-122"><dt>**Perf- \_ Detail \_ Experte**</dt></span><span class="sxs-lookup"><span data-stu-id="850da-122"><dt>**PERF\_DETAIL\_EXPERT**</dt></span></span> </dl>       | <span data-ttu-id="850da-123">Leistungsindikatoren für den Benutzer und den Softwareentwickler, zusätzlich zu den Leistungsindikatoren für die Anfänger und Fortgeschrittene.</span><span class="sxs-lookup"><span data-stu-id="850da-123">Counters that the expert user and software developer is likely to understand, in addition to the counters for the novice and advanced users.</span></span><br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <span data-ttu-id="850da-124"><dt>**Perf- \_ Detail- \_ Anfänger**</dt></span><span class="sxs-lookup"><span data-stu-id="850da-124"><dt>**PERF\_DETAIL\_NOVICE**</dt></span></span> </dl>       | <span data-ttu-id="850da-125">Nur Leistungsindikatoren, die der Anfänger wahrscheinlich versteht.</span><span class="sxs-lookup"><span data-stu-id="850da-125">Only counters that the novice user is likely to understand.</span></span><br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <span data-ttu-id="850da-126"><dt>**Perf- \_ Detail- \_ Assistent**</dt></span><span class="sxs-lookup"><span data-stu-id="850da-126"><dt>**PERF\_DETAIL\_WIZARD**</dt></span></span> </dl>       | <span data-ttu-id="850da-127">Alle Leistungsindikatoren im System.</span><span class="sxs-lookup"><span data-stu-id="850da-127">All counters in the system.</span></span><br/>                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="850da-128">*Captionstring*</span><span class="sxs-lookup"><span data-stu-id="850da-128">*CaptionString*</span></span> 
</dt> <dd>

<span data-ttu-id="850da-129">Zeichen folgen Variable, die den Text enthält, der auf der Beschriftungs Leiste des Dialog Felds angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="850da-129">String variable that contains the text that will be displayed in the caption bar of the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="850da-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="850da-130">Return value</span></span>

<span data-ttu-id="850da-131">Die-Funktion gibt die Anzahl der Zeichen zurück, die in den *PathString* -Puffer geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="850da-131">The function returns the number of characters written to the *PathString* buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="850da-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="850da-132">Requirements</span></span>



| <span data-ttu-id="850da-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="850da-133">Requirement</span></span> | <span data-ttu-id="850da-134">Wert</span><span class="sxs-lookup"><span data-stu-id="850da-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="850da-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="850da-135">Minimum supported client</span></span><br/> | <span data-ttu-id="850da-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="850da-136">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="850da-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="850da-137">Minimum supported server</span></span><br/> | <span data-ttu-id="850da-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="850da-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="850da-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="850da-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="850da-140"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="850da-140"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="850da-141">DLL</span><span class="sxs-lookup"><span data-stu-id="850da-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="850da-142"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="850da-142"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="850da-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="850da-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="850da-144">**Pdhvbkreatecounterpathlist**</span><span class="sxs-lookup"><span data-stu-id="850da-144">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="850da-145">**Pdhvbgetcounterpathelements**</span><span class="sxs-lookup"><span data-stu-id="850da-145">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="850da-146">**Pdhvbgetcounterpathfromlist**</span><span class="sxs-lookup"><span data-stu-id="850da-146">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> </dl>

 

 




