---
description: Ruft einen Wert ab, der die Jahres Komponente des DateTime-Werts darstellt, oder legt diesen fest.
ms.assetid: eab3738a-c92a-4602-b1ee-e2547da88308
ms.tgt_platform: multiple
title: Taubemdatetime. Year-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Year
- ISWbemDateTime.Year
- ISWbemDateTime.get_Year
- ISWbemDateTime.put_Year
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5fe8988b3772f0f5d976c38eb5e9cc44fb9c4ede
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355307"
---
# <a name="swbemdatetimeyear-property"></a><span data-ttu-id="d626f-103">' Swap DateTime. Year '-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d626f-103">SWbemDateTime.Year property</span></span>

<span data-ttu-id="d626f-104">Die **year** -Eigenschaft des " [**Swap DateTime**](swbemdatetime.md) "-Objekts Ruft einen Wert ab, der die Jahres Komponente des [**DateTime**](datetime.md) -Werts darstellt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="d626f-104">The **Year** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the year component of the [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="d626f-105">Der Wert muss im Bereich von 0000-9999 liegen, oder der Fehler wbemErrValueOutOfRange wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d626f-105">The value must be in the range of 0000 - 9999 or the error wbemErrValueOutOfRange is returned.</span></span>

<span data-ttu-id="d626f-106">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d626f-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="d626f-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d626f-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d626f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d626f-108">Syntax</span></span>


```VB
SWbemDateTime.Year As Long
```



## <a name="property-value"></a><span data-ttu-id="d626f-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d626f-109">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="d626f-110">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d626f-110">Error codes</span></span>

<span data-ttu-id="d626f-111">Nachdem Sie die **year** -Eigenschaft festgelegt oder festgelegt haben, enthält das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt möglicherweise den folgenden Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d626f-111">After you get or set the **Year** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="d626f-112">**wbemErrValueOutOfRange** -2147749931 (0x8004102b)</span><span class="sxs-lookup"><span data-stu-id="d626f-112">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="d626f-113">Der Wert lag nicht im Bereich von 0000 bis 9999.</span><span class="sxs-lookup"><span data-stu-id="d626f-113">The value was not in the range of 0000 through 9999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d626f-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d626f-114">Examples</span></span>

<span data-ttu-id="d626f-115">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="d626f-115">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="d626f-116">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="d626f-116">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d626f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d626f-117">Requirements</span></span>



| <span data-ttu-id="d626f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d626f-118">Requirement</span></span> | <span data-ttu-id="d626f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d626f-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d626f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d626f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d626f-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d626f-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d626f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d626f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d626f-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d626f-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d626f-124">Header</span><span class="sxs-lookup"><span data-stu-id="d626f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d626f-125"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d626f-125"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d626f-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d626f-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="d626f-127"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d626f-127"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d626f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d626f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d626f-129"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d626f-129"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d626f-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="d626f-130">CLSID</span></span><br/>                    | <span data-ttu-id="d626f-131">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="d626f-131">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="d626f-132">IID</span><span class="sxs-lookup"><span data-stu-id="d626f-132">IID</span></span><br/>                      | <span data-ttu-id="d626f-133">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="d626f-133">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d626f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d626f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d626f-135">**' Swap DateTime. year' angegeben**</span><span class="sxs-lookup"><span data-stu-id="d626f-135">**SWbemDateTime.YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
</dt> <dt>

[<span data-ttu-id="d626f-136">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="d626f-136">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="d626f-137">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="d626f-137">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

