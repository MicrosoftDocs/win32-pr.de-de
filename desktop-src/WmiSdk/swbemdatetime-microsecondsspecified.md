---
description: Boolescher Wert, der angibt, ob die Mikrosekunden Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.
ms.assetid: 65244ece-2326-4edc-b982-57e2046ec33e
ms.tgt_platform: multiple
title: "' Taubemdatetime. Mikro secondsangegebene '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MicrosecondsSpecified
- ISWbemDateTime.MicrosecondsSpecified
- ISWbemDateTime.get_MicrosecondsSpecified
- ISWbemDateTime.put_MicrosecondsSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d4fa9d99cf323e19ccd298786896f789bbb08be6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360169"
---
# <a name="swbemdatetimemicrosecondsspecified-property"></a><span data-ttu-id="7f944-103">' Taubemdatetime. Mikro secondsangegebene '-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7f944-103">SWbemDateTime.MicrosecondsSpecified property</span></span>

<span data-ttu-id="7f944-104">Die Eigenschaft " **mikrosecondsspezifiziert** " des Objekts " [**Swap DateTime**](swbemdatetime.md) " ist ein boolescher Wert, der angibt, ob die Mikrosekunden Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="7f944-104">The **MicrosecondsSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the microseconds component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="7f944-105">Wenn " **Mikro secondsist** **true** " und " [**isinterval**](swbemdatetime-isinterval.md) " auf " **false**" festgelegt ist, enthält " [**taubemdatetime. Mikro seconds**](swbemdatetime-microseconds.md) " einen DateTime-Wert.</span><span class="sxs-lookup"><span data-stu-id="7f944-105">If **MicrosecondsSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Microseconds**](swbemdatetime-microseconds.md) contains a datetime value.</span></span> <span data-ttu-id="7f944-106">Ein DateTime-Wert, der ein Intervall enthält, kann nicht in das **VT- \_ Datums** Format oder das **FILETIME** -Format konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="7f944-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="7f944-107">Wenn [**"hoursist**](swbemdatetime-hoursspecified.md) **false** " und " **isinterval** " auf " **true**" festgelegt ist, enthält " **taubemdatetime. Mikro seconds** " ein Intervall.</span><span class="sxs-lookup"><span data-stu-id="7f944-107">If [**HoursSpecified**](swbemdatetime-hoursspecified.md) is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Microseconds** contains an interval.</span></span>

<span data-ttu-id="7f944-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7f944-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="7f944-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7f944-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f944-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f944-110">Syntax</span></span>


```VB
SWbemDateTime.MicrosecondsSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="7f944-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7f944-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="7f944-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f944-112">Examples</span></span>

<span data-ttu-id="7f944-113">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="7f944-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="7f944-114">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="7f944-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f944-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f944-115">Requirements</span></span>



| <span data-ttu-id="7f944-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f944-116">Requirement</span></span> | <span data-ttu-id="7f944-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7f944-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f944-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f944-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7f944-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f944-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f944-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f944-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7f944-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f944-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f944-122">Header</span><span class="sxs-lookup"><span data-stu-id="7f944-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f944-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f944-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f944-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7f944-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="7f944-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7f944-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7f944-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7f944-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f944-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f944-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7f944-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="7f944-128">CLSID</span></span><br/>                    | <span data-ttu-id="7f944-129">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="7f944-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="7f944-130">IID</span><span class="sxs-lookup"><span data-stu-id="7f944-130">IID</span></span><br/>                      | <span data-ttu-id="7f944-131">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="7f944-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="7f944-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f944-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f944-133">**Swap-DateTime. Mikrosekunden**</span><span class="sxs-lookup"><span data-stu-id="7f944-133">**SWbemDateTime.Microseconds**</span></span>](swbemdatetime-microseconds.md)
</dt> <dt>

[<span data-ttu-id="7f944-134">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="7f944-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="7f944-135">DateTime</span><span class="sxs-lookup"><span data-stu-id="7f944-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




