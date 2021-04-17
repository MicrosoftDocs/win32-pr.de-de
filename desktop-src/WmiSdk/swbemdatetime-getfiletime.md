---
description: Konvertiert einen Datums-und Uhrzeitwert im CIM-DateTime-Format in das FILETIME-Format.
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: Methode ' Swap DateTime. GetFileTime ' (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3f8a8c85cb4c78be578187b1f55afce078fe7bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485731"
---
# <a name="swbemdatetimegetfiletime-method"></a><span data-ttu-id="db6a8-103">Methode ' Swap DateTime. GetFileTime '</span><span class="sxs-lookup"><span data-stu-id="db6a8-103">SWbemDateTime.GetFileTime method</span></span>

<span data-ttu-id="db6a8-104">Die **GetFileTime** -Methode des " [**slibemdatetime**](swbemdatetime.md) "-Objekts konvertiert einen Datums-und Uhrzeitwert im CIM- [DateTime](datetime.md) -Format in das FILETIME-Format.</span><span class="sxs-lookup"><span data-stu-id="db6a8-104">The **GetFileTime** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date and time value in the CIM [DATETIME](datetime.md) format to the FILETIME format.</span></span>

<span data-ttu-id="db6a8-105">Wenn der-Parameter auf **true** festgelegt ist, stellt der Rückgabewert eine Ortszeit für den Client dar.</span><span class="sxs-lookup"><span data-stu-id="db6a8-105">If the parameter is set to **TRUE**, then the return value represents a local time for the client.</span></span> <span data-ttu-id="db6a8-106">Andernfalls ist der Rückgabewert eine koordinierte Weltzeit (UTC).</span><span class="sxs-lookup"><span data-stu-id="db6a8-106">Otherwise, the return value is a Coordinated Universal Time (UTC) time.</span></span> <span data-ttu-id="db6a8-107">Eine **FILETIME** - [DateTime](datetime.md) -Struktur ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Einheiten seit dem Beginn des 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="db6a8-107">A **FILETIME** [DATETIME](datetime.md) structure is a 64-bit value that represents the number of 100-nanosecond units since the beginning of January 1, 1601.</span></span> <span data-ttu-id="db6a8-108">Windows-Verwaltungsinstrumentation (WMI) behandelt **FILETIME** -Werte als Zeichen folgen Darstellungen von nicht signierten 64-Bit-Zahlen.</span><span class="sxs-lookup"><span data-stu-id="db6a8-108">Windows Management Instrumentation (WMI) treats **FILETIME** values as string representations of unsigned 64-bit numbers.</span></span>

<span data-ttu-id="db6a8-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="db6a8-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="db6a8-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="db6a8-110">Syntax</span></span>


```VB
vDate = .GetFileTime( _
  [ ByVal bIsLocaL ] _
)
```



## <a name="parameters"></a><span data-ttu-id="db6a8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="db6a8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db6a8-112">*bislocal* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="db6a8-112">*bIsLocaL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="db6a8-113">Gibt an, ob der zurückgegebene Wert als Ortszeit interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="db6a8-113">Indicates whether the returned value is interpreted as local time.</span></span> <span data-ttu-id="db6a8-114">Die UTC-Eigenschaft enthält dann die Ortszeit, die in den richtigen UTC-Offset (koordinierte Weltzeit) konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="db6a8-114">The UTC property then contains the local time converted to the correct Coordinated Universal Times (UTC) offset.</span></span> <span data-ttu-id="db6a8-115">Wenn der Wert **false** ist, wird der Wert als UTC mit einem Offset von 0 (null) interpretiert.</span><span class="sxs-lookup"><span data-stu-id="db6a8-115">If the value is **FALSE**, then the value is interpreted as UTC with a zero (0) offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db6a8-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db6a8-116">Return value</span></span>

<span data-ttu-id="db6a8-117">Das Datum und die Uhrzeit im **FILETIME** -Format.</span><span class="sxs-lookup"><span data-stu-id="db6a8-117">The date and time in the **FILETIME** format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="db6a8-118">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="db6a8-118">Error codes</span></span>

<span data-ttu-id="db6a8-119">Nach dem Abschließen der **GetFileTime** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt den Fehlercode in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="db6a8-119">After completing the **GetFileTime** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="db6a8-120">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="db6a8-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="db6a8-121">Der Aufruf schlug fehl.</span><span class="sxs-lookup"><span data-stu-id="db6a8-121">The call failed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db6a8-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db6a8-122">Remarks</span></span>

<span data-ttu-id="db6a8-123">**VT \_ Datums** -und **FILETIME** -Werte dürfen keine Platzhalter Felder enthalten.</span><span class="sxs-lookup"><span data-stu-id="db6a8-123">**VT\_DATE** and **FILETIME** values cannot contain wildcard fields.</span></span>

<span data-ttu-id="db6a8-124">Bei der **GetFileTime** -Methode tritt ein Fehler auf (wbemErrFailed), wenn eine der folgenden Eigenschaften **false** ist:</span><span class="sxs-lookup"><span data-stu-id="db6a8-124">The **GetFileTime** method fails (wbemErrFailed) if any of the following properties are **FALSE**:</span></span>

-   [<span data-ttu-id="db6a8-125">**Yearfest gelegt**</span><span class="sxs-lookup"><span data-stu-id="db6a8-125">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
-   [<span data-ttu-id="db6a8-126">**Monthspezifiziert**</span><span class="sxs-lookup"><span data-stu-id="db6a8-126">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
-   [<span data-ttu-id="db6a8-127">**Dayangegeben**</span><span class="sxs-lookup"><span data-stu-id="db6a8-127">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
-   [<span data-ttu-id="db6a8-128">**Sansangegeben**</span><span class="sxs-lookup"><span data-stu-id="db6a8-128">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
-   [<span data-ttu-id="db6a8-129">**Minutesangegeben**</span><span class="sxs-lookup"><span data-stu-id="db6a8-129">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
-   [<span data-ttu-id="db6a8-130">**Secondsspezifiziert**</span><span class="sxs-lookup"><span data-stu-id="db6a8-130">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
-   [<span data-ttu-id="db6a8-131">**' Mikroseconds' angegeben**</span><span class="sxs-lookup"><span data-stu-id="db6a8-131">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
-   [<span data-ttu-id="db6a8-132">**Utcangegeben**</span><span class="sxs-lookup"><span data-stu-id="db6a8-132">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)

<span data-ttu-id="db6a8-133">Bei erfolgreicher Rückgabe von [**SetFileTime**](swbemdatetime-setfiletime.md)werden alle diese Eigenschaften auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="db6a8-133">On a successful return from [**SetFileTime**](swbemdatetime-setfiletime.md), all of these properties are set to **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="db6a8-134">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db6a8-134">Examples</span></span>

<span data-ttu-id="db6a8-135">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="db6a8-135">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="db6a8-136">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="db6a8-136">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="db6a8-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db6a8-137">Requirements</span></span>



| <span data-ttu-id="db6a8-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db6a8-138">Requirement</span></span> | <span data-ttu-id="db6a8-139">Wert</span><span class="sxs-lookup"><span data-stu-id="db6a8-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db6a8-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db6a8-140">Minimum supported client</span></span><br/> | <span data-ttu-id="db6a8-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db6a8-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="db6a8-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db6a8-142">Minimum supported server</span></span><br/> | <span data-ttu-id="db6a8-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db6a8-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="db6a8-144">Header</span><span class="sxs-lookup"><span data-stu-id="db6a8-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="db6a8-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="db6a8-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="db6a8-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="db6a8-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="db6a8-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="db6a8-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="db6a8-148">DLL</span><span class="sxs-lookup"><span data-stu-id="db6a8-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db6a8-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db6a8-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="db6a8-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="db6a8-150">CLSID</span></span><br/>                    | <span data-ttu-id="db6a8-151">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="db6a8-151">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="db6a8-152">IID</span><span class="sxs-lookup"><span data-stu-id="db6a8-152">IID</span></span><br/>                      | <span data-ttu-id="db6a8-153">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="db6a8-153">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="db6a8-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db6a8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db6a8-155">**"Slibemdatetime. getVarDate"**</span><span class="sxs-lookup"><span data-stu-id="db6a8-155">**SWbemDateTime.GetVarDate**</span></span>](swbemdatetime-getvardate.md)
</dt> <dt>

[<span data-ttu-id="db6a8-156">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="db6a8-156">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="db6a8-157">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="db6a8-157">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

