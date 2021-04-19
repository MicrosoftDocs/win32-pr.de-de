---
description: Die pdhvbgetcounterpathelements-Funktion analysiert eine voll qualifizierte Zeichenfolge für den Leistungsindikator Pfad in die einzelnen Elemente.
ms.assetid: 5459c7dd-e8b6-48cd-a33f-cafdc64dd9ee
title: Pdhvbgetcounterpathelements-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathElements
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 003374141b0454d730ba4b844715bd6f00b544da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368748"
---
# <a name="pdhvbgetcounterpathelements-function"></a><span data-ttu-id="c3eda-103">Pdhvbgetcounterpathelements-Funktion</span><span class="sxs-lookup"><span data-stu-id="c3eda-103">PdhVbGetCounterPathElements function</span></span>

<span data-ttu-id="c3eda-104">Die **pdhvbgetcounterpathelements** -Funktion analysiert eine voll qualifizierte Zeichenfolge für den Leistungsindikator Pfad in die einzelnen Elemente.</span><span class="sxs-lookup"><span data-stu-id="c3eda-104">The **PdhVbGetCounterPathElements** function parses a fully qualified performance counter path string into its individual elements.</span></span> <span data-ttu-id="c3eda-105">Jede der Zeichen folgen Variablen muss dieselbe Größe aufweisen (*bufferSize*) und dimensioniert und initialisiert werden, bevor Sie in dieser Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3eda-105">Each of the string variables must be the same size (*BufferSize*) and dimensioned and initialized before it is used in this function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3eda-106">Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="c3eda-106">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="c3eda-107">Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c3eda-107">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="c3eda-108">Funktion pdhvbgetcounterpathelements ( \_ ByVal PathString As String, \_ ByVal MachineName As String, \_ ByVal ObjectName As String, \_ ByVal instanceName As String, \_ ByVal Parameter instance As String, \_ ByVal CounterName As String, \_ ByVal BufferSize As Long \_ )</span><span class="sxs-lookup"><span data-stu-id="c3eda-108">Function PdhVbGetCounterPathElements( \_ ByVal PathString As String, \_ ByVal MachineName As String, \_ ByVal ObjectName As String, \_ ByVal InstanceName As String, \_ ByVal ParentInstance As String, \_ ByVal CounterName As String, \_ ByVal BufferSize As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="c3eda-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3eda-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3eda-110">*PathString*</span><span class="sxs-lookup"><span data-stu-id="c3eda-110">*PathString*</span></span> 
</dt> <dd>

<span data-ttu-id="c3eda-111">Die Zeichenfolge für den Counter-Pfad, die in die einzelnen Elemente aufgeteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3eda-111">Counter path string that is to be broken up into its individual elements.</span></span>

</dd> <dt>

<span data-ttu-id="c3eda-112">*MachineName*</span><span class="sxs-lookup"><span data-stu-id="c3eda-112">*MachineName*</span></span> 
</dt> <dd>

<span data-ttu-id="c3eda-113">Zeichenfolge, die den Computernamen empfängt.</span><span class="sxs-lookup"><span data-stu-id="c3eda-113">String to receive the computer name.</span></span>

</dd> <dt>

<span data-ttu-id="c3eda-114">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="c3eda-114">*ObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="c3eda-115">Zeichenfolge, die den Objektnamen empfängt.</span><span class="sxs-lookup"><span data-stu-id="c3eda-115">String to receive the object name.</span></span>

</dd> <dt>

<span data-ttu-id="c3eda-116">*InstanceName*</span><span class="sxs-lookup"><span data-stu-id="c3eda-116">*InstanceName*</span></span> 
</dt> <dd>

<span data-ttu-id="c3eda-117">Zeichenfolge, die den Instanznamen empfängt, falls verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3eda-117">String to receive the instance name, if used.</span></span>

</dd> <dt>

<span data-ttu-id="c3eda-118">*Parametriinstance*</span><span class="sxs-lookup"><span data-stu-id="c3eda-118">*ParentInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="c3eda-119">Zeichenfolge, die die übergeordnete Instanz empfängt, sofern Sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3eda-119">String to receive the parent instance, if used.</span></span>

