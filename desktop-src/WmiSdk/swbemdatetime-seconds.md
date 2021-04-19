---
description: Ruft einen Wert ab, der die Sekunden Komponente des DateTime-Werts darstellt, oder legt diesen fest.
ms.assetid: 194d4309-6abf-4c5f-99f8-60d2c835af6c
ms.tgt_platform: multiple
title: Swap DateTime. seconds-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Seconds
- ISWbemDateTime.Seconds
- ISWbemDateTime.get_Seconds
- ISWbemDateTime.put_Seconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0ef4ef15f13bf3d8dfc9272b2a3b734c3678f8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353205"
---
# <a name="swbemdatetimeseconds-property"></a><span data-ttu-id="cb8e7-103">Swap DateTime. seconds (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cb8e7-103">SWbemDateTime.Seconds property</span></span>

<span data-ttu-id="cb8e7-104">Die **seconds** -Eigenschaft des " [**Swap DateTime**](swbemdatetime.md) "-Objekts Ruft einen Wert ab, der die Sekunden Komponente des DateTime-Werts darstellt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="cb8e7-104">The **Seconds** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the seconds component of the datetime value.</span></span>

<span data-ttu-id="cb8e7-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="cb8e7-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="cb8e7-106">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="cb8e7-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb8e7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb8e7-107">Syntax</span></span>


```VB
SWbemDateTime.Seconds As Long
```



## <a name="property-value"></a><span data-ttu-id="cb8e7-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cb8e7-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="cb8e7-109">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="cb8e7-109">Error codes</span></span>

<span data-ttu-id="cb8e7-110">Nachdem Sie die **seconds** -Eigenschaft festgelegt oder festgelegt haben, enthält das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt möglicherweise den folgenden Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="cb8e7-110">After you get or set the **Seconds** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="cb8e7-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102b)</span><span class="sxs-lookup"><span data-stu-id="cb8e7-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="cb8e7-112">Der Wert lag nicht im Bereich von 0 bis 59.</span><span class="sxs-lookup"><span data-stu-id="cb8e7-112">The value was not in the range of 0 through 59.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb8e7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb8e7-113">Remarks</span></span>

<span data-ttu-id="cb8e7-114">Die Eigenschaft " **Swap DateTime. seconds** " kann einen falschen Wert enthalten, wenn die Eigenschaft " [**Swap DateTime. minutes**](swbemdatetime-minutes.md) " auf 1 festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="cb8e7-114">The **SWbemDateTime.Seconds** property may contain an incorrect value if the [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) property has been set to 1.</span></span> <span data-ttu-id="cb8e7-115">Sie enthält einen Wert, der aufgrund eines Rundungs Fehlers, der auftritt, wenn ein CIM- [**DateTime**](datetime.md) -Wert in einen VT- **\_ Datums** Wert übersetzt wird, um eine Sekunde versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="cb8e7-115">It contains a value that is offset by one second because of a rounding error that occurs when a CIM [**DATETIME**](datetime.md) value is translated to a **VT\_DATE** value.</span></span> <span data-ttu-id="cb8e7-116">Wenn die Eigenschaft **Minutes** stattdessen auf 0 (null) festgelegt ist, gibt die **seconds** -Eigenschaft den richtigen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cb8e7-116">If the **Minutes** property is set to 0 (zero) instead, then the **Seconds** property returns the correct value.</span></span>

## <a name="examples"></a><span data-ttu-id="cb8e7-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb8e7-117">Examples</span></span>

<span data-ttu-id="cb8e7-118">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="cb8e7-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="cb8e7-119">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="cb8e7-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb8e7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb8e7-120">Requirements</span></span>



| <span data-ttu-id="cb8e7-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb8e7-121">Requirement</span></span> | <span data-ttu-id="cb8e7-122">Wert</span><span class="sxs-lookup"><span data-stu-id="cb8e7-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb8e7-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb8e7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cb8e7-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb8e7-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cb8e7-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb8e7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cb8e7-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb8e7-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cb8e7-127">Header</span><span class="sxs-lookup"><span data-stu-id="cb8e7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb8e7-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb8e7-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb8e7-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="cb8e7-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="cb8e7-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cb8e7-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cb8e7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="cb8e7-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb8e7-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb8e7-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cb8e7-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="cb8e7-133">CLSID</span></span><br/>                    | <span data-ttu-id="cb8e7-134">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="cb8e7-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="cb8e7-135">IID</span><span class="sxs-lookup"><span data-stu-id="cb8e7-135">IID</span></span><br/>                      | <span data-ttu-id="cb8e7-136">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="cb8e7-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="cb8e7-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb8e7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb8e7-138">**' Taubemdatetime. seconds' angegeben**</span><span class="sxs-lookup"><span data-stu-id="cb8e7-138">**SWbemDateTime.SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
</dt> <dt>

[<span data-ttu-id="cb8e7-139">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="cb8e7-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="cb8e7-140">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="cb8e7-140">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

