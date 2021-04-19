---
description: Ruft einen Wert ab, der die Monats Komponente des DateTime-Werts darstellt, oder legt diesen fest.
ms.assetid: 05818f0a-7e15-4ddd-a6a7-9d16ae82cd3c
ms.tgt_platform: multiple
title: Taubemdatetime. Month-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Month
- ISWbemDateTime.Month
- ISWbemDateTime.get_Month
- ISWbemDateTime.put_Month
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 73769d73cffc5b9731cfd55785e2fa087182b33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350152"
---
# <a name="swbemdatetimemonth-property"></a><span data-ttu-id="3dd4d-103">' Swap DateTime. month '-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3dd4d-103">SWbemDateTime.Month property</span></span>

<span data-ttu-id="3dd4d-104">Die **Month** -Eigenschaft des " [**Swap DateTime**](swbemdatetime.md) "-Objekts Ruft einen Wert ab, der die Monats Komponente des DateTime-Werts darstellt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="3dd4d-104">The **Month** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the month component of the datetime value.</span></span> <span data-ttu-id="3dd4d-105">Die Zahl muss zwischen 01 und 12 liegen, oder es wird der Fehler " **wbemvalueouum Frange** " zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3dd4d-105">The number must be in the range of 01 through 12 or the error **wbemValueOutOfRange** is returned.</span></span>

<span data-ttu-id="3dd4d-106">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3dd4d-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="3dd4d-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3dd4d-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dd4d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3dd4d-108">Syntax</span></span>


```VB
SWbemDateTime.Month As Long
```



## <a name="property-value"></a><span data-ttu-id="3dd4d-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3dd4d-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="3dd4d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3dd4d-110">Examples</span></span>

<span data-ttu-id="3dd4d-111">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="3dd4d-111">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="3dd4d-112">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="3dd4d-112">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3dd4d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3dd4d-113">Requirements</span></span>



| <span data-ttu-id="3dd4d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3dd4d-114">Requirement</span></span> | <span data-ttu-id="3dd4d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3dd4d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dd4d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3dd4d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3dd4d-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3dd4d-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3dd4d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3dd4d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3dd4d-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3dd4d-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3dd4d-120">Header</span><span class="sxs-lookup"><span data-stu-id="3dd4d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dd4d-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dd4d-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3dd4d-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3dd4d-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="3dd4d-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3dd4d-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3dd4d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3dd4d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dd4d-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dd4d-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3dd4d-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="3dd4d-126">CLSID</span></span><br/>                    | <span data-ttu-id="3dd4d-127">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="3dd4d-127">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="3dd4d-128">IID</span><span class="sxs-lookup"><span data-stu-id="3dd4d-128">IID</span></span><br/>                      | <span data-ttu-id="3dd4d-129">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="3dd4d-129">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="3dd4d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dd4d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd4d-131">**"Swap DateTime. monthspezifiziert"**</span><span class="sxs-lookup"><span data-stu-id="3dd4d-131">**SWbemDateTime.MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
</dt> <dt>

[<span data-ttu-id="3dd4d-132">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="3dd4d-132">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="3dd4d-133">DateTime</span><span class="sxs-lookup"><span data-stu-id="3dd4d-133">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




