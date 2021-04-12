---
description: Vergleicht zwei Unicode-Zeichen folgen, um zu bestimmen, ob eine Zeichenfolge ein Präfix der anderen ist.
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: Rtlprefixunicodestring-Funktion (ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlPrefixUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 47382daab1bac5e71098f79a601d89255f1cf0e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483134"
---
# <a name="rtlprefixunicodestring-function"></a><span data-ttu-id="e4aeb-103">Rtlprefixunicodestring-Funktion</span><span class="sxs-lookup"><span data-stu-id="e4aeb-103">RtlPrefixUnicodeString function</span></span>

<span data-ttu-id="e4aeb-104">Vergleicht zwei Unicode-Zeichen folgen, um zu bestimmen, ob eine Zeichenfolge ein Präfix der anderen ist.</span><span class="sxs-lookup"><span data-stu-id="e4aeb-104">Compares two Unicode strings to determine whether one string is a prefix of the other.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4aeb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4aeb-105">Syntax</span></span>


```C++
BOOLEAN RtlPrefixUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a><span data-ttu-id="e4aeb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4aeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4aeb-107">*Zeichenfolge1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4aeb-107">*String1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4aeb-108">Ein Zeiger auf die erste Zeichenfolge, die möglicherweise ein Präfix der gepufferten Unicode-Zeichenfolge in *Zeichenfolge2* ist.</span><span class="sxs-lookup"><span data-stu-id="e4aeb-108">Pointer to the first string, which might be a prefix of the buffered Unicode string at *String2*.</span></span>

</dd> <dt>

<span data-ttu-id="e4aeb-109">*Zeichenfolge2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4aeb-109">*String2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4aeb-110">Zeiger auf die zweite Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e4aeb-110">Pointer to the second string.</span></span>

</dd> <dt>

<span data-ttu-id="e4aeb-111">*CaseInsensitive* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4aeb-111">*CaseInSensitive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4aeb-112">**True** gibt an, dass die Groß-/Kleinschreibung beim Vergleich ignoriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4aeb-112">If **TRUE**, case should be ignored when doing the comparison.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4aeb-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4aeb-113">Return value</span></span>

<span data-ttu-id="e4aeb-114">**True** , wenn *Zeichenfolge1* ein Präfix von *Zeichenfolge2* ist.</span><span class="sxs-lookup"><span data-stu-id="e4aeb-114">**TRUE** if *String1* is a prefix of *String2*.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4aeb-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4aeb-115">Requirements</span></span>



| <span data-ttu-id="e4aeb-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4aeb-116">Requirement</span></span> | <span data-ttu-id="e4aeb-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e4aeb-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4aeb-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4aeb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e4aeb-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4aeb-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="e4aeb-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4aeb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e4aeb-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4aeb-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="e4aeb-122">Zielplattform</span><span class="sxs-lookup"><span data-stu-id="e4aeb-122">Target platform</span></span><br/>          | <dl> <span data-ttu-id="e4aeb-123"><dt>[Universell](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="e4aeb-123"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="e4aeb-124">Header</span><span class="sxs-lookup"><span data-stu-id="e4aeb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4aeb-125"><dt>Ntddk. h (einschließlich ntddk. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4aeb-125"><dt>Ntddk.h (include Ntddk.h)</dt></span></span> </dl>                                    |
| <span data-ttu-id="e4aeb-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e4aeb-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="e4aeb-127"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4aeb-127"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e4aeb-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e4aeb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4aeb-129"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4aeb-129"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="e4aeb-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4aeb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4aeb-131">**Rtlcompareunicodestring**</span><span class="sxs-lookup"><span data-stu-id="e4aeb-131">**RtlCompareUnicodeString**</span></span>](rtlcompareunicodestring.md)
</dt> </dl>

 

 




