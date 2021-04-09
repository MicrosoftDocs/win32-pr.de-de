---
description: Boolescher Wert, der angibt, ob die Sekunden Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.
ms.assetid: 9f9b75c3-ae08-49a6-b747-294831601a62
ms.tgt_platform: multiple
title: "' Swap DateTime. secondsangegebene '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SecondsSpecified
- ISWbemDateTime.SecondsSpecified
- ISWbemDateTime.get_SecondsSpecified
- ISWbemDateTime.put_SecondsSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e0cf97eff544d6e244890014108506f39b1934b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868388"
---
# <a name="swbemdatetimesecondsspecified-property"></a><span data-ttu-id="20b93-103">' Swap DateTime. secondsangegebene '-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="20b93-103">SWbemDateTime.SecondsSpecified property</span></span>

<span data-ttu-id="20b93-104">Die **secondsspezifisierte** Eigenschaft des-Objekts von " [**Swap DateTime**](swbemdatetime.md) " ist ein boolescher Wert, der angibt, ob die Sekunden Komponente im CIM- [**DateTime**](datetime.md) -Wert ein Intervall oder einen Platzhalter Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="20b93-104">The **SecondsSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the seconds component in the CIM [**DATETIME**](datetime.md) value contains an interval or a wildcard value.</span></span> <span data-ttu-id="20b93-105">Wenn **secondsspezifiziert** **true** und [**isinterval**](swbemdatetime-isinterval.md) den Wert **false** aufweist, enthält " [**slibemdatetime. seconds**](swbemdatetime-seconds.md) " einen Datumswert.</span><span class="sxs-lookup"><span data-stu-id="20b93-105">If **SecondsSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Seconds**](swbemdatetime-seconds.md) contains a date value.</span></span> <span data-ttu-id="20b93-106">Ein DateTime-Wert, der ein Intervall enthält, kann nicht in das **VT- \_ Datums** Format oder das **FILETIME** -Format konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="20b93-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="20b93-107">Wenn **secondsist** auf **false** festgelegt und **isinterval** den Wert **true** aufweist, enthält der Wert von " **taubemdatetime. seconds** " ein Intervall.</span><span class="sxs-lookup"><span data-stu-id="20b93-107">If **SecondsSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Seconds** contains an interval.</span></span>

<span data-ttu-id="20b93-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="20b93-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="20b93-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="20b93-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="20b93-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="20b93-110">Syntax</span></span>


```VB
SWbemDateTime.SecondsSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="20b93-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="20b93-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="20b93-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20b93-112">Examples</span></span>

<span data-ttu-id="20b93-113">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="20b93-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="20b93-114">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="20b93-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20b93-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20b93-115">Requirements</span></span>



| <span data-ttu-id="20b93-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20b93-116">Requirement</span></span> | <span data-ttu-id="20b93-117">Wert</span><span class="sxs-lookup"><span data-stu-id="20b93-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20b93-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20b93-118">Minimum supported client</span></span><br/> | <span data-ttu-id="20b93-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20b93-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="20b93-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20b93-120">Minimum supported server</span></span><br/> | <span data-ttu-id="20b93-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20b93-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="20b93-122">Header</span><span class="sxs-lookup"><span data-stu-id="20b93-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="20b93-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="20b93-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="20b93-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="20b93-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="20b93-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="20b93-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="20b93-126">DLL</span><span class="sxs-lookup"><span data-stu-id="20b93-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20b93-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20b93-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="20b93-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="20b93-128">CLSID</span></span><br/>                    | <span data-ttu-id="20b93-129">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="20b93-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="20b93-130">IID</span><span class="sxs-lookup"><span data-stu-id="20b93-130">IID</span></span><br/>                      | <span data-ttu-id="20b93-131">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="20b93-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="20b93-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20b93-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20b93-133">**Swap-DateTime. Sekunden**</span><span class="sxs-lookup"><span data-stu-id="20b93-133">**SWbemDateTime.Seconds**</span></span>](swbemdatetime-seconds.md)
</dt> <dt>

[<span data-ttu-id="20b93-134">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="20b93-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="20b93-135">DateTime</span><span class="sxs-lookup"><span data-stu-id="20b93-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




