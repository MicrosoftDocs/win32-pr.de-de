---
description: Boolescher Wert, der angibt, ob die Year-Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.
ms.assetid: afac0a08-7bd0-42f1-b5a7-8664f9db8615
ms.tgt_platform: multiple
title: Die Eigenschaft "Swap DateTime. Year" (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.YearSpecified
- ISWbemDateTime.YearSpecified
- ISWbemDateTime.get_YearSpecified
- ISWbemDateTime.put_YearSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3ad6ae5b120c2b38d7b6170951ef30b3b19f5295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360167"
---
# <a name="swbemdatetimeyearspecified-property"></a><span data-ttu-id="eaa8a-103">Eigenschaft ' Swap DateTime. year'</span><span class="sxs-lookup"><span data-stu-id="eaa8a-103">SWbemDateTime.YearSpecified property</span></span>

<span data-ttu-id="eaa8a-104">Die **yearangegebene** Eigenschaft des-Objekts von " [**Swap DateTime**](swbemdatetime.md) " ist ein boolescher Wert, der angibt, ob die Year-Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="eaa8a-104">The **YearSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the year component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="eaa8a-105">Wenn "Year" auf " **true** " **festgelegt** ist und [**isinterval**](swbemdatetime-isinterval.md) " **false**" ist, enthält " [**taubemdatetime. Year**](swbemdatetime-year.md) " einen DateTime-Wert.</span><span class="sxs-lookup"><span data-stu-id="eaa8a-105">If **YearSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Year**](swbemdatetime-year.md) contains a datetime value.</span></span> <span data-ttu-id="eaa8a-106">Ein DateTime-Wert, der ein Intervall enthält, kann nicht in das **VT- \_ Datums** Format oder das **FILETIME** -Format konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="eaa8a-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="eaa8a-107">Wenn "Year" auf " **false** " **festgelegt** ist und **isinterval** " **true**" ist, enthält " **Swap DateTime. Year** " ein Intervall.</span><span class="sxs-lookup"><span data-stu-id="eaa8a-107">If **YearSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Year** contains an interval.</span></span>

<span data-ttu-id="eaa8a-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="eaa8a-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="eaa8a-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="eaa8a-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaa8a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="eaa8a-110">Syntax</span></span>


```VB
SWbemDateTime.YearSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="eaa8a-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="eaa8a-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="eaa8a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eaa8a-112">Examples</span></span>

<span data-ttu-id="eaa8a-113">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="eaa8a-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="eaa8a-114">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="eaa8a-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eaa8a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eaa8a-115">Requirements</span></span>



| <span data-ttu-id="eaa8a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eaa8a-116">Requirement</span></span> | <span data-ttu-id="eaa8a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="eaa8a-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eaa8a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eaa8a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eaa8a-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eaa8a-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eaa8a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eaa8a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eaa8a-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eaa8a-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eaa8a-122">Header</span><span class="sxs-lookup"><span data-stu-id="eaa8a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaa8a-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaa8a-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="eaa8a-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="eaa8a-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="eaa8a-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eaa8a-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eaa8a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="eaa8a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaa8a-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaa8a-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eaa8a-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="eaa8a-128">CLSID</span></span><br/>                    | <span data-ttu-id="eaa8a-129">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="eaa8a-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="eaa8a-130">IID</span><span class="sxs-lookup"><span data-stu-id="eaa8a-130">IID</span></span><br/>                      | <span data-ttu-id="eaa8a-131">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="eaa8a-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="eaa8a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eaa8a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaa8a-133">**Swap-DateTime. Year**</span><span class="sxs-lookup"><span data-stu-id="eaa8a-133">**SWbemDateTime.Year**</span></span>](swbemdatetime-year.md)
</dt> <dt>

[<span data-ttu-id="eaa8a-134">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="eaa8a-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="eaa8a-135">DateTime</span><span class="sxs-lookup"><span data-stu-id="eaa8a-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




