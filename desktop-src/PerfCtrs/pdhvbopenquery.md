---
description: Die pdhvbopenquery-Funktion erstellt und Initialisiert eine eindeutige Abfrage Struktur, die verwendet wird, um die Erfassung von Leistungsdaten zu verwalten.
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: Pdhvbopenquery-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenQuery
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c657f033e2e972473218f2b283e03b11659d9f2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131677"
---
# <a name="pdhvbopenquery-function"></a><span data-ttu-id="bb6ac-103">Pdhvbopenquery-Funktion</span><span class="sxs-lookup"><span data-stu-id="bb6ac-103">PdhVbOpenQuery function</span></span>

<span data-ttu-id="bb6ac-104">Die **pdhvbopenquery** -Funktion erstellt und Initialisiert eine eindeutige Abfrage Struktur, die verwendet wird, um die Erfassung von Leistungsdaten zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-104">The **PdhVbOpenQuery** function creates and initializes a unique query structure that is used to manage the collection of performance data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bb6ac-105">Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="bb6ac-106">Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="bb6ac-107">Funktion "pdhvbopenquery" ( \_ ByVal queryhandle "Long" \_ )</span><span class="sxs-lookup"><span data-stu-id="bb6ac-107">Function PdhVbOpenQuery( \_ ByVal QueryHandle As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="bb6ac-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb6ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb6ac-109">*Queryhandle*</span><span class="sxs-lookup"><span data-stu-id="bb6ac-109">*QueryHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="bb6ac-110">Variable, die gelöscht wird (0 entspricht), bevor die Funktion aufgerufen wird, und, wenn die Funktion erfolgreich ist, enthält die eindeutige ID der erstellten und geöffneten Abfrage.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-110">Variable that is cleared (equals 0) before the function is called and, if the function is successful, contains the unique ID of the query that is created and opened.</span></span> <span data-ttu-id="bb6ac-111">Dieses Handle wird in den nachfolgenden Aufrufen anderer PDH-Funktionen verwendet, um die Abfrage zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-111">This handle is used in the subsequent calls to other PDH functions to identify the query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb6ac-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb6ac-112">Return value</span></span>

<span data-ttu-id="bb6ac-113">Wenn die Funktion erfolgreich ausgeführt wird, wird eine **lange** ganze Zahl zurückgegeben, \_ die der Fehler Erfolgs-und einem neuen Handle in der *queryhandle* -Variablen entspricht.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-113">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS and a new handle in the *QueryHandle* variable.</span></span>

<span data-ttu-id="bb6ac-114">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein [Systemfehler Code](/windows/desktop/Debug/system-error-codes) oder ein [PDH-Fehlercode](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bb6ac-114">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="bb6ac-115">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-115">The following are possible values.</span></span>



| <span data-ttu-id="bb6ac-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bb6ac-116">Return code</span></span>                                                                                                     | <span data-ttu-id="bb6ac-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb6ac-117">Description</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="bb6ac-118"><dt>**Ungültiges PDH- \_ \_ Argument**</dt></span><span class="sxs-lookup"><span data-stu-id="bb6ac-118"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="bb6ac-119">Das Argument ist ungültig oder falsch.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-119">The argument is invalid or incorrect.</span></span><br/>             |
| <dl> <span data-ttu-id="bb6ac-120"><dt>**PDH-Speicher Belegungs \_ \_ \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="bb6ac-120"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="bb6ac-121">Ein temporärer Speicherpuffer konnte nicht zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-121">A temporary memory buffer could not be allocated.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bb6ac-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb6ac-122">Requirements</span></span>



| <span data-ttu-id="bb6ac-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb6ac-123">Requirement</span></span> | <span data-ttu-id="bb6ac-124">Wert</span><span class="sxs-lookup"><span data-stu-id="bb6ac-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb6ac-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb6ac-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bb6ac-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb6ac-126">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb6ac-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb6ac-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bb6ac-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb6ac-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bb6ac-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bb6ac-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb6ac-130"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb6ac-130"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="bb6ac-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bb6ac-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb6ac-132"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb6ac-132"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb6ac-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb6ac-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb6ac-134">**Pdhclosequery**</span><span class="sxs-lookup"><span data-stu-id="bb6ac-134">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

