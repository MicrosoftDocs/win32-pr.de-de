---
description: Die hoursangegebene-Eigenschaft des ' waybemdatetime '-Objekts ist ein boolescher Wert, der angibt, ob die Stunden Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.
ms.assetid: 55211da6-cbd5-4e61-ab7d-ee20363e9d81
ms.tgt_platform: multiple
title: "' Taubemdatetime. hoursangegebene '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.HoursSpecified
- ISWbemDateTime.HoursSpecified
- ISWbemDateTime.get_HoursSpecified
- ISWbemDateTime.put_HoursSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e092747768035b7948ddef66f4c4d542bfa2c38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343794"
---
# <a name="swbemdatetimehoursspecified-property"></a><span data-ttu-id="e7eba-103">Eigenschaft ' Swap DateTime. hoursangegebene '</span><span class="sxs-lookup"><span data-stu-id="e7eba-103">SWbemDateTime.HoursSpecified property</span></span>

<span data-ttu-id="e7eba-104">Die **hoursangegebene** -Eigenschaft des ' [**waybemdatetime**](swbemdatetime.md) '-Objekts ist ein boolescher Wert, der angibt, ob die Stunden Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="e7eba-104">The **HoursSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the hours component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="e7eba-105">Wenn **"hoursist** **true** " und " [**isinterval**](swbemdatetime-isinterval.md) " auf " **false**" festgelegt ist, enthält " [**taubemdatetime. Hours**](swbemdatetime-hours.md) " einen DateTime-Wert.</span><span class="sxs-lookup"><span data-stu-id="e7eba-105">If **HoursSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Hours**](swbemdatetime-hours.md) contains a datetime value.</span></span> <span data-ttu-id="e7eba-106">Ein DateTime-Wert, der ein Intervall enthält, kann nicht in das **VT- \_ Datums** Format oder das **FILETIME** -Format konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="e7eba-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="e7eba-107">Wenn **"hoursist** **false** " und " **isinterval** " auf " **true**" festgelegt ist, enthält " **taubemdatetime. Hours** " ein Intervall.</span><span class="sxs-lookup"><span data-stu-id="e7eba-107">If **HoursSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Hours** contains an interval.</span></span>

<span data-ttu-id="e7eba-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e7eba-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="e7eba-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e7eba-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7eba-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7eba-110">Syntax</span></span>


```VB
SWbemDateTime.HoursSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e7eba-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e7eba-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="e7eba-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7eba-112">Examples</span></span>

<span data-ttu-id="e7eba-113">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="e7eba-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="e7eba-114">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="e7eba-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7eba-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7eba-115">Requirements</span></span>



| <span data-ttu-id="e7eba-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7eba-116">Requirement</span></span> | <span data-ttu-id="e7eba-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e7eba-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7eba-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7eba-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e7eba-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7eba-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e7eba-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7eba-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e7eba-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7eba-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7eba-122">Header</span><span class="sxs-lookup"><span data-stu-id="e7eba-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7eba-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7eba-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7eba-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e7eba-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="e7eba-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e7eba-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e7eba-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e7eba-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7eba-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7eba-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e7eba-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="e7eba-128">CLSID</span></span><br/>                    | <span data-ttu-id="e7eba-129">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="e7eba-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="e7eba-130">IID</span><span class="sxs-lookup"><span data-stu-id="e7eba-130">IID</span></span><br/>                      | <span data-ttu-id="e7eba-131">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="e7eba-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="e7eba-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7eba-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7eba-133">**Swap-DateTime. Hours**</span><span class="sxs-lookup"><span data-stu-id="e7eba-133">**SWbemDateTime.Hours**</span></span>](swbemdatetime-hours.md)
</dt> <dt>

[<span data-ttu-id="e7eba-134">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="e7eba-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="e7eba-135">DateTime</span><span class="sxs-lookup"><span data-stu-id="e7eba-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




