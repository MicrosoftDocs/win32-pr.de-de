---
description: Konvertiert einen Datums-und Uhrzeitwert im CIM-DateTime-Format in das VT \_ Date-Format.
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: "' Slibemdatetime. getVarDate '-Methode (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d0c71e4748774eacab4b234092178179a4a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348287"
---
# <a name="swbemdatetimegetvardate-method"></a><span data-ttu-id="dfd8f-103">Slibemdatetime. getVarDate-Methode</span><span class="sxs-lookup"><span data-stu-id="dfd8f-103">SWbemDateTime.GetVarDate method</span></span>

<span data-ttu-id="dfd8f-104">Die **getVarDate** -Methode des " [**slibemdatetime**](swbemdatetime.md) "-Objekts konvertiert einen Datums-und Uhrzeitwert im CIM- [**DateTime**](datetime.md) -Format in das **VT \_ Date** -Format.</span><span class="sxs-lookup"><span data-stu-id="dfd8f-104">The **GetVarDate** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date and time value in the CIM [**DATETIME**](datetime.md) format to the **VT\_DATE** format.</span></span>

<span data-ttu-id="dfd8f-105">Das **VT \_ Date** -Format ist ein [**DateTime**](datetime.md) -Wert für die Automatisierung, der von Visual Basic und ActiveX verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dfd8f-105">The **VT\_DATE** format is an automation variant [**DATETIME**](datetime.md) value that Visual Basic and ActiveX use.</span></span>

<span data-ttu-id="dfd8f-106">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="dfd8f-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dfd8f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfd8f-107">Syntax</span></span>


