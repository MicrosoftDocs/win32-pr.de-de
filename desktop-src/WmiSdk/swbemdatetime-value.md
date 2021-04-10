---
description: Ruft das RAW-CIM-Datum im DMTF-Format (verteilter Verwaltungs Task Force) ab oder legt es fest.
ms.assetid: 426a60d5-c364-406e-8346-049a13d59c7f
ms.tgt_platform: multiple
title: "' Taubemdatetime. Value '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Value
- ISWbemDateTime.Value
- ISWbemDateTime.get_Value
- ISWbemDateTime.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2ecb3a42a865559ba9b3c3e5fbec7302f975fa0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130992"
---
# <a name="swbemdatetimevalue-property"></a><span data-ttu-id="63adc-103">Swap DateTime. Value-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="63adc-103">SWbemDateTime.Value property</span></span>

<span data-ttu-id="63adc-104">Die **value** -Eigenschaft des " [**slibemdatetime**](swbemdatetime.md) "-Objekts Ruft das RAW-CIM-Datum im DMTF-Format (verteilter Verwaltungs Task Force) ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="63adc-104">The **Value** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets the raw CIM date in the DMTF (Distributed Management Task Force) format.</span></span> <span data-ttu-id="63adc-105">Das DMTF-Format ist eine Zeichen folgen Darstellung des [**DateTime**](datetime.md) -Werts.</span><span class="sxs-lookup"><span data-stu-id="63adc-105">The DMTF format is a string representation of the [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="63adc-106">Diese Eigenschaft ist die Standard Eigenschaft für " **Swap DateTime** "-Objekte.</span><span class="sxs-lookup"><span data-stu-id="63adc-106">This property is the default property for **SWbemDateTime** objects.</span></span> <span data-ttu-id="63adc-107">Die **value** -Eigenschaft hat den Standardwert 00000101000000.000000 + 000.</span><span class="sxs-lookup"><span data-stu-id="63adc-107">The **Value** property has a default value of 00000101000000.000000+000.</span></span>

<span data-ttu-id="63adc-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="63adc-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="63adc-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="63adc-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="63adc-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="63adc-110">Syntax</span></span>


```VB
SWbemDateTime.Value As String
```



## <a name="property-value"></a><span data-ttu-id="63adc-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="63adc-111">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="63adc-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="63adc-112">Error codes</span></span>

<span data-ttu-id="63adc-113">Nachdem Sie die **value** -Eigenschaft erhalten oder festgelegt haben, enthält das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt möglicherweise den folgenden Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="63adc-113">After you get or set the **Value** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="63adc-114">**wbemErrInvalidSyntax** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="63adc-114">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="63adc-115">Das Format von " *strevalue* " ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="63adc-115">The format of *strValue* is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="63adc-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63adc-116">Examples</span></span>

<span data-ttu-id="63adc-117">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="63adc-117">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="63adc-118">Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="63adc-118">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="63adc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63adc-119">Requirements</span></span>



| <span data-ttu-id="63adc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63adc-120">Requirement</span></span> | <span data-ttu-id="63adc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="63adc-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63adc-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63adc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="63adc-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63adc-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="63adc-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63adc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="63adc-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63adc-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="63adc-126">Header</span><span class="sxs-lookup"><span data-stu-id="63adc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="63adc-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="63adc-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="63adc-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="63adc-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="63adc-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="63adc-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="63adc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="63adc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63adc-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63adc-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="63adc-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="63adc-132">CLSID</span></span><br/>                    | <span data-ttu-id="63adc-133">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="63adc-133">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="63adc-134">IID</span><span class="sxs-lookup"><span data-stu-id="63adc-134">IID</span></span><br/>                      | <span data-ttu-id="63adc-135">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="63adc-135">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="63adc-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63adc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63adc-137">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="63adc-137">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="63adc-138">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="63adc-138">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

