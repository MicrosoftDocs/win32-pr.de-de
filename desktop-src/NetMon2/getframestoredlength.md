---
description: Die getframestoredlength-Funktion gibt die Länge des Frames zurück.
ms.assetid: 7ac0e528-a45a-4c36-a99d-647347bdd143
title: Getframestoredlength-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameStoredLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e48f1d357645a9f50a85da4aba79d72baba4e4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356925"
---
# <a name="getframestoredlength-function"></a><span data-ttu-id="f3ed8-103">Getframestoredlength-Funktion</span><span class="sxs-lookup"><span data-stu-id="f3ed8-103">GetFrameStoredLength function</span></span>

<span data-ttu-id="f3ed8-104">Die **getframestoredlength** -Funktion gibt die Länge des Frames zurück.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-104">The **GetFrameStoredLength** function returns the length of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3ed8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3ed8-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameStoredLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="f3ed8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3ed8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3ed8-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3ed8-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3ed8-108">Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3ed8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3ed8-109">Return value</span></span>

<span data-ttu-id="f3ed8-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Länge des Frames als gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-110">If the function is successful, the return value is the length of the frame as stored.</span></span>

<span data-ttu-id="f3ed8-111">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f3ed8-111">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3ed8-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3ed8-112">Remarks</span></span>

<span data-ttu-id="f3ed8-113">[*Experten*](e.md) und [*Parser*](p.md) können die **getframestoredlength** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameStoredLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3ed8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3ed8-114">Requirements</span></span>



| <span data-ttu-id="f3ed8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3ed8-115">Requirement</span></span> | <span data-ttu-id="f3ed8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f3ed8-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f3ed8-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f3ed8-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3ed8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f3ed8-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f3ed8-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3ed8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f3ed8-121">Header</span><span class="sxs-lookup"><span data-stu-id="f3ed8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3ed8-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3ed8-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f3ed8-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f3ed8-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="f3ed8-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3ed8-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f3ed8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f3ed8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3ed8-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3ed8-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3ed8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3ed8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3ed8-128">GetFrameLength</span><span class="sxs-lookup"><span data-stu-id="f3ed8-128">GetFrameLength</span></span>](getframelength.md)
</dt> </dl>

 

 




