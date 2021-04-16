---
description: Konvertiert ein Datum im VT- \_ Datumsformat in das CIM-DateTime-Format.
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: "' Slibemdatetime. SetVarDate '-Methode (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetVarDate
- ISWbemDateTime.SetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8641bad2c59f100b689c74e23faf727bc80d2f49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348888"
---
# <a name="swbemdatetimesetvardate-method"></a><span data-ttu-id="02541-103">Slibemdatetime. SetVarDate-Methode</span><span class="sxs-lookup"><span data-stu-id="02541-103">SWbemDateTime.SetVarDate method</span></span>

<span data-ttu-id="02541-104">Die **SetVarDate** -Methode des [**"slibemdatetime**](swbemdatetime.md) "-Objekts konvertiert ein Datum im Format " **VT \_ Date** " in das [CIM-DateTime](date-and-time-format.md) -Format.</span><span class="sxs-lookup"><span data-stu-id="02541-104">The **SetVarDate** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date in the **VT\_DATE** format to the [CIM datetime](date-and-time-format.md) format.</span></span>

<span data-ttu-id="02541-105">Ein **VT- \_ Datums** Wert ist ein Variant-DateTime-Wert, der von Visual Basic und ActiveX verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="02541-105">A **VT\_DATE** value is a variant datetime value that Visual Basic and ActiveX use.</span></span>

<span data-ttu-id="02541-106">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="02541-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="02541-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="02541-107">Syntax</span></span>


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="02541-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="02541-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02541-109">*vdate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02541-109">*vdate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02541-110">Der Variant-Datumswert zum Festlegen des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="02541-110">The variant date value to set the object.</span></span> <span data-ttu-id="02541-111">Dieser Parameter muss das **VT \_ Date** -Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="02541-111">This parameter must be in the **VT\_DATE** format.</span></span>

</dd> <dt>

<span data-ttu-id="02541-112">*bislocal* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="02541-112">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="02541-113">Wenn **true**, wird *vdate* als Ortszeit interpretiert, und die koordinierte Weltzeit (UTC)-Eigenschaft enthält die Ortszeit, die in den korrekten UTC-Offset konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="02541-113">If **TRUE**, *vdate* is interpreted as a local time, and the Coordinated Universal Time (UTC) property contains the local time that is converted to the correct UTC offset.</span></span> <span data-ttu-id="02541-114">Wenn *bislocal den* Wert **false** aufweist, wird *vdate* direkt in einen UTC-Wert mit einem Offset von 0 (null) konvertiert.</span><span class="sxs-lookup"><span data-stu-id="02541-114">When *bIsLocal* is **FALSE**, then *vdate* is converted directly into a UTC value with an offset of zero (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02541-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02541-115">Return value</span></span>

<span data-ttu-id="02541-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="02541-116">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="02541-117">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="02541-117">Error codes</span></span>

<span data-ttu-id="02541-118">Nach Abschluss der **SetVarDate** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt den Fehlercode in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="02541-118">After completing the **SetVarDate** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="02541-119">**wbemErrInvalidSyntax** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="02541-119">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="02541-120">Das Format von *vdate* ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="02541-120">The format of *vdate* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02541-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02541-121">Remarks</span></span>

<span data-ttu-id="02541-122">Nach einem erfolgreichen Aufruf von **SetVarDate** wird der [**DateTime**](datetime.md) -Wert als absoluter DateTime-Wert anstelle eines Intervalls interpretiert, und die [**isinterval**](swbemdatetime-isinterval.md) -Eigenschaft ist auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="02541-122">After a successful call to **SetVarDate**, the [**DATETIME**](datetime.md) value is interpreted as an absolute datetime value instead of an interval, and the [**IsInterval**](swbemdatetime-isinterval.md) property is set to **FALSE**.</span></span>

<span data-ttu-id="02541-123">Die intrinsische Visual Basic-oder VBScript-Funktion [CDate](/previous-versions//2dt118h2(v=vs.85)) stellt einen [**DateTime**](datetime.md) -Wert im **VT- \_ Datums** Format für die Eingabe in **SetVarDate** bereit.</span><span class="sxs-lookup"><span data-stu-id="02541-123">The intrinsic Visual Basic or VBScript function [CDate](/previous-versions//2dt118h2(v=vs.85)) provides a [**datetime**](datetime.md) value in the **VT\_DATE** format for input to **SetVarDate**.</span></span>

## <a name="examples"></a><span data-ttu-id="02541-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02541-124">Examples</span></span>

<span data-ttu-id="02541-125">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="02541-125">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="02541-126">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="02541-126">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

<span data-ttu-id="02541-127">Im Codebeispiel [Convert Date to WMI Date-Time Format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript in der TechNet Gallery wird SetVarDate verwendet, um einen regulären Datums-/Uhrzeitwert in das UTC-Datums-/Uhrzeitformat zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="02541-127">The [Convert Date to WMI Date-Time Format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript code sample in the TechNet Gallery uses SetVarDate to convert a regular date-time value into the UTC date-time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="02541-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02541-128">Requirements</span></span>



| <span data-ttu-id="02541-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02541-129">Requirement</span></span> | <span data-ttu-id="02541-130">Wert</span><span class="sxs-lookup"><span data-stu-id="02541-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02541-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02541-131">Minimum supported client</span></span><br/> | <span data-ttu-id="02541-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02541-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02541-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02541-133">Minimum supported server</span></span><br/> | <span data-ttu-id="02541-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02541-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02541-135">Header</span><span class="sxs-lookup"><span data-stu-id="02541-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="02541-136"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="02541-136"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="02541-137">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="02541-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="02541-138"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="02541-138"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="02541-139">DLL</span><span class="sxs-lookup"><span data-stu-id="02541-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02541-140"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02541-140"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="02541-141">CLSID</span><span class="sxs-lookup"><span data-stu-id="02541-141">CLSID</span></span><br/>                    | <span data-ttu-id="02541-142">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="02541-142">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="02541-143">IID</span><span class="sxs-lookup"><span data-stu-id="02541-143">IID</span></span><br/>                      | <span data-ttu-id="02541-144">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="02541-144">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="02541-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02541-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02541-146">**' Swap DateTime. SetFileTime '**</span><span class="sxs-lookup"><span data-stu-id="02541-146">**SWbemDateTime.SetFileTime**</span></span>](swbemdatetime-setfiletime.md)
</dt> <dt>

[<span data-ttu-id="02541-147">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="02541-147">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="02541-148">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="02541-148">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

