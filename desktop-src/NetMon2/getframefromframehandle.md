---
description: Die getframefromframehandle-Funktion gibt einen Zeiger auf einen Frame aus einem Frame Handle zurück.
ms.assetid: 790fe5fe-a857-4947-a471-d0538c0f0d61
title: Getframefromframehandle-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameFromFrameHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ce8151b2f4c81c61dea5969ff52e9ddf2d6615a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344403"
---
# <a name="getframefromframehandle-function"></a><span data-ttu-id="e95c5-103">Getframefromframehandle-Funktion</span><span class="sxs-lookup"><span data-stu-id="e95c5-103">GetFrameFromFrameHandle function</span></span>

<span data-ttu-id="e95c5-104">Die **getframefromframehandle** -Funktion gibt einen Zeiger auf einen Frame aus einem Frame Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="e95c5-104">The **GetFrameFromFrameHandle** function returns a pointer to a frame from a frame handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="e95c5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e95c5-105">Syntax</span></span>


```C++
ULPFRAME WINAPI GetFrameFromFrameHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="e95c5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e95c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e95c5-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e95c5-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e95c5-108">Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="e95c5-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e95c5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e95c5-109">Return value</span></span>

<span data-ttu-id="e95c5-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den Frame.</span><span class="sxs-lookup"><span data-stu-id="e95c5-110">If the function is successful, the return value is a pointer to the frame.</span></span>

<span data-ttu-id="e95c5-111">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0.</span><span class="sxs-lookup"><span data-stu-id="e95c5-111">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="e95c5-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e95c5-112">Remarks</span></span>

<span data-ttu-id="e95c5-113">Die **getframefromframehandle** -Funktion Ruft Daten ab, die von den anderen von Netzwerkmonitor bereitgestellten Hilfsfunktionen nicht abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="e95c5-113">The **GetFrameFromFrameHandle** function retrieves data that cannot be retrieved by the other helper functions that Network Monitor provides.</span></span> <span data-ttu-id="e95c5-114">Verwenden Sie nach Möglichkeit die folgenden Funktionen.</span><span class="sxs-lookup"><span data-stu-id="e95c5-114">Use the following functions whenever possible.</span></span>

<dl>

[<span data-ttu-id="e95c5-115">**Getframedstaddressoffset**</span><span class="sxs-lookup"><span data-stu-id="e95c5-115">**GetFrameDstAddressOffset**</span></span>](getframedstaddressoffset.md)  
[<span data-ttu-id="e95c5-116">**Getframesrcaddressoffset**</span><span class="sxs-lookup"><span data-stu-id="e95c5-116">**GetFrameSrcAddressOffset**</span></span>](getframesrcaddressoffset.md)  
[<span data-ttu-id="e95c5-117">**Getframecapturehandle**</span><span class="sxs-lookup"><span data-stu-id="e95c5-117">**GetFrameCaptureHandle**</span></span>](getframecapturehandle.md)  
[<span data-ttu-id="e95c5-118">**Getframeumstaddress**</span><span class="sxs-lookup"><span data-stu-id="e95c5-118">**GetFrameDestAddress**</span></span>](getframedestaddress.md)  
[<span data-ttu-id="e95c5-119">**Getframesourceaddress**</span><span class="sxs-lookup"><span data-stu-id="e95c5-119">**GetFrameSourceAddress**</span></span>](getframesourceaddress.md)  
[<span data-ttu-id="e95c5-120">**Getframemacheaderlength**</span><span class="sxs-lookup"><span data-stu-id="e95c5-120">**GetFrameMacHeaderLength**</span></span>](getframemacheaderlength.md)  
[<span data-ttu-id="e95c5-121">**GetFrameLength**</span><span class="sxs-lookup"><span data-stu-id="e95c5-121">**GetFrameLength**</span></span>](getframelength.md)  
[<span data-ttu-id="e95c5-122">**Getframestoredlength**</span><span class="sxs-lookup"><span data-stu-id="e95c5-122">**GetFrameStoredLength**</span></span>](getframestoredlength.md)  
[<span data-ttu-id="e95c5-123">**Getframemactype**</span><span class="sxs-lookup"><span data-stu-id="e95c5-123">**GetFrameMacType**</span></span>](getframemactype.md)  
[<span data-ttu-id="e95c5-124">**Getframennummer**</span><span class="sxs-lookup"><span data-stu-id="e95c5-124">**GetFrameNumber**</span></span>](getframenumber.md)  
[<span data-ttu-id="e95c5-125">**Getframetimestamp**</span><span class="sxs-lookup"><span data-stu-id="e95c5-125">**GetFrameTimeStamp**</span></span>](getframetimestamp.md)  
</dl>

<span data-ttu-id="e95c5-126">[*Experten*](e.md) und [*Parser*](p.md) können die **getframefromframehandle** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e95c5-126">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameFromFrameHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e95c5-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e95c5-127">Requirements</span></span>



| <span data-ttu-id="e95c5-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e95c5-128">Requirement</span></span> | <span data-ttu-id="e95c5-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e95c5-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e95c5-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e95c5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e95c5-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e95c5-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e95c5-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e95c5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e95c5-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e95c5-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e95c5-134">Header</span><span class="sxs-lookup"><span data-stu-id="e95c5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e95c5-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e95c5-135"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e95c5-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e95c5-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="e95c5-137"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e95c5-137"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e95c5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e95c5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e95c5-139"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e95c5-139"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




