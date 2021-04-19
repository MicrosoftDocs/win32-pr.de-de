---
description: Diese Funktion beendet das aufrufende Programm, wenn es in einer Lade Programm Legende aufgerufen wird. Andernfalls hat Sie keine Auswirkung.
ms.assetid: 5C10BF04-B7C7-4481-A184-FDD418FE5F52
title: Ldrfastfailinloadercallout-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrFastFailInLoaderCallout
api_type:
- DllExport
api_location:
- NTDll.dll
ms.openlocfilehash: f74b9cdc0aec666242a8267fab8d6255c75dc94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373603"
---
# <a name="ldrfastfailinloadercallout-function"></a><span data-ttu-id="256e4-104">Ldrfastfailinloadercallout-Funktion</span><span class="sxs-lookup"><span data-stu-id="256e4-104">LdrFastFailInLoaderCallout function</span></span>

<span data-ttu-id="256e4-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="256e4-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="256e4-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="256e4-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="256e4-107">Diese Funktion beendet das aufrufende Programm, wenn es in einer Lade Programm Legende aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="256e4-107">This function forcefully terminates the calling program if it is invoked inside a loader callout.</span></span> <span data-ttu-id="256e4-108">Andernfalls hat Sie keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="256e4-108">Otherwise, it has no effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="256e4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="256e4-109">Syntax</span></span>


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a><span data-ttu-id="256e4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="256e4-110">Parameters</span></span>

<span data-ttu-id="256e4-111">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="256e4-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="256e4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="256e4-112">Return value</span></span>

<span data-ttu-id="256e4-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="256e4-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="256e4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="256e4-114">Remarks</span></span>

<span data-ttu-id="256e4-115">Diese Routine fängt nicht alle potenziellen deadlockfälle ab. Es ist möglich, dass ein Thread innerhalb eines Lade Programmen eine Sperre erhält, während ein Thread außerhalb einer Lade Modul Legende die gleiche Sperre besitzt und einen Aufruf an das Lade Modul durchführt.</span><span class="sxs-lookup"><span data-stu-id="256e4-115">This routine does not catch all potential deadlock cases; it is possible for a thread inside a loader callout to acquire a lock while some thread outside a loader callout holds the same lock and makes a call into the loader.</span></span> <span data-ttu-id="256e4-116">Anders ausgedrückt: zwischen der Loadersperre und einer Client Sperre kann eine Sperr Reihenfolge-Inversion vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="256e4-116">In other words, there can be a lock order inversion between the loader lock and a client lock.</span></span>

## <a name="requirements"></a><span data-ttu-id="256e4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="256e4-117">Requirements</span></span>



| <span data-ttu-id="256e4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="256e4-118">Requirement</span></span> | <span data-ttu-id="256e4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="256e4-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="256e4-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="256e4-120">Library</span></span><br/> | <dl> <span data-ttu-id="256e4-121"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="256e4-121"><dt>NTDll.lib</dt></span></span> </dl> |
| <span data-ttu-id="256e4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="256e4-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="256e4-123"><dt>NTDll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="256e4-123"><dt>NTDll.dll</dt></span></span> </dl> |



 

 




