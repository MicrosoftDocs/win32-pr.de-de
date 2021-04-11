---
description: Die compareframesourceaddress-Funktion vergleicht eine Adresse mit der Quelladresse eines Frames.
ms.assetid: 7221c0cc-d6c1-4ec9-bf11-3ba1fefb35da
title: Compareframesourceaddress-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a100273c37e25a7b1deba86ed2704886dbfccc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217339"
---
# <a name="compareframesourceaddress-function"></a><span data-ttu-id="61026-103">Compareframesourceaddress-Funktion</span><span class="sxs-lookup"><span data-stu-id="61026-103">CompareFrameSourceAddress function</span></span>

<span data-ttu-id="61026-104">Die **compareframesourceaddress** -Funktion vergleicht eine Adresse mit der Quelladresse eines Frames.</span><span class="sxs-lookup"><span data-stu-id="61026-104">The **CompareFrameSourceAddress** function compares an address to the source address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="61026-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="61026-105">Syntax</span></span>


```C++
BOOL WINAPI CompareFrameSourceAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="61026-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="61026-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61026-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61026-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61026-108">Handle für einen Frame.</span><span class="sxs-lookup"><span data-stu-id="61026-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="61026-109">*lpAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61026-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61026-110">Zeiger auf eine Adresse.</span><span class="sxs-lookup"><span data-stu-id="61026-110">Pointer to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61026-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61026-111">Return value</span></span>

<span data-ttu-id="61026-112">Wenn die Adressen identisch sind, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="61026-112">If the addresses are the same, the return value is **TRUE**.</span></span>

<span data-ttu-id="61026-113">Wenn die Adressen nicht identisch sind, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="61026-113">If the addresses are not the same, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="61026-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61026-114">Remarks</span></span>

<span data-ttu-id="61026-115">Damit die **compareframesourceaddress** -Funktion erfolgreich ausgeführt werden kann, muss der Quell Adresstyp mit dem Adresstyp übereinstimmen, der im *lpAddress* -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="61026-115">For the **CompareFrameSourceAddress** function to succeed, the source address type must match the type of address specified in the *lpAddress* parameter.</span></span>

<span data-ttu-id="61026-116">Netzwerkmonitor bietet zwei weitere Funktionen zum Vergleichen von Adressen: [compareframedestaddress](compareframedestaddress.md) und [compareadressen](compareaddresses.md).</span><span class="sxs-lookup"><span data-stu-id="61026-116">Network Monitor provides two other functions for comparing addresses: [CompareFrameDestAddress](compareframedestaddress.md) and [CompareAddresses](compareaddresses.md).</span></span> <span data-ttu-id="61026-117">Die **compareframerestaddress** -Funktion vergleicht eine angegebene Adresse mit der Zieladresse des Frames, und die **compareaddress** -Funktion vergleicht zwei angegebene Adressen.</span><span class="sxs-lookup"><span data-stu-id="61026-117">The **CompareFrameDestAddress** function compares a given address to the frame's destination address, and the **CompareAddress** function compares two given addresses.</span></span>

<span data-ttu-id="61026-118">[*Experten*](e.md) und [*Parser*](p.md) können die **compareframesourceaddress** -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="61026-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **CompareFrameSourceAddress** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="61026-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61026-119">Requirements</span></span>



| <span data-ttu-id="61026-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61026-120">Requirement</span></span> | <span data-ttu-id="61026-121">Wert</span><span class="sxs-lookup"><span data-stu-id="61026-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="61026-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61026-122">Minimum supported client</span></span><br/> | <span data-ttu-id="61026-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61026-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="61026-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61026-124">Minimum supported server</span></span><br/> | <span data-ttu-id="61026-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61026-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="61026-126">Header</span><span class="sxs-lookup"><span data-stu-id="61026-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="61026-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="61026-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="61026-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="61026-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="61026-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61026-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="61026-130">DLL</span><span class="sxs-lookup"><span data-stu-id="61026-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61026-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61026-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61026-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61026-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61026-133">Compareadressen</span><span class="sxs-lookup"><span data-stu-id="61026-133">CompareAddresses</span></span>](compareaddresses.md)
</dt> <dt>

[<span data-ttu-id="61026-134">Compareframedebug</span><span class="sxs-lookup"><span data-stu-id="61026-134">CompareFrameDestAddress</span></span>](compareframedestaddress.md)
</dt> </dl>

 

 




