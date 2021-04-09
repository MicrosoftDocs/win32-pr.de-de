---
description: Ruft einen Wert ab, der die Tages Komponente des DateTime-Werts darstellt, oder legt diesen fest.
ms.assetid: 60da99bc-560c-45bc-b787-f4bef8e5a509
ms.tgt_platform: multiple
title: Taubemdatetime. Day-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Day
- ISWbemDateTime.Day
- ISWbemDateTime.get_Day
- ISWbemDateTime.put_Day
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1de77a8e5d616284c3dc13a19bce2526db371c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960611"
---
# <a name="swbemdatetimeday-property"></a><span data-ttu-id="7cf6d-103">Taubemdatetime. Day (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7cf6d-103">SWbemDateTime.Day property</span></span>

<span data-ttu-id="7cf6d-104">Die **Day** -Eigenschaft des " [**Swap DateTime**](swbemdatetime.md) "-Objekts Ruft einen Wert ab, der die Tages Komponente des DateTime-Werts darstellt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="7cf6d-104">The **Day** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the day component of the datetime value.</span></span> <span data-ttu-id="7cf6d-105">Der Wert muss zwischen 1 und 31 liegen, wenn [**isinterval**](swbemdatetime-isinterval.md) den Wert **false** hat.</span><span class="sxs-lookup"><span data-stu-id="7cf6d-105">The value must be in the range of 1 through 31 if [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**.</span></span> <span data-ttu-id="7cf6d-106">Allerdings ist die Fehlerüberprüfung für den Monatswert nicht vertraulich.</span><span class="sxs-lookup"><span data-stu-id="7cf6d-106">However, error checking is not sensitive to the month value.</span></span> <span data-ttu-id="7cf6d-107">Folglich gibt der in-Range-Wert 31 in den Fällen, in denen der Wert für " [**Swap DateTime. Month**](swbemdatetime-month.md) " für einen Monat weniger als 31 Tage beträgt (Februar, April, Juni, September, November), keinen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7cf6d-107">Thus, the in-range value of 31 will not return an error in the cases where the [**SWbemDateTime.Month**](swbemdatetime-month.md) value is for a month of fewer than 31 days (February, April, June, September, November).</span></span>

<span data-ttu-id="7cf6d-108">Der Standardwert für **Day** ist 01.</span><span class="sxs-lookup"><span data-stu-id="7cf6d-108">The default value for **Day** is 01.</span></span>

<span data-ttu-id="7cf6d-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7cf6d-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="7cf6d-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7cf6d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf6d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cf6d-111">Syntax</span></span>


```VB
SWbemDateTime.Day As Long
```



## <a name="property-value"></a><span data-ttu-id="7cf6d-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7cf6d-112">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="7cf6d-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7cf6d-113">Error codes</span></span>

<span data-ttu-id="7cf6d-114">Nachdem Sie die **Day** -Eigenschaft festgelegt oder festgelegt haben, enthält das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt möglicherweise den folgenden Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7cf6d-114">After you get or set the **Day** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="7cf6d-115">**wbemErrValueOutOfRange** -2147749931 (0x8004102b)</span><span class="sxs-lookup"><span data-stu-id="7cf6d-115">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="7cf6d-116">Wenn [**isinterval**](swbemdatetime-isinterval.md) den Wert **true** hat und der Bereich der korrekten Werte 0 bis 99999999 überschreitet.</span><span class="sxs-lookup"><span data-stu-id="7cf6d-116">If [**IsInterval**](swbemdatetime-isinterval.md) is **TRUE** and the range of correct values exceeds 0 through 99999999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="7cf6d-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7cf6d-117">Examples</span></span>

<span data-ttu-id="7cf6d-118">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="7cf6d-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="7cf6d-119">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="7cf6d-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7cf6d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7cf6d-120">Requirements</span></span>



| <span data-ttu-id="7cf6d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7cf6d-121">Requirement</span></span> | <span data-ttu-id="7cf6d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7cf6d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cf6d-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7cf6d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7cf6d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7cf6d-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7cf6d-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7cf6d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7cf6d-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7cf6d-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7cf6d-127">Header</span><span class="sxs-lookup"><span data-stu-id="7cf6d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cf6d-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cf6d-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7cf6d-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7cf6d-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="7cf6d-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7cf6d-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7cf6d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7cf6d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cf6d-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cf6d-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7cf6d-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="7cf6d-133">CLSID</span></span><br/>                    | <span data-ttu-id="7cf6d-134">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="7cf6d-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="7cf6d-135">IID</span><span class="sxs-lookup"><span data-stu-id="7cf6d-135">IID</span></span><br/>                      | <span data-ttu-id="7cf6d-136">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="7cf6d-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="7cf6d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cf6d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cf6d-138">**Swap-DateTime. dayangegebene**</span><span class="sxs-lookup"><span data-stu-id="7cf6d-138">**SWbemDateTime.DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
</dt> <dt>

[<span data-ttu-id="7cf6d-139">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="7cf6d-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="7cf6d-140">DateTime</span><span class="sxs-lookup"><span data-stu-id="7cf6d-140">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

