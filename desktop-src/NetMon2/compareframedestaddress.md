---
description: Die compareframedebug-Funktion vergleicht eine Adresse mit der Zieladresse eines Frames.
ms.assetid: 739b3b9f-f989-459d-ac3e-6be7769adc06
title: Compareframedebug-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: a9ce0ff776588c06b8fddc34240e9c2170ceca69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864796"
---
# <a name="compareframedestaddress-function"></a><span data-ttu-id="6e5a3-103">Compareframedebug-Funktion</span><span class="sxs-lookup"><span data-stu-id="6e5a3-103">CompareFrameDestAddress function</span></span>

<span data-ttu-id="6e5a3-104">Die **compareframedebug** -Funktion vergleicht eine Adresse mit der Zieladresse eines Frames.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-104">The **CompareFrameDestAddress** function compares an address to the destination address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e5a3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e5a3-105">Syntax</span></span>


```C++
BOOL WINAPI CompareFrameDestAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="6e5a3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e5a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e5a3-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e5a3-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e5a3-108">Handle für einen Frame.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="6e5a3-109">*lpAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e5a3-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e5a3-110">Zeiger auf eine Adresse.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-110">Pointer to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e5a3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e5a3-111">Return value</span></span>

<span data-ttu-id="6e5a3-112">Wenn die Adressen identisch sind, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="6e5a3-112">If the addresses are the same, the return value is **TRUE**.</span></span>

<span data-ttu-id="6e5a3-113">Wenn die Adressen nicht identisch sind, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-113">If the addresses are not the same, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e5a3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e5a3-114">Remarks</span></span>

<span data-ttu-id="6e5a3-115">Damit die **compareframedestaddress** -Funktion erfolgreich zurückgegeben wird, muss der Ziel Adresstyp mit dem im *lpAddress* -Parameter angegebenen Adresstyp identisch sein.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-115">For the **CompareFrameDestAddress** function to return successfully, the destination address type must match the type of address specified in the *lpAddress* parameter.</span></span>

<span data-ttu-id="6e5a3-116">Netzwerkmonitor bietet zwei weitere Funktionen, [compareframesourceaddress](compareframesourceaddress.md) und [compareaddress](compareaddresses.md), die Sie zum Vergleichen von Adressen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-116">Network Monitor provides two other functions, [CompareFrameSourceAddress](compareframesourceaddress.md) and [CompareAddresses](compareaddresses.md), which you can use to compare addresses.</span></span> <span data-ttu-id="6e5a3-117">Die **compareframesourceaddress** -Funktion vergleicht eine angegebene Adresse mit der Quelladresse des Frames, und die **compareaddress** -Funktion vergleicht zwei angegebene Adressen.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-117">The **CompareFrameSourceAddress** function compares a given address to the frame's source address, and the **CompareAddress** function compares two given addresses.</span></span>

<span data-ttu-id="6e5a3-118">[*Experten*](e.md) und [*Parser*](p.md) können die **compareframedebug** -Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **CompareFrameDestAddress** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e5a3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e5a3-119">Requirements</span></span>



| <span data-ttu-id="6e5a3-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e5a3-120">Requirement</span></span> | <span data-ttu-id="6e5a3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6e5a3-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6e5a3-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e5a3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6e5a3-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e5a3-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6e5a3-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e5a3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6e5a3-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e5a3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6e5a3-126">Header</span><span class="sxs-lookup"><span data-stu-id="6e5a3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e5a3-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a3-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="6e5a3-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6e5a3-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e5a3-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a3-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="6e5a3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6e5a3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e5a3-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a3-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e5a3-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e5a3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e5a3-133">Compareadressen</span><span class="sxs-lookup"><span data-stu-id="6e5a3-133">CompareAddresses</span></span>](compareaddresses.md)
</dt> <dt>

[<span data-ttu-id="6e5a3-134">Compareframesourceaddress</span><span class="sxs-lookup"><span data-stu-id="6e5a3-134">CompareFrameSourceAddress</span></span>](compareframesourceaddress.md)
</dt> </dl>

 

 




