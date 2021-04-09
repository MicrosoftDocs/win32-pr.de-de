---
description: Vergleicht zwei Unicode-Zeichen folgen.
ms.assetid: D2703180-946C-4762-AFBA-1E882B01B944
title: Rtlcompareunicodestring-Funktion (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlCompareUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9de12f218c37916c7e30393c0701efcf1889973f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861056"
---
# <a name="rtlcompareunicodestring-function"></a><span data-ttu-id="7bd8a-103">Rtlcompareunicodestring-Funktion</span><span class="sxs-lookup"><span data-stu-id="7bd8a-103">RtlCompareUnicodeString function</span></span>

<span data-ttu-id="7bd8a-104">Vergleicht zwei Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="7bd8a-104">Compares two Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bd8a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bd8a-105">Syntax</span></span>


```C++
LONG RtlCompareUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a><span data-ttu-id="7bd8a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bd8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bd8a-107">*Zeichenfolge1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bd8a-107">*String1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bd8a-108">Zeiger auf die erste Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7bd8a-108">Pointer to the first string.</span></span>

</dd> <dt>

<span data-ttu-id="7bd8a-109">*Zeichenfolge2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bd8a-109">*String2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bd8a-110">Zeiger auf die zweite Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7bd8a-110">Pointer to the second string.</span></span>

</dd> <dt>

<span data-ttu-id="7bd8a-111">*CaseInsensitive* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bd8a-111">*CaseInSensitive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bd8a-112">**True** gibt an, dass die Groß-/Kleinschreibung beim Vergleich ignoriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7bd8a-112">If **TRUE**, case should be ignored when doing the comparison.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bd8a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7bd8a-113">Return value</span></span>

<span data-ttu-id="7bd8a-114">Ein Wert mit Vorzeichen, der die Ergebnisse des Vergleichs ergibt:</span><span class="sxs-lookup"><span data-stu-id="7bd8a-114">A signed value that gives the results of the comparison:</span></span>



| <span data-ttu-id="7bd8a-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7bd8a-115">Return code</span></span>                                                                               | <span data-ttu-id="7bd8a-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bd8a-116">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="7bd8a-117"><dt>**Zins**</dt></span><span class="sxs-lookup"><span data-stu-id="7bd8a-117"><dt>**Zero**</dt></span></span> </dl>       | <span data-ttu-id="7bd8a-118">*Zeichenfolge1* ist *Zeichenfolge2*.</span><span class="sxs-lookup"><span data-stu-id="7bd8a-118">*String1* equals *String2*.</span></span><br/>          |
| <dl> <span data-ttu-id="7bd8a-119"><dt>**< NULL**</dt></span><span class="sxs-lookup"><span data-stu-id="7bd8a-119"><dt>**< Zero**</dt></span></span> </dl>  | <span data-ttu-id="7bd8a-120">*Zeichenfolge1* ist kleiner als *Zeichenfolge2*.</span><span class="sxs-lookup"><span data-stu-id="7bd8a-120">*String1* is less than *String2*.</span></span><br/>    |
| <dl> <span data-ttu-id="7bd8a-121"><dt>**> NULL**</dt></span><span class="sxs-lookup"><span data-stu-id="7bd8a-121"><dt>**> Zero** </dt></span></span> </dl> | <span data-ttu-id="7bd8a-122">*Zeichenfolge1* ist größer als *Zeichenfolge2*.</span><span class="sxs-lookup"><span data-stu-id="7bd8a-122">*String1* is greater than *String2*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7bd8a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bd8a-123">Requirements</span></span>



| <span data-ttu-id="7bd8a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7bd8a-124">Requirement</span></span> | <span data-ttu-id="7bd8a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7bd8a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bd8a-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7bd8a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7bd8a-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7bd8a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="7bd8a-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7bd8a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7bd8a-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7bd8a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="7bd8a-130">Zielplattform</span><span class="sxs-lookup"><span data-stu-id="7bd8a-130">Target platform</span></span><br/>          | <dl> <span data-ttu-id="7bd8a-131"><dt>[Universell](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="7bd8a-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="7bd8a-132">Header</span><span class="sxs-lookup"><span data-stu-id="7bd8a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bd8a-133"><dt>WDM. h (Include WDM. h, ntddk. h oder ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7bd8a-133"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="7bd8a-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7bd8a-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="7bd8a-135"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7bd8a-135"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7bd8a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7bd8a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bd8a-137"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bd8a-137"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="7bd8a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bd8a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bd8a-139">**Rtlcomparestring**</span><span class="sxs-lookup"><span data-stu-id="7bd8a-139">**RtlCompareString**</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlcomparestring)
</dt> <dt>

[<span data-ttu-id="7bd8a-140">**Rtlequalstring**</span><span class="sxs-lookup"><span data-stu-id="7bd8a-140">**RtlEqualString**</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlequalstring)
</dt> </dl>

 

 
