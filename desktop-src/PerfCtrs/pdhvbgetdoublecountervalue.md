---
description: Die pdhvbgetdoublecountervalue-Funktion gibt den aktuellen Wert des angegebenen Zählers als Gleit Komma Wert mit doppelter Genauigkeit zurück.
ms.assetid: a2ee63dd-da39-4104-921d-371172bcb45c
title: Pdhvbgetdoublecountervalue-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetDoubleCounterValue
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 67f0372a26649fbe781cf4d9bd25794b82d6346e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345509"
---
# <a name="pdhvbgetdoublecountervalue-function"></a><span data-ttu-id="95213-103">Pdhvbgetdoublecountervalue-Funktion</span><span class="sxs-lookup"><span data-stu-id="95213-103">PdhVbGetDoubleCounterValue function</span></span>

<span data-ttu-id="95213-104">Die **pdhvbgetdoublecountervalue** -Funktion gibt den aktuellen Wert des angegebenen Zählers als Gleit Komma Wert mit doppelter Genauigkeit zurück.</span><span class="sxs-lookup"><span data-stu-id="95213-104">The **PdhVbGetDoubleCounterValue** function returns the current value of the specified counter as a double-precision floating point value.</span></span> <span data-ttu-id="95213-105">Sie sollten den *Counter-Status* vor der Rückgabe der zurückgegebenen Nummer überprüfen, da der Indikator beim Lesen möglicherweise nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="95213-105">You should check *CounterStatus* before using the returned number, because the counter may not be valid when it is read.</span></span> <span data-ttu-id="95213-106">Zum Überprüfen des Status des Zählers wird die [**pdhvbisgoodstatus**](pdhvbisgoodstatus.md) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="95213-106">To check the counter status, call the [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95213-107">Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="95213-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="95213-108">Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="95213-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="95213-109">Funktion "pdhvbgetdoublecountervalue" ( \_ ByVal counterhandle "Long", \_ ByVal counterstatus "Long" \_ ) als "Double"</span><span class="sxs-lookup"><span data-stu-id="95213-109">Function PdhVbGetDoubleCounterValue( \_ ByVal CounterHandle As Long, \_ ByVal CounterStatus As Long \_ ) As Double</span></span>

## <a name="parameters"></a><span data-ttu-id="95213-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="95213-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95213-111">*Counter handle*</span><span class="sxs-lookup"><span data-stu-id="95213-111">*CounterHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="95213-112">ID des Zählers, dessen aktueller Wert gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="95213-112">ID of the counter whose current value is to be read.</span></span>

</dd> <dt>

<span data-ttu-id="95213-113">*Gegen Status*</span><span class="sxs-lookup"><span data-stu-id="95213-113">*CounterStatus*</span></span> 
</dt> <dd>

<span data-ttu-id="95213-114">Variable, in der der aktuelle Status des Leistungs Zählers an den Aufrufer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="95213-114">Variable in which the current status of the counter value is returned to the caller.</span></span> <span data-ttu-id="95213-115">Der zurückgegebene Datenwert ist nur gültig, wenn der im counterstatus zurückgegebene Wert PDH \_ cstatus \_ gültige \_ Daten oder PDH \_ cstatus \_ New \_ Data ist (siehe PDH-Fehlercodes).</span><span class="sxs-lookup"><span data-stu-id="95213-115">The returned data value is valid if and only if the value returned in CounterStatus is PDH\_CSTATUS\_VALID\_DATA or PDH\_CSTATUS\_NEW\_DATA (see PDH error codes).</span></span> <span data-ttu-id="95213-116">Wenn der in Counter Status zurückgegebene Wert ein beliebiger anderer Wert ist, verwenden Sie die Daten nicht.</span><span class="sxs-lookup"><span data-stu-id="95213-116">If the value returned in CounterStatus is any other value, do not use the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95213-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95213-117">Return value</span></span>

<span data-ttu-id="95213-118">Die-Funktion gibt den Gleit Komma Wert mit doppelter Genauigkeit des aktuellen Zählers zurück, berechnet und formatiert, wie vom Zählertyp definiert.</span><span class="sxs-lookup"><span data-stu-id="95213-118">The function returns the double-precision floating point value of the current counter, computed and formatted as defined by the counter type.</span></span>

## <a name="requirements"></a><span data-ttu-id="95213-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95213-119">Requirements</span></span>



| <span data-ttu-id="95213-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95213-120">Requirement</span></span> | <span data-ttu-id="95213-121">Wert</span><span class="sxs-lookup"><span data-stu-id="95213-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="95213-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95213-122">Minimum supported client</span></span><br/> | <span data-ttu-id="95213-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95213-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95213-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95213-124">Minimum supported server</span></span><br/> | <span data-ttu-id="95213-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95213-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="95213-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95213-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="95213-127"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95213-127"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="95213-128">DLL</span><span class="sxs-lookup"><span data-stu-id="95213-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95213-129"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95213-129"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95213-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95213-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95213-131">**Pdhvbisgoodstatus**</span><span class="sxs-lookup"><span data-stu-id="95213-131">**PdhVbIsGoodStatus**</span></span>](pdhvbisgoodstatus.md)
</dt> </dl>

 

 




