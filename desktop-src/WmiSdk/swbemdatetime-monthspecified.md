---
description: Boolescher Wert, der angibt, ob die Monats Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.
ms.assetid: 12dd94de-24be-4b13-bde5-2fc28be94efa
ms.tgt_platform: multiple
title: "' Taubemdatetime. monthspezifi'-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MonthSpecified
- ISWbemDateTime.MonthSpecified
- ISWbemDateTime.get_MonthSpecified
- ISWbemDateTime.put_MonthSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 52b44444a5810577289353778c2c00b1ebfb80fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372956"
---
# <a name="swbemdatetimemonthspecified-property"></a><span data-ttu-id="6ef77-103">' Swap DateTime. monthangegebene '-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6ef77-103">SWbemDateTime.MonthSpecified property</span></span>

<span data-ttu-id="6ef77-104">Die **monthspezifisierte** Eigenschaft des Objekts " [**Swap DateTime**](swbemdatetime.md) " ist ein boolescher Wert, der angibt, ob die Monats Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="6ef77-104">The **MonthSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the month component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="6ef77-105">Wenn **monthspezifiziert** **true** und [**isinterval**](swbemdatetime-isinterval.md) den Wert **false** aufweist, enthält " [**slibemdatetime. Month**](swbemdatetime-month.md) " einen Datumswert.</span><span class="sxs-lookup"><span data-stu-id="6ef77-105">If **MonthSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Month**](swbemdatetime-month.md) contains a date value.</span></span> <span data-ttu-id="6ef77-106">Ein DateTime-Wert, der ein Intervall enthält, kann nicht in das **VT- \_ Datums** Format oder das **FILETIME** -Format konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="6ef77-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="6ef77-107">Wenn **monthist** auf " **false** " festgelegt ist und **isinterval** " **true**" ist, enthält " **taubemdatetime. Month** " ein Intervall.</span><span class="sxs-lookup"><span data-stu-id="6ef77-107">If **MonthSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Month** contains an interval.</span></span>

<span data-ttu-id="6ef77-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6ef77-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="6ef77-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6ef77-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ef77-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ef77-110">Syntax</span></span>


```VB
SWbemDateTime.MonthSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="6ef77-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6ef77-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="6ef77-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ef77-112">Examples</span></span>

<span data-ttu-id="6ef77-113">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="6ef77-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="6ef77-114">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="6ef77-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ef77-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ef77-115">Requirements</span></span>



| <span data-ttu-id="6ef77-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ef77-116">Requirement</span></span> | <span data-ttu-id="6ef77-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6ef77-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef77-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ef77-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6ef77-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ef77-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ef77-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ef77-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6ef77-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ef77-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ef77-122">Header</span><span class="sxs-lookup"><span data-stu-id="6ef77-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ef77-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ef77-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ef77-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6ef77-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="6ef77-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6ef77-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6ef77-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6ef77-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ef77-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ef77-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ef77-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="6ef77-128">CLSID</span></span><br/>                    | <span data-ttu-id="6ef77-129">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="6ef77-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="6ef77-130">IID</span><span class="sxs-lookup"><span data-stu-id="6ef77-130">IID</span></span><br/>                      | <span data-ttu-id="6ef77-131">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="6ef77-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="6ef77-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ef77-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef77-133">**Swap-DateTime. Month**</span><span class="sxs-lookup"><span data-stu-id="6ef77-133">**SWbemDateTime.Month**</span></span>](swbemdatetime-month.md)
</dt> <dt>

[<span data-ttu-id="6ef77-134">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="6ef77-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="6ef77-135">DateTime</span><span class="sxs-lookup"><span data-stu-id="6ef77-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




