---
description: Die getframesrcaddressoffset-Funktion gibt den Offset der Quelladresse der Frames zurück.
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: Getframesrcaddressoffset-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSrcAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f7310c0ac2c6f402c37537100cc8060fef9eedd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217173"
---
# <a name="getframesrcaddressoffset-function"></a><span data-ttu-id="52aa5-103">Getframesrcaddressoffset-Funktion</span><span class="sxs-lookup"><span data-stu-id="52aa5-103">GetFrameSrcAddressOffset function</span></span>

<span data-ttu-id="52aa5-104">Die **getframesrcaddressoffset** -Funktion gibt den Offset der Quelladresse des Frames zurück.</span><span class="sxs-lookup"><span data-stu-id="52aa5-104">The **GetFrameSrcAddressOffset** function returns the offset of the frame's source address.</span></span>

## <a name="syntax"></a><span data-ttu-id="52aa5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="52aa5-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameSrcAddressOffset(
   HFRAME  hFrame,
   DWORD   AddressType,
   LPDWORD AddressLength
);
```



## <a name="parameters"></a><span data-ttu-id="52aa5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="52aa5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52aa5-107">*hframe*</span><span class="sxs-lookup"><span data-stu-id="52aa5-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="52aa5-108">Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="52aa5-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="52aa5-109">*Adresstyp*</span><span class="sxs-lookup"><span data-stu-id="52aa5-109">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="52aa5-110">Der Quell Adressentyp.</span><span class="sxs-lookup"><span data-stu-id="52aa5-110">Source address type.</span></span> <span data-ttu-id="52aa5-111">Der Parameterwert kann eines der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="52aa5-111">The parameter value can be one of the following:</span></span>

-   <span data-ttu-id="52aa5-112">\_Adresstyp \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="52aa5-112">ADDRESS\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="52aa5-113">Address \_ Type \_ IP</span><span class="sxs-lookup"><span data-stu-id="52aa5-113">ADDRESS\_TYPE\_IP</span></span>
-   <span data-ttu-id="52aa5-114">\_Adresstyp \_ IPX</span><span class="sxs-lookup"><span data-stu-id="52aa5-114">ADDRESS\_TYPE\_IPX</span></span>
-   <span data-ttu-id="52aa5-115">\_Adresstyp \_ TokenRing</span><span class="sxs-lookup"><span data-stu-id="52aa5-115">ADDRESS\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="52aa5-116">Adresstyp " \_ \_ f"</span><span class="sxs-lookup"><span data-stu-id="52aa5-116">ADDRESS\_TYPE\_FDDI</span></span>
-   <span data-ttu-id="52aa5-117">Address \_ Type \_ XNS</span><span class="sxs-lookup"><span data-stu-id="52aa5-117">ADDRESS\_TYPE\_XNS</span></span>
-   <span data-ttu-id="52aa5-118">Address \_ Type \_ Vines \_ IP</span><span class="sxs-lookup"><span data-stu-id="52aa5-118">ADDRESS\_TYPE\_VINES\_IP</span></span>
-   <span data-ttu-id="52aa5-119">\_Adresstyp \_ ATM</span><span class="sxs-lookup"><span data-stu-id="52aa5-119">ADDRESS\_TYPE\_ATM</span></span>

</dd> <dt>

<span data-ttu-id="52aa5-120">*Addresslength*</span><span class="sxs-lookup"><span data-stu-id="52aa5-120">*AddressLength*</span></span> 
</dt> <dd>

<span data-ttu-id="52aa5-121">Ein Zeiger auf ein **DWORD**, das bei der Rückgabe die Länge der Adresse in Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="52aa5-121">Pointer to a **DWORD**, which on return, contains the length of the address, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52aa5-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52aa5-122">Return value</span></span>

<span data-ttu-id="52aa5-123">Wenn die Funktion erfolgreich ist, ist der Rückgabewert der Offset zur Quelladresse.</span><span class="sxs-lookup"><span data-stu-id="52aa5-123">If the function is successful, the return value is the offset to the source address.</span></span>

<span data-ttu-id="52aa5-124">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert minus eins (-1).</span><span class="sxs-lookup"><span data-stu-id="52aa5-124">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="requirements"></a><span data-ttu-id="52aa5-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52aa5-125">Requirements</span></span>



| <span data-ttu-id="52aa5-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52aa5-126">Requirement</span></span> | <span data-ttu-id="52aa5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="52aa5-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="52aa5-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52aa5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="52aa5-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52aa5-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="52aa5-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52aa5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="52aa5-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52aa5-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="52aa5-132">Header</span><span class="sxs-lookup"><span data-stu-id="52aa5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="52aa5-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="52aa5-133"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="52aa5-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="52aa5-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="52aa5-135"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52aa5-135"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="52aa5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="52aa5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52aa5-137"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52aa5-137"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




