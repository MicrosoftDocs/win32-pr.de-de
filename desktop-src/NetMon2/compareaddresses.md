---
description: Die compareaddress-Funktion vergleicht zwei Adressen, die angeben, dass eine der Adressen größer als, kleiner oder gleich der anderen Adresse ist.
ms.assetid: 76ff37d2-714f-4bac-adcc-eab78c8f25d3
title: Compareadressen-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: fd72ef0281615c0b56176e86ee9bb3659b498a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348106"
---
# <a name="compareaddresses-function"></a><span data-ttu-id="c1c6d-103">Compareadressen-Funktion</span><span class="sxs-lookup"><span data-stu-id="c1c6d-103">CompareAddresses function</span></span>

<span data-ttu-id="c1c6d-104">Die **compareaddress** -Funktion vergleicht zwei Adressen, die angeben, dass eine der Adressen größer als, kleiner oder gleich der anderen Adresse ist.</span><span class="sxs-lookup"><span data-stu-id="c1c6d-104">The **CompareAddresses** function compares two addresses, indicating that one of the addresses is greater than, less than, or equal to the other address.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c6d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1c6d-105">Syntax</span></span>


```C++
int WINAPI CompareAddresses(
  _In_ LPADDRESS lpAddress1,
  _In_ LPADDRESS lpAddress2
);
```



## <a name="parameters"></a><span data-ttu-id="c1c6d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1c6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1c6d-107">*lpAddress1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1c6d-107">*lpAddress1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c6d-108">Zeiger auf die erste Adresse.</span><span class="sxs-lookup"><span data-stu-id="c1c6d-108">Pointer to the first address.</span></span>

</dd> <dt>

<span data-ttu-id="c1c6d-109">*lpAddress2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1c6d-109">*lpAddress2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c6d-110">Zeiger auf die zweite Adresse.</span><span class="sxs-lookup"><span data-stu-id="c1c6d-110">Pointer to the second address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1c6d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1c6d-111">Return value</span></span>

<span data-ttu-id="c1c6d-112">Wenn die Adressen identisch sind, gibt die Funktion 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c1c6d-112">If the addresses are the same, the function returns zero.</span></span>

<span data-ttu-id="c1c6d-113">Wenn der *lpAddress1* -Parameter eine Adresse angibt, die kleiner als die Adresse ist, die der *lpAddress2* -Parameter angibt, ist der Rückgabewert eine negative Zahl.</span><span class="sxs-lookup"><span data-stu-id="c1c6d-113">If the *lpAddress1* parameter specifies an address that is less than the address that the *lpAddress2* parameter specifies, the return value is a negative number.</span></span>

<span data-ttu-id="c1c6d-114">Wenn der *lpAddress1* -Parameter eine Adresse angibt, die größer als die Adresse ist, die der *lpAddress2* -Parameter angibt, ist der Rückgabewert eine positive Zahl.</span><span class="sxs-lookup"><span data-stu-id="c1c6d-114">If the *lpAddress1* parameter specifies an address that is greater than the address that the *lpAddress2* parameter specifies, the return value is a positive number.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1c6d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1c6d-115">Remarks</span></span>

<span data-ttu-id="c1c6d-116">Eine Adresse, die kleiner als eine andere Adresse ist, weist auf einen vorherigen Frame hin.</span><span class="sxs-lookup"><span data-stu-id="c1c6d-116">An address that is less than another address indicates a previous frame.</span></span> <span data-ttu-id="c1c6d-117">Eine Adresse, die größer als eine andere Adresse ist, weist auf einen späteren Frame hin.</span><span class="sxs-lookup"><span data-stu-id="c1c6d-117">An address that is greater than another address indicates a later frame.</span></span>

<span data-ttu-id="c1c6d-118">Netzwerkmonitor bietet zwei weitere Funktionen, [compareframedestaddress](compareframedestaddress.md) und [compareframesourceaddress](compareframesourceaddress.md), die Sie zum Vergleichen von Adressen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c1c6d-118">Network Monitor provides two other functions, [CompareFrameDestAddress](compareframedestaddress.md) and [CompareFrameSourceAddress](compareframesourceaddress.md), which you can use to compare addresses.</span></span> <span data-ttu-id="c1c6d-119">Die **compareframedebug** -Funktion vergleicht eine angegebene Adresse mit der Zieladresse des Frames, und die **compareframesourceaddress** -Funktion vergleicht eine angegebene Adresse mit der Quelladresse des Frames.</span><span class="sxs-lookup"><span data-stu-id="c1c6d-119">The **CompareFrameDestAddress** function compares a given address to the frame's destination address, and the **CompareFrameSourceAddress** function compares a given address to the frame's source address.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1c6d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1c6d-120">Requirements</span></span>



| <span data-ttu-id="c1c6d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1c6d-121">Requirement</span></span> | <span data-ttu-id="c1c6d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c1c6d-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c6d-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1c6d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c1c6d-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1c6d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c1c6d-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1c6d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c1c6d-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1c6d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c1c6d-127">Header</span><span class="sxs-lookup"><span data-stu-id="c1c6d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1c6d-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1c6d-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="c1c6d-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c1c6d-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="c1c6d-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1c6d-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c1c6d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c1c6d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1c6d-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1c6d-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1c6d-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1c6d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c6d-134">Compareframedebug</span><span class="sxs-lookup"><span data-stu-id="c1c6d-134">CompareFrameDestAddress</span></span>](compareframedestaddress.md)
</dt> <dt>

[<span data-ttu-id="c1c6d-135">Compareframesourceaddress</span><span class="sxs-lookup"><span data-stu-id="c1c6d-135">CompareFrameSourceAddress</span></span>](compareframesourceaddress.md)
</dt> </dl>

 

 




