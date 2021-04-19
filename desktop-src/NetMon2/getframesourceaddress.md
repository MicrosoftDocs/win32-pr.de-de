---
description: Ruft die Quelladresse eines Frames ab.
ms.assetid: 414f9e64-f1b2-46f1-822e-0fffacfad843
title: Getframesourceaddress-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6939e5875c4d2f6f41ae33574c7a7240697042ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343253"
---
# <a name="getframesourceaddress-function"></a><span data-ttu-id="02938-103">Getframesourceaddress-Funktion</span><span class="sxs-lookup"><span data-stu-id="02938-103">GetFrameSourceAddress function</span></span>

<span data-ttu-id="02938-104">Die **getframesourceaddress** -Funktion Ruft die Quelladresse eines Frames ab.</span><span class="sxs-lookup"><span data-stu-id="02938-104">The **GetFrameSourceAddress** function retrieves the source address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="02938-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02938-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameSourceAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="02938-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="02938-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02938-107">*hframe*</span><span class="sxs-lookup"><span data-stu-id="02938-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="02938-108">Ein Handle für den Frame, auf den ein Zeiger zu erhalten ist.</span><span class="sxs-lookup"><span data-stu-id="02938-108">A handle to the frame for which to get a pointer to.</span></span>

</dd> <dt>

<span data-ttu-id="02938-109">*lpAddress*</span><span class="sxs-lookup"><span data-stu-id="02938-109">*lpAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="02938-110">Ein Rückgabe Puffer, in dem die Frame Quelladresse gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="02938-110">A return buffer that stores the frame source address.</span></span>

</dd> <dt>

<span data-ttu-id="02938-111">*Adresstyp*</span><span class="sxs-lookup"><span data-stu-id="02938-111">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="02938-112">Der Typ der Adresse, nach der gesucht wird, \_ z \_ . b. adrestyp Ethernet oder \_ Adresstyp \_ -IP.</span><span class="sxs-lookup"><span data-stu-id="02938-112">The type of address searched for, such as ADDRESS\_TYPE\_ETHERNET or ADDRESS\_TYPE\_IP.</span></span>

</dd> <dt>

<span data-ttu-id="02938-113">*Flags*</span><span class="sxs-lookup"><span data-stu-id="02938-113">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="02938-114">Die Flags, die zum Ändern der zurückgegebenen Quell Adressdaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="02938-114">The flags used to modify returned source address data.</span></span>



| <span data-ttu-id="02938-115">Wert</span><span class="sxs-lookup"><span data-stu-id="02938-115">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="02938-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="02938-116">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <span data-ttu-id="02938-117"><dt>**adressstype- \_ Flags \_ normalisieren**</dt></span><span class="sxs-lookup"><span data-stu-id="02938-117"><dt>**ADDRESSTYPE\_FLAGS\_NORMALIZE**</dt></span></span> </dl>        | <span data-ttu-id="02938-118">Bricht die Routing-und Gruppen Bits ab.</span><span class="sxs-lookup"><span data-stu-id="02938-118">Cancels the routing and group BITs.</span></span><br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <span data-ttu-id="02938-119"><dt>**adressstype- \_ Flags \_ Bit \_ umkehren**</dt></span><span class="sxs-lookup"><span data-stu-id="02938-119"><dt>**ADDRESSTYPE\_FLAGS\_BIT\_REVERSE**</dt></span></span> </dl> | <span data-ttu-id="02938-120">Konvertiert die Netzwerkadressen des tokenrings wieder in den normalen Zustand.</span><span class="sxs-lookup"><span data-stu-id="02938-120">Converts token ring network addresses back to normal.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02938-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02938-121">Return value</span></span>

<span data-ttu-id="02938-122">Wenn die Funktion erfolgreich ist, ist der *lpAddress* -Wert gültig, und der Rückgabewert ist bHerrn \_ Success.</span><span class="sxs-lookup"><span data-stu-id="02938-122">If the function is successful, the *lpAddress* value is valid, and the return value is BHERR\_SUCCESS.</span></span>

<span data-ttu-id="02938-123">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="02938-123">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="02938-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="02938-124">Return code</span></span>                                                                                                | <span data-ttu-id="02938-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02938-125">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="02938-126"><dt>**bHerr- \_ Protokoll \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="02938-126"><dt>**BHERR\_PROTOCOL\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="02938-127">Das vom *adressstype* -Parameter angegebene Protokoll ist für den Frame ungültig.</span><span class="sxs-lookup"><span data-stu-id="02938-127">The protocol specified by the *AddressType* parameter is invalid for the frame.</span></span><br/> |
| <dl> <span data-ttu-id="02938-128"><dt>**bWer hat einen \_ ungültigen \_ hframe**</dt></span><span class="sxs-lookup"><span data-stu-id="02938-128"><dt>**BHERR\_INVALID\_HFRAME**</dt></span></span> </dl>      | <span data-ttu-id="02938-129">Der Wert des *hframe* -Parameters ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="02938-129">The *hFrame* parameter value is invalid.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="02938-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02938-130">Remarks</span></span>

<span data-ttu-id="02938-131">Es ist ein Adresstyp vom Typ " **Address \_ Type \_ Find \_ Best** " zulässig.</span><span class="sxs-lookup"><span data-stu-id="02938-131">An address type of **ADDRESS\_TYPE\_FIND\_HIGHEST** is allowed.</span></span> <span data-ttu-id="02938-132">Wenn dieser Adresstyp verwendet wird, sucht die-Funktion nach der IP-Adresse von IPX, xns, IP oder Vines, bevor die Ethernet-, TokenRing-oder die f-di-Adresse zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="02938-132">When this address type is used, the function searches for the IPX, XNS, IP, or VINES IP address before returning the ETHERNET, TOKENRING, or FDDI address.</span></span> <span data-ttu-id="02938-133">Diese Vorgehensweise ist nützlich für Protokolle und Umgebungen, in denen zwei NICs unter einer einzelnen Server Adresse multiplext werden können.</span><span class="sxs-lookup"><span data-stu-id="02938-133">This approach is useful for protocols and environments in which two NICs can be multiplexed under a single server address.</span></span>

## <a name="requirements"></a><span data-ttu-id="02938-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02938-134">Requirements</span></span>



| <span data-ttu-id="02938-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02938-135">Requirement</span></span> | <span data-ttu-id="02938-136">Wert</span><span class="sxs-lookup"><span data-stu-id="02938-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="02938-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02938-137">Minimum supported client</span></span><br/> | <span data-ttu-id="02938-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02938-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="02938-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02938-139">Minimum supported server</span></span><br/> | <span data-ttu-id="02938-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02938-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="02938-141">Header</span><span class="sxs-lookup"><span data-stu-id="02938-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="02938-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="02938-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="02938-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="02938-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="02938-144"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02938-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="02938-145">DLL</span><span class="sxs-lookup"><span data-stu-id="02938-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02938-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02938-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