</dd> <dt>

<span data-ttu-id="c3eda-120">*CounterName*</span><span class="sxs-lookup"><span data-stu-id="c3eda-120">*CounterName*</span></span> 
</dt> <dd>

<span data-ttu-id="c3eda-121">Zeichenfolge, die den Namen des Zählers empfängt.</span><span class="sxs-lookup"><span data-stu-id="c3eda-121">String to receive the counter name.</span></span>

</dd> <dt>

<span data-ttu-id="c3eda-122">*BufferSize*</span><span class="sxs-lookup"><span data-stu-id="c3eda-122">*BufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="c3eda-123">Maximale Größe der einzelnen Zeichen folgen Variablen, die als Parameter für diesen Funktions Aufrufsatz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3eda-123">Maximum size of each string variable used as a parameter to this function call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3eda-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3eda-124">Return value</span></span>

<span data-ttu-id="c3eda-125">Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie eine **Long** -Ganzzahl zurück, die dem Fehler \_ Erfolg entspricht.</span><span class="sxs-lookup"><span data-stu-id="c3eda-125">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS.</span></span>

<span data-ttu-id="c3eda-126">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein [Systemfehler Code](/windows/desktop/Debug/system-error-codes) oder ein [PDH-Fehlercode](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c3eda-126">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="c3eda-127">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="c3eda-127">The following are possible values.</span></span>



| <span data-ttu-id="c3eda-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c3eda-128">Return code</span></span>                                                                                                     | <span data-ttu-id="c3eda-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3eda-129">Description</span></span>                                                                                    |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c3eda-130"><dt>**Ungültiges PDH- \_ \_ Argument**</dt></span><span class="sxs-lookup"><span data-stu-id="c3eda-130"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="c3eda-131">Mindestens ein Zeichen folgen Puffer weist nicht die richtige Größe auf.</span><span class="sxs-lookup"><span data-stu-id="c3eda-131">One or more of the string buffers is not the correct size.</span></span><br/>                          |
| <dl> <span data-ttu-id="c3eda-132"><dt>**PDH \_ Weitere \_ Daten**</dt></span><span class="sxs-lookup"><span data-stu-id="c3eda-132"><dt>**PDH\_MORE\_DATA**</dt></span></span> </dl>                  | <span data-ttu-id="c3eda-133">Mindestens eines der Counter-Pfad Elemente ist zu groß für die Rückgabe Pufferlänge.</span><span class="sxs-lookup"><span data-stu-id="c3eda-133">One or more of the counter path elements is too large for the return buffer length.</span></span><br/> |
| <dl> <span data-ttu-id="c3eda-134"><dt>**PDH-Speicher Belegungs \_ \_ \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="c3eda-134"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="c3eda-135">Ein temporärer Speicherpuffer konnte nicht zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="c3eda-135">A temporary memory buffer could not be allocated.</span></span><br/>                                   |



 

## <a name="requirements"></a><span data-ttu-id="c3eda-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3eda-136">Requirements</span></span>



| <span data-ttu-id="c3eda-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3eda-137">Requirement</span></span> | <span data-ttu-id="c3eda-138">Wert</span><span class="sxs-lookup"><span data-stu-id="c3eda-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3eda-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3eda-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c3eda-140">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3eda-140">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3eda-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3eda-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c3eda-142">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3eda-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c3eda-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c3eda-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="c3eda-144"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3eda-144"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="c3eda-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c3eda-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3eda-146"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3eda-146"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3eda-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3eda-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3eda-148">**Pdhvbkreatecounterpathlist**</span><span class="sxs-lookup"><span data-stu-id="c3eda-148">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="c3eda-149">**Pdhvbgetcounterpathfromlist**</span><span class="sxs-lookup"><span data-stu-id="c3eda-149">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[<span data-ttu-id="c3eda-150">**Pdhvbgetonecounterpath**</span><span class="sxs-lookup"><span data-stu-id="c3eda-150">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

