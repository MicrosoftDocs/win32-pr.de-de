---
description: Konvertiert ein Datum im FILETIME-Zeichen folgen Format in das CIM-DateTime-Format.
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: Taubemdatetime. SetFileTime-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ca3e36a284e3700e166e86f6786218bada8f369e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130993"
---
# <a name="swbemdatetimesetfiletime-method"></a><span data-ttu-id="c498e-103">Taubemdatetime. SetFileTime-Methode</span><span class="sxs-lookup"><span data-stu-id="c498e-103">SWbemDateTime.SetFileTime method</span></span>

<span data-ttu-id="c498e-104">Die **SetFileTime** -Methode des " [**slibemdatetime**](swbemdatetime.md) "-Objekts konvertiert ein Datum im **FILETIME** -Format der Zeichenfolge in das [CIM-DateTime](date-and-time-format.md) -Format.</span><span class="sxs-lookup"><span data-stu-id="c498e-104">The **SetFileTime** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date in the string **FILETIME** format to the [CIM datetime](date-and-time-format.md) format.</span></span>

<span data-ttu-id="c498e-105">Das **FILETIME** -Format ist eine 64-Bit-DateTime-Struktur, die die Anzahl der 100-Nanosecond-Einheiten seit dem Beginn des 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="c498e-105">The **FILETIME** format is a 64-bit datetime structure that represents the number of 100-nanosecond units since the beginning of January 1, 1601.</span></span> <span data-ttu-id="c498e-106">Windows-Verwaltungsinstrumentation (WMI) behandelt **FILETIME** -Werte als Zeichen folgen Darstellungen von nicht signierten 64-Bit-Zahlen.</span><span class="sxs-lookup"><span data-stu-id="c498e-106">Windows Management Instrumentation (WMI) treats **FILETIME** values as string representations of unsigned 64-bit numbers.</span></span>

<span data-ttu-id="c498e-107">Die Syntax Erklärung finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c498e-107">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c498e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c498e-108">Syntax</span></span>


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c498e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c498e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c498e-110">" *strinfiletime* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="c498e-110">*strFileTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c498e-111">Der **FILETIME** -Wert, der zum Festlegen des Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c498e-111">**FILETIME** value used to set the object.</span></span>

</dd> <dt>

<span data-ttu-id="c498e-112">*bislocal* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c498e-112">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c498e-113">**True** gibt an, dass " *strinfiletime* " als lokale Zeit interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="c498e-113">If **TRUE**, *strFileTime* is interpreted as a local time.</span></span> <span data-ttu-id="c498e-114">Die koordinierte Weltzeit (UTC)-Eigenschaft enthält die Ortszeit, die in den korrekten UTC-Offset konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c498e-114">The Coordinated Universal Time (UTC) property contains the local time converted to the correct UTC offset.</span></span> <span data-ttu-id="c498e-115">Wenn " *bislocal" den* Wert " **false**" aufweist, wird " *straufiletime* " direkt in einen UTC-Wert mit einem Offset von 0 (null) konvertiert.</span><span class="sxs-lookup"><span data-stu-id="c498e-115">When *bIsLocal* is **FALSE**, then *strFileTime* is converted directly into a UTC value with an offset of 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c498e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c498e-116">Return value</span></span>

<span data-ttu-id="c498e-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c498e-117">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c498e-118">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c498e-118">Error codes</span></span>

<span data-ttu-id="c498e-119">Nach dem Abschließen der **SetFileTime** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt den Fehlercode in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="c498e-119">After completing the **SetFileTime** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c498e-120">**wbemErrInvalidSyntax** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="c498e-120">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="c498e-121">Das Format von " *straufiletime* " ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c498e-121">The format of *strFileTime* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c498e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c498e-122">Remarks</span></span>

<span data-ttu-id="c498e-123">Nach einem erfolgreichen Aufruf von **SetFileTime** wird der [**DateTime**](datetime.md) -Wert immer als absoluter Wert (**DateTime**) interpretiert, und [**isinterval**](swbemdatetime-isinterval.md) ist auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c498e-123">After a successful call to **SetFileTime**, the [**datetime**](datetime.md) value is always interpreted as an absolute (**datetime**) value, and [**IsInterval**](swbemdatetime-isinterval.md) is set to **FALSE**.</span></span>

## <a name="examples"></a><span data-ttu-id="c498e-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c498e-124">Examples</span></span>

<span data-ttu-id="c498e-125">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="c498e-125">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="c498e-126">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="c498e-126">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c498e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c498e-127">Requirements</span></span>



| <span data-ttu-id="c498e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c498e-128">Requirement</span></span> | <span data-ttu-id="c498e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c498e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c498e-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c498e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c498e-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c498e-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c498e-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c498e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c498e-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c498e-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c498e-134">Header</span><span class="sxs-lookup"><span data-stu-id="c498e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c498e-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c498e-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c498e-136">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c498e-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="c498e-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c498e-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c498e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c498e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c498e-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c498e-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c498e-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="c498e-140">CLSID</span></span><br/>                    | <span data-ttu-id="c498e-141">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="c498e-141">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="c498e-142">IID</span><span class="sxs-lookup"><span data-stu-id="c498e-142">IID</span></span><br/>                      | <span data-ttu-id="c498e-143">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="c498e-143">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="c498e-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c498e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c498e-145">**Slibemdatetime. SetVarDate**</span><span class="sxs-lookup"><span data-stu-id="c498e-145">**SWbemDateTime.SetVarDate**</span></span>](swbemdatetime-setvardate.md)
</dt> <dt>

[<span data-ttu-id="c498e-146">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="c498e-146">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="c498e-147">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="c498e-147">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

