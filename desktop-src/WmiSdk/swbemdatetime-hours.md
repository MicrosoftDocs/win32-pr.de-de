---
description: Ruft einen Wert ab, der die Stunden Komponente des DateTime-Werts darstellt, oder legt diesen fest.
ms.assetid: 83f084fa-57a5-4467-acea-7e19de82a91f
ms.tgt_platform: multiple
title: Swap DateTime. Hours-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Hours
- ISWbemDateTime.Hours
- ISWbemDateTime.get_Hours
- ISWbemDateTime.put_Hours
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 27edb3c209e2e95ae7aff20930d260f8f6d44427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217951"
---
# <a name="swbemdatetimehours-property"></a><span data-ttu-id="7c717-103">Swap DateTime. Hours (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7c717-103">SWbemDateTime.Hours property</span></span>

<span data-ttu-id="7c717-104">Die **Hours** -Eigenschaft des-Objekts von " [**waybemdatetime**](swbemdatetime.md) " Ruft einen Wert ab, der die Stunden Komponente des DateTime-Werts darstellt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="7c717-104">The **Hours** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the hours component of the datetime value.</span></span>

<span data-ttu-id="7c717-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7c717-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="7c717-106">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7c717-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c717-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c717-107">Syntax</span></span>


```VB
SWbemDateTime.Hours As Long
```



## <a name="property-value"></a><span data-ttu-id="7c717-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7c717-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="7c717-109">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7c717-109">Error codes</span></span>

<span data-ttu-id="7c717-110">Nachdem Sie die **Hours** -Eigenschaft festgelegt oder festgelegt haben, enthält das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt möglicherweise den folgenden Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7c717-110">After you get or set the **Hours** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="7c717-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102b)</span><span class="sxs-lookup"><span data-stu-id="7c717-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="7c717-112">Der Wert lag nicht im Bereich von 0 bis 23.</span><span class="sxs-lookup"><span data-stu-id="7c717-112">The value was not in the range of 0 through 23.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="7c717-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c717-113">Examples</span></span>

<span data-ttu-id="7c717-114">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="7c717-114">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="7c717-115">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="7c717-115">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c717-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c717-116">Requirements</span></span>



| <span data-ttu-id="7c717-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c717-117">Requirement</span></span> | <span data-ttu-id="7c717-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7c717-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c717-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c717-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7c717-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c717-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c717-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c717-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7c717-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c717-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c717-123">Header</span><span class="sxs-lookup"><span data-stu-id="7c717-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c717-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c717-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c717-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7c717-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="7c717-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7c717-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7c717-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7c717-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c717-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c717-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7c717-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="7c717-129">CLSID</span></span><br/>                    | <span data-ttu-id="7c717-130">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="7c717-130">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="7c717-131">IID</span><span class="sxs-lookup"><span data-stu-id="7c717-131">IID</span></span><br/>                      | <span data-ttu-id="7c717-132">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="7c717-132">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="7c717-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c717-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c717-134">**' Taubemdatetime. hoursangegeben '**</span><span class="sxs-lookup"><span data-stu-id="7c717-134">**SWbemDateTime.HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
</dt> <dt>

[<span data-ttu-id="7c717-135">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="7c717-135">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="7c717-136">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="7c717-136">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

