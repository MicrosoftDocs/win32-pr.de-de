---
description: Ruft die koordinierte Weltzeit (UTC) des DateTime-Werts ab oder legt diese fest.
ms.assetid: 43d9d0c8-5521-410f-825b-6b00c3dd0039
ms.tgt_platform: multiple
title: Taubemdatetime. UTC-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTC
- ISWbemDateTime.UTC
- ISWbemDateTime.get_UTC
- ISWbemDateTime.put_UTC
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 80a4c32e47b94289f66999fdbf1f7daf5f9f03cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360168"
---
# <a name="swbemdatetimeutc-property"></a><span data-ttu-id="b572c-103">Taubemdatetime. UTC (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b572c-103">SWbemDateTime.UTC property</span></span>

<span data-ttu-id="b572c-104">Die **UTC** -Eigenschaft des " [**Swap DateTime**](swbemdatetime.md) "-Objekts Ruft die koordinierte Weltzeit (UTC) des **DateTime** -Werts ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="b572c-104">The **UTC** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets the Coordinated Universal Times (UTC) representation of the **datetime** value.</span></span> <span data-ttu-id="b572c-105">UTC ist die Zeit, die durch den Welt Zeit Standard festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b572c-105">UTC is the time as set by the World Time Standard.</span></span> <span data-ttu-id="b572c-106">Die UTC hat eine Ortszeit (GMT) ersetzt.</span><span class="sxs-lookup"><span data-stu-id="b572c-106">UTC has replaced Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="b572c-107">Ein UTC-Wert mit einem Offset von 0 (null) entspricht der GMT-Abweichung mit einem Offset von 0.</span><span class="sxs-lookup"><span data-stu-id="b572c-107">A UTC value with a zero offset is the same as GMT with a zero offset.</span></span> <span data-ttu-id="b572c-108">Die Zahl mit Vorzeichen muss im Bereich von-720 bis 720 liegen, oder der Fehler **wbemErrValueOutOfRange** wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b572c-108">The signed number must be in the range of -720 through 720 or the error **wbemErrValueOutOfRange** is returned.</span></span>

<span data-ttu-id="b572c-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b572c-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="b572c-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b572c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b572c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="b572c-111">Syntax</span></span>


```VB
SWbemDateTime.UTC As Long
```



## <a name="property-value"></a><span data-ttu-id="b572c-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b572c-112">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="b572c-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b572c-113">Error codes</span></span>

<span data-ttu-id="b572c-114">Nachdem Sie die **UTC** -Eigenschaft erhalten oder festgelegt haben, enthält das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt möglicherweise den folgenden Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b572c-114">After you get or set the **UTC** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="b572c-115">**wbemErrValueOutOfRange** -2147749931 (0x8004102b)</span><span class="sxs-lookup"><span data-stu-id="b572c-115">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="b572c-116">Der Wert lag nicht im Bereich von-720 bis 720.</span><span class="sxs-lookup"><span data-stu-id="b572c-116">The value was not in the range of -720 through 720.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b572c-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b572c-117">Examples</span></span>

<span data-ttu-id="b572c-118">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="b572c-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="b572c-119">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="b572c-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b572c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b572c-120">Requirements</span></span>



| <span data-ttu-id="b572c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b572c-121">Requirement</span></span> | <span data-ttu-id="b572c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b572c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b572c-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b572c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b572c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b572c-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b572c-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b572c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b572c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b572c-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b572c-127">Header</span><span class="sxs-lookup"><span data-stu-id="b572c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b572c-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b572c-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b572c-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b572c-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="b572c-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b572c-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b572c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b572c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b572c-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b572c-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b572c-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="b572c-133">CLSID</span></span><br/>                    | <span data-ttu-id="b572c-134">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="b572c-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="b572c-135">IID</span><span class="sxs-lookup"><span data-stu-id="b572c-135">IID</span></span><br/>                      | <span data-ttu-id="b572c-136">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="b572c-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="b572c-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b572c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b572c-138">**' Taubemdatetime. utc' angegeben**</span><span class="sxs-lookup"><span data-stu-id="b572c-138">**SWbemDateTime.UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)
</dt> <dt>

[<span data-ttu-id="b572c-139">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="b572c-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="b572c-140">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="b572c-140">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

