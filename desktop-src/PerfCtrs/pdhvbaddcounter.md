---
description: Die pdhvbaddcounter-Funktion erstellt einen Counter-Eintrag im angegebenen Abfrageobjekt und gibt nach erfolgreichem Abschluss ein Handle für diesen Wert zurück.
ms.assetid: 20a9e6cd-bf0d-497d-b660-88e786e2f004
title: Pdhvbaddcounter-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbAddCounter
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 19f97abeec74af0d08f340b70aa139e1bec7bf1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347588"
---
# <a name="pdhvbaddcounter-function"></a><span data-ttu-id="35325-103">Pdhvbaddcounter-Funktion</span><span class="sxs-lookup"><span data-stu-id="35325-103">PdhVbAddCounter function</span></span>

<span data-ttu-id="35325-104">Die **pdhvbaddcounter** -Funktion erstellt einen Counter-Eintrag im angegebenen Abfrageobjekt und gibt nach erfolgreichem Abschluss ein Handle für diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="35325-104">The **PdhVbAddCounter** function creates a counter entry in the specified query object, and returns a handle to that counter upon successful completion.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35325-105">Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="35325-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="35325-106">Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="35325-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="35325-107">Funktion pdhvbaddcounter ( \_ ByVal queryhandle als Long, \_ ByVal counterpath As String, \_ ByVal counterhandle so Long \_ ) wie Long</span><span class="sxs-lookup"><span data-stu-id="35325-107">Function PdhVbAddCounter( \_ ByVal QueryHandle As Long, \_ ByVal CounterPath As String, \_ ByVal CounterHandle As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="35325-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="35325-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35325-109">*Queryhandle*</span><span class="sxs-lookup"><span data-stu-id="35325-109">*QueryHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="35325-110">Die ID der Abfrage, der dieser Counter zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="35325-110">ID of the query to which this counter is to be assigned.</span></span> <span data-ttu-id="35325-111">Dieser Wert wird von der [**pdhvbopenquery**](pdhvbopenquery.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="35325-111">This value is returned by the [**PdhVbOpenQuery**](pdhvbopenquery.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="35325-112">*CounterPath*</span><span class="sxs-lookup"><span data-stu-id="35325-112">*CounterPath*</span></span> 
</dt> <dd>

<span data-ttu-id="35325-113">Eine Text Zeichenfolge, die den Namen des der Abfrage hinzu zufügenden Zählers angibt.</span><span class="sxs-lookup"><span data-stu-id="35325-113">Text string that specifies the name of the counter path to add to the query.</span></span> <span data-ttu-id="35325-114">Der Inhalt dieser Zeichenfolge muss ein gültiger Counter-Pfad sein, der vom-gegen Browser oder von einer anderen Quelle abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="35325-114">The contents of this string must be a valid counter path, as obtained from the counter browser or other source.</span></span>

</dd> <dt>

<span data-ttu-id="35325-115">*Counter handle*</span><span class="sxs-lookup"><span data-stu-id="35325-115">*CounterHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="35325-116">Eindeutiger Verweis, der diesen Counter in der Abfrage identifiziert.</span><span class="sxs-lookup"><span data-stu-id="35325-116">Unique reference that identifies this counter in the query.</span></span> <span data-ttu-id="35325-117">Diese Variable muss mit 0 (null) initialisiert werden, bevor die-Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="35325-117">This variable must be initialized to zero before the function is called.</span></span> <span data-ttu-id="35325-118">Sie enthält einen gültigen Wert bei Rückgabe nur, wenn die Funktion erfolgreich abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="35325-118">It contains a valid value on return only if the function completes successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35325-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35325-119">Return value</span></span>

<span data-ttu-id="35325-120">Wenn die Funktion erfolgreich ausgeführt wird, wird eine **lange** ganze Zahl zurückgegeben, \_ die der Fehler Erfolgs-und einem neuen Handle in der *Counter handle* -Variablen entspricht.</span><span class="sxs-lookup"><span data-stu-id="35325-120">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS and a new handle in the *CounterHandle* variable.</span></span>

<span data-ttu-id="35325-121">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein [Systemfehler Code](/windows/desktop/Debug/system-error-codes) oder ein [PDH-Fehlercode](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="35325-121">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="35325-122">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="35325-122">The following are possible values.</span></span>



| <span data-ttu-id="35325-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="35325-123">Return code</span></span>                                                                                                     | <span data-ttu-id="35325-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35325-124">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="35325-125"><dt>**Ungültiges PDH- \_ \_ Argument**</dt></span><span class="sxs-lookup"><span data-stu-id="35325-125"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="35325-126">Mindestens eines der Argumente ist ungültig oder falsch.</span><span class="sxs-lookup"><span data-stu-id="35325-126">One or more of the arguments is invalid or incorrect.</span></span><br/>              |
| <dl> <span data-ttu-id="35325-127"><dt>**PDH-Speicher Belegungs \_ \_ \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="35325-127"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="35325-128">Ein Arbeitsspeicher Puffer konnte nicht zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="35325-128">A memory buffer could not be allocated.</span></span><br/>                            |
| <dl> <span data-ttu-id="35325-129"><dt>**Ungültiges PDH- \_ \_ handle**</dt></span><span class="sxs-lookup"><span data-stu-id="35325-129"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>             | <span data-ttu-id="35325-130">Das Abfrage Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="35325-130">The query handle is not valid.</span></span><br/>                                     |
| <dl> <span data-ttu-id="35325-131"><dt>**PDH \_ cstatus \_ kein \_ Counter**</dt></span><span class="sxs-lookup"><span data-stu-id="35325-131"><dt>**PDH\_CSTATUS\_NO\_COUNTER**</dt></span></span> </dl>        | <span data-ttu-id="35325-132">Der angegebene gegen Wert wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="35325-132">The specified counter was not found.</span></span><br/>                               |
| <dl> <span data-ttu-id="35325-133"><dt>**PDH \_ cstatus \_ No- \_ Objekt**</dt></span><span class="sxs-lookup"><span data-stu-id="35325-133"><dt>**PDH\_CSTATUS\_NO\_OBJECT**</dt></span></span> </dl>         | <span data-ttu-id="35325-134">Das angegebene Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="35325-134">The specified object could not be found.</span></span><br/>                           |
| <dl> <span data-ttu-id="35325-135"><dt>**PDH \_ cstatus \_ kein \_ Computer**</dt></span><span class="sxs-lookup"><span data-stu-id="35325-135"><dt>**PDH\_CSTATUS\_NO\_MACHINE**</dt></span></span> </dl>        | <span data-ttu-id="35325-136">Ein Computer Eintrag konnte nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="35325-136">A computer entry could not be created.</span></span><br/>                             |
| <dl> <span data-ttu-id="35325-137"><dt>**PDH \_ cstatus ungültiger \_ \_ counterName**</dt></span><span class="sxs-lookup"><span data-stu-id="35325-137"><dt>**PDH\_CSTATUS\_BAD\_COUNTERNAME**</dt></span></span> </dl>   | <span data-ttu-id="35325-138">Es wurde eine leere Zeichenfolge für den Namen des Counter-namens angegeben.</span><span class="sxs-lookup"><span data-stu-id="35325-138">An empty counter name path string was passed in.</span></span><br/>                   |
| <dl> <span data-ttu-id="35325-139"><dt>**PDH- \_ Funktion wurde \_ nicht \_ gefunden.**</dt></span><span class="sxs-lookup"><span data-stu-id="35325-139"><dt>**PDH\_FUNCTION\_NOT\_FOUND**</dt></span></span> </dl>        | <span data-ttu-id="35325-140">Die Berechnungsfunktion für diesen Counter konnte nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="35325-140">The calculation function for this counter could not be determined.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="35325-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35325-141">Requirements</span></span>



| <span data-ttu-id="35325-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35325-142">Requirement</span></span> | <span data-ttu-id="35325-143">Wert</span><span class="sxs-lookup"><span data-stu-id="35325-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35325-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35325-144">Minimum supported client</span></span><br/> | <span data-ttu-id="35325-145">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35325-145">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="35325-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35325-146">Minimum supported server</span></span><br/> | <span data-ttu-id="35325-147">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35325-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="35325-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="35325-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="35325-149"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35325-149"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="35325-150">DLL</span><span class="sxs-lookup"><span data-stu-id="35325-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35325-151"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35325-151"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35325-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35325-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35325-153">**Pdhvbopenquery**</span><span class="sxs-lookup"><span data-stu-id="35325-153">**PdhVbOpenQuery**</span></span>](pdhvbopenquery.md)
</dt> </dl>

 

