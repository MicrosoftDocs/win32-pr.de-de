---
description: Ruft einen Wert ab, der die Mikrosekunden Komponente des DateTime-Werts darstellt, oder legt diesen fest.
ms.assetid: b810b781-86a3-4730-8114-44d10454f7c3
ms.tgt_platform: multiple
title: Swap DateTime. Mikro seconds-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Microseconds
- ISWbemDateTime.Microseconds
- ISWbemDateTime.get_Microseconds
- ISWbemDateTime.put_Microseconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 94213eb70a98be1af8f8404ddece8bf2f07ca807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349619"
---
# <a name="swbemdatetimemicroseconds-property"></a><span data-ttu-id="3e02b-103">Swap DateTime. Mikro seconds (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3e02b-103">SWbemDateTime.Microseconds property</span></span>

<span data-ttu-id="3e02b-104">Die **Mikro seconds** -Eigenschaft des-Objekts von " [**Swap DateTime**](swbemdatetime.md) " Ruft einen Wert ab, der die Mikrosekunden Komponente des DateTime-Werts darstellt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="3e02b-104">The **Microseconds** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the microseconds component of the datetime value.</span></span>

<span data-ttu-id="3e02b-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3e02b-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="3e02b-106">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3e02b-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e02b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e02b-107">Syntax</span></span>


```VB
SWbemDateTime.Microseconds As Long
```



## <a name="property-value"></a><span data-ttu-id="3e02b-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3e02b-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e02b-109">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3e02b-109">Error codes</span></span>

<span data-ttu-id="3e02b-110">Nachdem Sie die **Mikrosekunden** -Eigenschaft erhalten oder festgelegt haben, enthält das **Err** -Objekt möglicherweise den folgenden Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="3e02b-110">After you get or set the **Microseconds** property, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="3e02b-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102b)</span><span class="sxs-lookup"><span data-stu-id="3e02b-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="3e02b-112">Der Wert lag nicht im Bereich von 0 bis 999999.</span><span class="sxs-lookup"><span data-stu-id="3e02b-112">The value was not in the range of 0 through 999999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="3e02b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e02b-113">Examples</span></span>

<span data-ttu-id="3e02b-114">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="3e02b-114">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="3e02b-115">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="3e02b-115">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e02b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e02b-116">Requirements</span></span>



| <span data-ttu-id="3e02b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e02b-117">Requirement</span></span> | <span data-ttu-id="3e02b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3e02b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e02b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e02b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3e02b-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e02b-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e02b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e02b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3e02b-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e02b-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e02b-123">Header</span><span class="sxs-lookup"><span data-stu-id="3e02b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e02b-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e02b-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e02b-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3e02b-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="3e02b-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3e02b-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3e02b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3e02b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e02b-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e02b-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3e02b-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="3e02b-129">CLSID</span></span><br/>                    | <span data-ttu-id="3e02b-130">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="3e02b-130">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="3e02b-131">IID</span><span class="sxs-lookup"><span data-stu-id="3e02b-131">IID</span></span><br/>                      | <span data-ttu-id="3e02b-132">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="3e02b-132">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="3e02b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e02b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e02b-134">**' Swap DateTime. Mikro seconds' angegeben**</span><span class="sxs-lookup"><span data-stu-id="3e02b-134">**SWbemDateTime.MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
</dt> <dt>

[<span data-ttu-id="3e02b-135">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="3e02b-135">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="3e02b-136">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="3e02b-136">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

 