```VB
vdate = .GetVarDate( _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="dfd8f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfd8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfd8f-109">*bislocal* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="dfd8f-109">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd8f-110">Gibt an, ob der zurückgegebene Wert als Ortszeit interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="dfd8f-110">Indicates whether the returned value is interpreted as local time.</span></span> <span data-ttu-id="dfd8f-111">Die koordinierte Weltzeit (UTC)-Eigenschaft enthält die Ortszeit, die in den korrekten UTC-Offset konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="dfd8f-111">The Coordinated Universal Time (UTC) property contains the local time converted to the correct UTC offset.</span></span> <span data-ttu-id="dfd8f-112">Wenn der Wert **false** ist, wird der Wert als UTC mit einem Offset von 0 (null) interpretiert.</span><span class="sxs-lookup"><span data-stu-id="dfd8f-112">If the value is **FALSE**, then the value is interpreted as UTC with a zero (0) offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfd8f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfd8f-113">Return value</span></span>

<span data-ttu-id="dfd8f-114">Der Datums-und Uhrzeitwert im **VT- \_ Datums** Format.</span><span class="sxs-lookup"><span data-stu-id="dfd8f-114">The date and time value in the **VT\_DATE** format.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfd8f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfd8f-115">Remarks</span></span>

<span data-ttu-id="dfd8f-116">**VT \_ Datums** -und **FILETIME** -Werte dürfen keine Platzhalter Felder enthalten.</span><span class="sxs-lookup"><span data-stu-id="dfd8f-116">**VT\_DATE** and **FILETIME** values cannot contain wildcard fields.</span></span>

<span data-ttu-id="dfd8f-117">Die **getVarDate** -Methode schlägt fehl (**wbemErrFailed**), wenn eine der folgenden Eigenschaften **false** ist:</span><span class="sxs-lookup"><span data-stu-id="dfd8f-117">The **GetVarDate** method fails (**wbemErrFailed**) if any of the following properties are **FALSE**:</span></span>

-   [<span data-ttu-id="dfd8f-118">**Yearfest gelegt**</span><span class="sxs-lookup"><span data-stu-id="dfd8f-118">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
-   [<span data-ttu-id="dfd8f-119">**Monthspezifiziert**</span><span class="sxs-lookup"><span data-stu-id="dfd8f-119">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
-   [<span data-ttu-id="dfd8f-120">**Dayangegeben**</span><span class="sxs-lookup"><span data-stu-id="dfd8f-120">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
-   [<span data-ttu-id="dfd8f-121">**Sansangegeben**</span><span class="sxs-lookup"><span data-stu-id="dfd8f-121">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
-   [<span data-ttu-id="dfd8f-122">**Minutesangegeben**</span><span class="sxs-lookup"><span data-stu-id="dfd8f-122">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
-   [<span data-ttu-id="dfd8f-123">**Secondsspezifiziert**</span><span class="sxs-lookup"><span data-stu-id="dfd8f-123">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
-   [<span data-ttu-id="dfd8f-124">**' Mikroseconds' angegeben**</span><span class="sxs-lookup"><span data-stu-id="dfd8f-124">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
-   [<span data-ttu-id="dfd8f-125">**Utcangegeben**</span><span class="sxs-lookup"><span data-stu-id="dfd8f-125">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)

<span data-ttu-id="dfd8f-126">Bei erfolgreicher Rückgabe von [**SetVarDate**](swbemdatetime-setvardate.md)werden alle diese Eigenschaften auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dfd8f-126">On successful return from [**SetVarDate**](swbemdatetime-setvardate.md), all of these properties are set to **TRUE**.</span></span>

<span data-ttu-id="dfd8f-127">Nach einem erfolgreichen Aufruf von [**SetVarDate**](swbemdatetime-setvardate.md)wird der [**DateTime**](datetime.md) -Wert immer als absoluter **DateTime** -Wert anstelle eines Intervalls interpretiert, und [**isinterval**](swbemdatetime-isinterval.md) ist auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dfd8f-127">After a successful call to [**SetVarDate**](swbemdatetime-setvardate.md), the [**DATETIME**](datetime.md) value is always interpreted as an absolute **DATETIME** value instead of an interval, and the [**IsInterval**](swbemdatetime-isinterval.md) is set to **FALSE**.</span></span>

<span data-ttu-id="dfd8f-128">Wenn [**isinterval**](swbemdatetime-isinterval.md) auf **true** festgelegt ist, führt ein Rückruf von **getVarDate** zu einem **wbemErrFailed** -Fehler.</span><span class="sxs-lookup"><span data-stu-id="dfd8f-128">If [**IsInterval**](swbemdatetime-isinterval.md) is set to **TRUE**, then a call to **GetVarDate** results in the **wbemErrFailed** error.</span></span>

<span data-ttu-id="dfd8f-129">Ein Genauigkeits Verlust tritt auf, wenn Sie **getVarDate** aufrufen, da [DateTime](datetime.md) -Werte eine Auflösung von einer Mikrosekunde (n) aufweisen und die **VT \_ Date** -Werte eine 500 Millisekunde-Auflösung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dfd8f-129">Some loss of precision occurs when you call **GetVarDate**, because [datetime](datetime.md) values have a one microsecond ( s) resolution, and **VT\_DATE** values have a 500 millisecond resolution.</span></span>

## <a name="examples"></a><span data-ttu-id="dfd8f-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dfd8f-130">Examples</span></span>

<span data-ttu-id="dfd8f-131">Beispiele für die Verwendung des [**"slibemdatetime**](swbemdatetime.md) "-Objekts zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datumsangaben und Uhrzeiten](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="dfd8f-131">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="dfd8f-132">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="dfd8f-132">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfd8f-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfd8f-133">Requirements</span></span>



| <span data-ttu-id="dfd8f-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfd8f-134">Requirement</span></span> | <span data-ttu-id="dfd8f-135">Wert</span><span class="sxs-lookup"><span data-stu-id="dfd8f-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfd8f-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dfd8f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dfd8f-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfd8f-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dfd8f-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dfd8f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dfd8f-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfd8f-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dfd8f-140">Header</span><span class="sxs-lookup"><span data-stu-id="dfd8f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfd8f-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfd8f-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dfd8f-142">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="dfd8f-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="dfd8f-143"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dfd8f-143"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dfd8f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="dfd8f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfd8f-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfd8f-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dfd8f-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="dfd8f-146">CLSID</span></span><br/>                    | <span data-ttu-id="dfd8f-147">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="dfd8f-147">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="dfd8f-148">IID</span><span class="sxs-lookup"><span data-stu-id="dfd8f-148">IID</span></span><br/>                      | <span data-ttu-id="dfd8f-149">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="dfd8f-149">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="dfd8f-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfd8f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfd8f-151">**' Swap DateTime. GetFileTime '**</span><span class="sxs-lookup"><span data-stu-id="dfd8f-151">**SWbemDateTime.GetFileTime**</span></span>](swbemdatetime-getfiletime.md)
</dt> <dt>

[<span data-ttu-id="dfd8f-152">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="dfd8f-152">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="dfd8f-153">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfd8f-153">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




