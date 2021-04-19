---
description: Boolescher Wert, der angibt, ob die Tages Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.
ms.assetid: a713378b-3953-49d8-9c6a-44aa9337eae2
ms.tgt_platform: multiple
title: "' Swap-DateTime. dayangegebene '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.DaySpecified
- ISWbemDateTime.DaySpecified
- ISWbemDateTime.get_DaySpecified
- ISWbemDateTime.put_DaySpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f295d33940f36212fde4fe821af8d5df24d4f75f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353206"
---
# <a name="swbemdatetimedayspecified-property"></a><span data-ttu-id="de8ef-103">Eigenschaft ' Swap DateTime. dayangegebene '</span><span class="sxs-lookup"><span data-stu-id="de8ef-103">SWbemDateTime.DaySpecified property</span></span>

<span data-ttu-id="de8ef-104">Die **dayangegebene** -Eigenschaft des-Objekts von " [**Swap DateTime**](swbemdatetime.md) " ist ein boolescher Wert, der angibt, ob die Tages Komponente im CIM- [**DateTime**](datetime.md) -Wert ein Intervall oder einen Platzhalter Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="de8ef-104">The **DaySpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the day component in the CIM [**DATETIME**](datetime.md) value contains an interval or a wildcard value.</span></span> <span data-ttu-id="de8ef-105">Wenn **dayfest gelegt** **ist** und [**isinterval**](swbemdatetime-isinterval.md) den Wert **false** aufweist, enthält " [**taubemdatetime. Day**](swbemdatetime-day.md) " einen DateTime-Wert.</span><span class="sxs-lookup"><span data-stu-id="de8ef-105">If **DaySpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Day**](swbemdatetime-day.md) contains a datetime value.</span></span> <span data-ttu-id="de8ef-106">Ein [**DateTime**](datetime.md) -Wert, der ein Intervall enthält, kann nicht in das **VT- \_ Datums** Format oder das **FILETIME** -Format konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="de8ef-106">A [**DATETIME**](datetime.md) value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="de8ef-107">Wenn **dayist** auf **false** festgelegt und **isinterval** den Wert **true** aufweist, enthält " **taubemdatetime. Day** " ein Intervall.</span><span class="sxs-lookup"><span data-stu-id="de8ef-107">If **DaySpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Day** contains an interval.</span></span>

<span data-ttu-id="de8ef-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="de8ef-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="de8ef-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="de8ef-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="de8ef-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="de8ef-110">Syntax</span></span>


```VB
SWbemDateTime.DaySpecified As BOOLEAN
```



## <a name="property-value"></a><span data-ttu-id="de8ef-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="de8ef-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="de8ef-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de8ef-112">Examples</span></span>

<span data-ttu-id="de8ef-113">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="de8ef-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="de8ef-114">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="de8ef-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de8ef-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de8ef-115">Requirements</span></span>



| <span data-ttu-id="de8ef-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de8ef-116">Requirement</span></span> | <span data-ttu-id="de8ef-117">Wert</span><span class="sxs-lookup"><span data-stu-id="de8ef-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de8ef-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de8ef-118">Minimum supported client</span></span><br/> | <span data-ttu-id="de8ef-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de8ef-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de8ef-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de8ef-120">Minimum supported server</span></span><br/> | <span data-ttu-id="de8ef-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de8ef-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de8ef-122">Header</span><span class="sxs-lookup"><span data-stu-id="de8ef-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="de8ef-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="de8ef-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="de8ef-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="de8ef-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="de8ef-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="de8ef-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="de8ef-126">DLL</span><span class="sxs-lookup"><span data-stu-id="de8ef-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de8ef-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de8ef-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="de8ef-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="de8ef-128">CLSID</span></span><br/>                    | <span data-ttu-id="de8ef-129">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="de8ef-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="de8ef-130">IID</span><span class="sxs-lookup"><span data-stu-id="de8ef-130">IID</span></span><br/>                      | <span data-ttu-id="de8ef-131">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="de8ef-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="de8ef-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de8ef-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de8ef-133">**Swap-DateTime. Day**</span><span class="sxs-lookup"><span data-stu-id="de8ef-133">**SWbemDateTime.Day**</span></span>](swbemdatetime-day.md)
</dt> <dt>

[<span data-ttu-id="de8ef-134">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="de8ef-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="de8ef-135">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="de8ef-135">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

 




