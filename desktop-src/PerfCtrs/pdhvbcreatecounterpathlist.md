---
description: Die pdhvbkreatecounterpathlist-Funktion zeigt das Dialogfeld zum Durchsuchen des Leistungsindikators an, mit dem der Benutzer mehrere Leistungsindikatoren auswählen kann. Jeder ausgewählte Indikator Pfad muss dann mithilfe der pdhvbgetcounterpathfromlist-Funktion gelesen werden.
ms.assetid: 8dda528f-2e06-4726-89a0-095781a2f80d
title: Pdhvbkreatecounterpathlist-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbCreateCounterPathList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: bef484846507bf68d8ccfc0ad3ea10a250b83133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865116"
---
# <a name="pdhvbcreatecounterpathlist-function"></a><span data-ttu-id="a5626-104">Pdhvbkreatecounterpathlist-Funktion</span><span class="sxs-lookup"><span data-stu-id="a5626-104">PdhVbCreateCounterPathList function</span></span>

<span data-ttu-id="a5626-105">Die **pdhvbkreatecounterpathlist** -Funktion zeigt das Dialogfeld zum Durchsuchen des Leistungsindikators an, mit dem der Benutzer mehrere Leistungsindikatoren auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="a5626-105">The **PdhVbCreateCounterPathList** function displays the performance counter browsing dialog box, which lets the user select several performance counters.</span></span> <span data-ttu-id="a5626-106">Jeder ausgewählte Indikator Pfad muss dann mithilfe der [**pdhvbgetcounterpathfromlist**](pdhvbgetcounterpathfromlist.md) -Funktion gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="a5626-106">Each selected counter path must then be read using the [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5626-107">Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="a5626-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="a5626-108">Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a5626-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="a5626-109">Function pdhvbkreatecounterpathlist ( \_ ByVal DetailLevel As Long, \_ ByVal captionstring As String \_ ) so lange</span><span class="sxs-lookup"><span data-stu-id="a5626-109">Function PdhVbCreateCounterPathList( \_ ByVal DetailLevel As Long, \_ ByVal CaptionString As String \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="a5626-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5626-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5626-111">*Detail Level*</span><span class="sxs-lookup"><span data-stu-id="a5626-111">*DetailLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="a5626-112">Typen von Leistungsindikatoren, die im Dialogfeld angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a5626-112">Types of counters to be displayed in the dialog box.</span></span> <span data-ttu-id="a5626-113">Verwenden Sie einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="a5626-113">Use one of the following values.</span></span>



| <span data-ttu-id="a5626-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a5626-114">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="a5626-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a5626-115">Meaning</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <span data-ttu-id="a5626-116"><dt>**Leistungs \_ Details \_ erweitert**</dt></span><span class="sxs-lookup"><span data-stu-id="a5626-116"><dt>**PERF\_DETAIL\_ADVANCED**</dt></span></span> </dl> | <span data-ttu-id="a5626-117">Leistungsindikatoren, die der Erweiterte Benutzer wahrscheinlich versteht, zusätzlich zu den Endbenutzer-Leistungsindikatoren.</span><span class="sxs-lookup"><span data-stu-id="a5626-117">Counters that the advanced user is likely to understand, in addition to the novice-user counters.</span></span><br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <span data-ttu-id="a5626-118"><dt>**Perf- \_ Detail \_ Experte**</dt></span><span class="sxs-lookup"><span data-stu-id="a5626-118"><dt>**PERF\_DETAIL\_EXPERT**</dt></span></span> </dl>       | <span data-ttu-id="a5626-119">Leistungsindikatoren für den Benutzer und den Softwareentwickler, zusätzlich zu den Leistungsindikatoren für die Anfänger und Fortgeschrittene.</span><span class="sxs-lookup"><span data-stu-id="a5626-119">Counters that the expert user and software developer is likely to understand, in addition to the counters for the novice and advanced users.</span></span><br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <span data-ttu-id="a5626-120"><dt>**Perf- \_ Detail- \_ Anfänger**</dt></span><span class="sxs-lookup"><span data-stu-id="a5626-120"><dt>**PERF\_DETAIL\_NOVICE**</dt></span></span> </dl>       | <span data-ttu-id="a5626-121">Nur Leistungsindikatoren, die der Anfänger wahrscheinlich versteht.</span><span class="sxs-lookup"><span data-stu-id="a5626-121">Only counters that the novice user is likely to understand.</span></span><br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <span data-ttu-id="a5626-122"><dt>**Perf- \_ Detail- \_ Assistent**</dt></span><span class="sxs-lookup"><span data-stu-id="a5626-122"><dt>**PERF\_DETAIL\_WIZARD**</dt></span></span> </dl>       | <span data-ttu-id="a5626-123">Alle Leistungsindikatoren im System.</span><span class="sxs-lookup"><span data-stu-id="a5626-123">All counters in the system.</span></span><br/>                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="a5626-124">*Captionstring*</span><span class="sxs-lookup"><span data-stu-id="a5626-124">*CaptionString*</span></span> 
</dt> <dd>

<span data-ttu-id="a5626-125">Zeichen folgen Variable, die den Text enthält, der auf der Beschriftungs Leiste des Dialog Felds angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a5626-125">String variable that contains the text that will be displayed in the caption bar of the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5626-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5626-126">Return value</span></span>

<span data-ttu-id="a5626-127">Die-Funktion gibt die Anzahl der gegen Pfade zurück, die vom Benutzer ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="a5626-127">The function returns the number of counter paths that the user selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5626-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5626-128">Requirements</span></span>



| <span data-ttu-id="a5626-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5626-129">Requirement</span></span> | <span data-ttu-id="a5626-130">Wert</span><span class="sxs-lookup"><span data-stu-id="a5626-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5626-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5626-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a5626-132">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5626-132">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a5626-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5626-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a5626-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5626-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a5626-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a5626-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5626-136"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5626-136"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="a5626-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a5626-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5626-138"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5626-138"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5626-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5626-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5626-140">**Pdhvbgetcounterpathelements**</span><span class="sxs-lookup"><span data-stu-id="a5626-140">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="a5626-141">**Pdhvbgetcounterpathfromlist**</span><span class="sxs-lookup"><span data-stu-id="a5626-141">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[<span data-ttu-id="a5626-142">**Pdhvbgetonecounterpath**</span><span class="sxs-lookup"><span data-stu-id="a5626-142">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




