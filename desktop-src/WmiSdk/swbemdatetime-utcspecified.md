---
description: Boolescher Wert, der angibt, ob die Komponente für die universelle koordinierte Uhrzeit (UTC) im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.
ms.assetid: 9cb04351-294b-48ba-8d1c-2f28cb9ce463
ms.tgt_platform: multiple
title: "' Taubemdatetime. utcangegebene '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTCSpecified
- ISWbemDateTime.UTCSpecified
- ISWbemDateTime.get_UTCSpecified
- ISWbemDateTime.put_UTCSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2ada5bbbfa68e6cb63c0e060d6c3a12c0f771a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347472"
---
# <a name="swbemdatetimeutcspecified-property"></a><span data-ttu-id="636d8-103">"Taubemdatetime. utcangegebene"-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="636d8-103">SWbemDateTime.UTCSpecified property</span></span>

<span data-ttu-id="636d8-104">Die **utcspezifische** Eigenschaft des Objekts " [**Swap DateTime**](swbemdatetime.md) " ist ein boolescher Wert, der angibt, ob die Komponente für die universelle koordinierte Uhrzeit (UTC) im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="636d8-104">The **UTCSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the Universal Coordinated Time (UTC) component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="636d8-105">Wenn **utcif** **true** und [**isinterval**](swbemdatetime-isinterval.md) den Wert **false** aufweist, enthält die Datei "- [**DateTime**](datetime.md) [**. UTC**](swbemdatetime-utc.md) " einen DateTime-Wert.</span><span class="sxs-lookup"><span data-stu-id="636d8-105">If **UTCSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.UTC**](swbemdatetime-utc.md) contains a [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="636d8-106">Ein **DateTime** -Wert, der ein Intervall enthält, kann nicht in das **VT- \_ Datums** Format oder das **FILETIME** -Format konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="636d8-106">A **DATETIME** value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="636d8-107">Wenn **utcif** **false** ist und **isinterval** den Wert **true** aufweist, enthält " **taubemdatetime. UTC** " ein Intervall.</span><span class="sxs-lookup"><span data-stu-id="636d8-107">If **UTCSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.UTC** contains an interval.</span></span>

<span data-ttu-id="636d8-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="636d8-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="636d8-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="636d8-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="636d8-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="636d8-110">Syntax</span></span>


```VB
SWbemDateTime.UTCSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="636d8-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="636d8-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="636d8-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="636d8-112">Examples</span></span>

<span data-ttu-id="636d8-113">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="636d8-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="636d8-114">Eine Beschreibung des CIM-DateTime-Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="636d8-114">For a description of the CIM datetime format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="636d8-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="636d8-115">Requirements</span></span>



| <span data-ttu-id="636d8-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="636d8-116">Requirement</span></span> | <span data-ttu-id="636d8-117">Wert</span><span class="sxs-lookup"><span data-stu-id="636d8-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="636d8-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="636d8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="636d8-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="636d8-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="636d8-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="636d8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="636d8-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="636d8-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="636d8-122">Header</span><span class="sxs-lookup"><span data-stu-id="636d8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="636d8-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="636d8-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="636d8-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="636d8-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="636d8-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="636d8-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="636d8-126">DLL</span><span class="sxs-lookup"><span data-stu-id="636d8-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="636d8-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="636d8-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="636d8-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="636d8-128">CLSID</span></span><br/>                    | <span data-ttu-id="636d8-129">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="636d8-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="636d8-130">IID</span><span class="sxs-lookup"><span data-stu-id="636d8-130">IID</span></span><br/>                      | <span data-ttu-id="636d8-131">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="636d8-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="636d8-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="636d8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="636d8-133">**"Taubemdatetime. UTC"**</span><span class="sxs-lookup"><span data-stu-id="636d8-133">**SWbemDateTime.UTC**</span></span>](swbemdatetime-utc.md)
</dt> <dt>

[<span data-ttu-id="636d8-134">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="636d8-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="636d8-135">DateTime</span><span class="sxs-lookup"><span data-stu-id="636d8-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




