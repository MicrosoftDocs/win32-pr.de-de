---
description: Ruft einen Wert ab, der die Minuten Komponente des DateTime-Werts darstellt, oder legt diesen fest.
ms.assetid: a52a66c2-f7ab-48d0-bdee-a07984ed3bc2
ms.tgt_platform: multiple
title: Swap DateTime. Minutes-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Minutes
- ISWbemDateTime.Minutes
- ISWbemDateTime.get_Minutes
- ISWbemDateTime.put_Minutes
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cce55d731916d0e8180de1bde495566d4ed22c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351566"
---
# <a name="swbemdatetimeminutes-property"></a><span data-ttu-id="35a15-103">' Swap DateTime. minutes '-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="35a15-103">SWbemDateTime.Minutes property</span></span>

<span data-ttu-id="35a15-104">Die **Minutes** -Eigenschaft des " [**Swap DateTime**](swbemdatetime.md) "-Objekts Ruft einen Wert ab, der die Minuten Komponente des DateTime-Werts darstellt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="35a15-104">The **Minutes** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the minutes component of the datetime value.</span></span>

<span data-ttu-id="35a15-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="35a15-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="35a15-106">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="35a15-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a15-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="35a15-107">Syntax</span></span>


```VB
SWbemDateTime.Minutes As Long
```



## <a name="property-value"></a><span data-ttu-id="35a15-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="35a15-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="35a15-109">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="35a15-109">Error codes</span></span>

<span data-ttu-id="35a15-110">Nachdem Sie die Eigenschaft **Minutes** festgelegt oder festgelegt haben, enthält das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt möglicherweise den folgenden Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="35a15-110">After you get or set the **Minutes** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="35a15-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102b)</span><span class="sxs-lookup"><span data-stu-id="35a15-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="35a15-112">Der Wert lag nicht im Bereich von 0 bis 59.</span><span class="sxs-lookup"><span data-stu-id="35a15-112">The value was not in the range of 0 through 59.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35a15-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35a15-113">Remarks</span></span>

<span data-ttu-id="35a15-114">Wenn die Eigenschaft " **slibemdatetime. minutes** " auf 1 festgelegt ist, enthält die Eigenschaft " [**slibemdatetime. seconds**](swbemdatetime-seconds.md) " einen Wert, der um eine Sekunde einen Rundungsfehler ergibt, der auftritt, wenn ein CIM- **DateTime** -Wert in einen **VT- \_ Datums** Wert übersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="35a15-114">If the **SWbemDateTime.Minutes** property is set to 1, then the [**SWbemDateTime.Seconds**](swbemdatetime-seconds.md) property contains a value that is offset by one second a rounding error that occurs when a CIM **datetime** value is translated to a **VT\_DATE** value.</span></span> <span data-ttu-id="35a15-115">Wenn die Eigenschaft **Minutes** stattdessen auf 0 festgelegt ist, gibt die **seconds** -Eigenschaft den richtigen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="35a15-115">If the **Minutes** property is set to 0 instead, then the **Seconds** property returns the correct value.</span></span>

## <a name="examples"></a><span data-ttu-id="35a15-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35a15-116">Examples</span></span>

<span data-ttu-id="35a15-117">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="35a15-117">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="35a15-118">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="35a15-118">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35a15-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35a15-119">Requirements</span></span>



| <span data-ttu-id="35a15-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35a15-120">Requirement</span></span> | <span data-ttu-id="35a15-121">Wert</span><span class="sxs-lookup"><span data-stu-id="35a15-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35a15-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35a15-122">Minimum supported client</span></span><br/> | <span data-ttu-id="35a15-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35a15-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35a15-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35a15-124">Minimum supported server</span></span><br/> | <span data-ttu-id="35a15-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35a15-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35a15-126">Header</span><span class="sxs-lookup"><span data-stu-id="35a15-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="35a15-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="35a15-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="35a15-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="35a15-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="35a15-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35a15-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35a15-130">DLL</span><span class="sxs-lookup"><span data-stu-id="35a15-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35a15-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35a15-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="35a15-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="35a15-132">CLSID</span></span><br/>                    | <span data-ttu-id="35a15-133">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="35a15-133">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="35a15-134">IID</span><span class="sxs-lookup"><span data-stu-id="35a15-134">IID</span></span><br/>                      | <span data-ttu-id="35a15-135">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="35a15-135">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="35a15-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35a15-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a15-137">**' Taubemdatetime. minutes' angegeben**</span><span class="sxs-lookup"><span data-stu-id="35a15-137">**SWbemDateTime.MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
</dt> <dt>

[<span data-ttu-id="35a15-138">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="35a15-138">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="35a15-139">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="35a15-139">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

