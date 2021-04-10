---
description: Gibt an, ob die Minuten Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.
ms.assetid: de15f87e-0092-467e-b0d7-42ef447fa00a
ms.tgt_platform: multiple
title: "' Taubemdatetime. minutesangegebene '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MinutesSpecified
- ISWbemDateTime.MinutesSpecified
- ISWbemDateTime.get_MinutesSpecified
- ISWbemDateTime.put_MinutesSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 62f64ad749ee020093008a308a3244e045f9995d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130996"
---
# <a name="swbemdatetimeminutesspecified-property"></a><span data-ttu-id="40f6b-103">"Taubemdatetime. minutesangegebene"-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="40f6b-103">SWbemDateTime.MinutesSpecified property</span></span>

<span data-ttu-id="40f6b-104">Die **minutesspezifizierte** -Eigenschaft des-Objekts von " [**Swap DateTime**](swbemdatetime.md) " ist ein boolescher Wert, der angibt, ob die Minuten Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="40f6b-104">The **MinutesSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the minutes component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="40f6b-105">Wenn **minutesist** **true** und [**isinterval**](swbemdatetime-isinterval.md) auf **false** festgelegt ist (was bedeutet, dass der CIM-DateTime-Wert keine Platzhalter hat), enthält " [**slibemdatetime. minutes**](swbemdatetime-minutes.md) " einen Datumswert.</span><span class="sxs-lookup"><span data-stu-id="40f6b-105">If **MinutesSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE** (indicating that the CIM datetime value has no wildcards), then [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) contains a date value.</span></span> <span data-ttu-id="40f6b-106">Ein DateTime-Wert, der ein Intervall enthält, kann nicht in das **VT- \_ Datums** Format oder das **FILETIME** -Format konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="40f6b-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="40f6b-107">Wenn [**"hoursist**](swbemdatetime-hoursspecified.md) **false** " und " **isinterval** " auf " **true**" festgelegt ist, enthält " **taubemdatetime. minutes** " ein Intervall.</span><span class="sxs-lookup"><span data-stu-id="40f6b-107">If [**HoursSpecified**](swbemdatetime-hoursspecified.md) is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Minutes** contains an interval.</span></span>

<span data-ttu-id="40f6b-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="40f6b-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="40f6b-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="40f6b-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="40f6b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="40f6b-110">Syntax</span></span>


```VB
SWbemDateTime.MinutesSpecified As boolean
```



## <a name="property-value"></a><span data-ttu-id="40f6b-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="40f6b-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="40f6b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40f6b-112">Examples</span></span>

<span data-ttu-id="40f6b-113">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="40f6b-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="40f6b-114">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="40f6b-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40f6b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40f6b-115">Requirements</span></span>



| <span data-ttu-id="40f6b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40f6b-116">Requirement</span></span> | <span data-ttu-id="40f6b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="40f6b-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40f6b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40f6b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="40f6b-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40f6b-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40f6b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40f6b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="40f6b-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40f6b-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40f6b-122">Header</span><span class="sxs-lookup"><span data-stu-id="40f6b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="40f6b-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="40f6b-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="40f6b-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="40f6b-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="40f6b-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="40f6b-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="40f6b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="40f6b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40f6b-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40f6b-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="40f6b-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="40f6b-128">CLSID</span></span><br/>                    | <span data-ttu-id="40f6b-129">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="40f6b-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="40f6b-130">IID</span><span class="sxs-lookup"><span data-stu-id="40f6b-130">IID</span></span><br/>                      | <span data-ttu-id="40f6b-131">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="40f6b-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="40f6b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40f6b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40f6b-133">**Swap DateTime. Minutes**</span><span class="sxs-lookup"><span data-stu-id="40f6b-133">**SWbemDateTime.Minutes**</span></span>](swbemdatetime-minutes.md)
</dt> <dt>

[<span data-ttu-id="40f6b-134">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="40f6b-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="40f6b-135">DateTime</span><span class="sxs-lookup"><span data-stu-id="40f6b-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




