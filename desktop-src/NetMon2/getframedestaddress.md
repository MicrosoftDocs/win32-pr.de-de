---
description: Ruft die Zieladresse eines Frames ab.
ms.assetid: f19a6753-37d8-4ec7-a7d4-ced0292d453c
title: Getframedebug-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: afec32f0e0fc66ccd5a1d78cc9769b0e742f1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958721"
---
# <a name="getframedestaddress-function"></a><span data-ttu-id="9caa4-103">Getframedebug-Funktion</span><span class="sxs-lookup"><span data-stu-id="9caa4-103">GetFrameDestAddress function</span></span>

<span data-ttu-id="9caa4-104">Die **getframedebug** -Funktion Ruft die Zieladresse eines Frames ab.</span><span class="sxs-lookup"><span data-stu-id="9caa4-104">The **GetFrameDestAddress** function retrieves the destination address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="9caa4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9caa4-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameDestAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="9caa4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9caa4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9caa4-107">*hframe*</span><span class="sxs-lookup"><span data-stu-id="9caa4-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="9caa4-108">Ein Handle des Frames, auf den ein Zeiger angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9caa4-108">A handle of the frame to get a pointer to.</span></span>

</dd> <dt>

<span data-ttu-id="9caa4-109">*lpAddress*</span><span class="sxs-lookup"><span data-stu-id="9caa4-109">*lpAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="9caa4-110">Ein Rückgabe Puffer, in dem die Frame Zieladresse gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="9caa4-110">A return buffer that stores the frame destination address.</span></span>

</dd> <dt>

<span data-ttu-id="9caa4-111">*Adresstyp*</span><span class="sxs-lookup"><span data-stu-id="9caa4-111">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="9caa4-112">Eine Art Adresse, z \_ . b. adrestyp \_ Ethernet oder \_ Adresstyp \_ -IP.</span><span class="sxs-lookup"><span data-stu-id="9caa4-112">A type of address, such as ADDRESS\_TYPE\_ETHERNET or ADDRESS\_TYPE\_IP.</span></span>

</dd> <dt>

<span data-ttu-id="9caa4-113">*Flags*</span><span class="sxs-lookup"><span data-stu-id="9caa4-113">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="9caa4-114">Die Flags, die zum Ändern der zurückgegebenen Ziel Adressdaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9caa4-114">The flags used to modify returned destination address data.</span></span>



| <span data-ttu-id="9caa4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9caa4-115">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="9caa4-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9caa4-116">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <span data-ttu-id="9caa4-117"><dt>**adressstype- \_ Flags \_ normalisieren**</dt></span><span class="sxs-lookup"><span data-stu-id="9caa4-117"><dt>**ADDRESSTYPE\_FLAGS\_NORMALIZE**</dt></span></span> </dl>        | <span data-ttu-id="9caa4-118">Bricht die Routing-und Gruppen Bits ab.</span><span class="sxs-lookup"><span data-stu-id="9caa4-118">Cancels the routing and group BITs.</span></span><br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <span data-ttu-id="9caa4-119"><dt>**adressstype- \_ Flags \_ Bit \_ umkehren**</dt></span><span class="sxs-lookup"><span data-stu-id="9caa4-119"><dt>**ADDRESSTYPE\_FLAGS\_BIT\_REVERSE**</dt></span></span> </dl> | <span data-ttu-id="9caa4-120">Konvertiert die Netzwerkadressen des tokenrings wieder in den normalen Zustand.</span><span class="sxs-lookup"><span data-stu-id="9caa4-120">Converts token ring network addresses back to normal.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9caa4-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9caa4-121">Return value</span></span>

<span data-ttu-id="9caa4-122">Wenn die Funktion erfolgreich ist, ist der *lpAddress* -Wert gültig, und der Rückgabewert ist bHerrn \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9caa4-122">If the function is successful, the *lpAddress* value is valid, and the return value is BHERR\_SUCCESS.</span></span>

<span data-ttu-id="9caa4-123">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9caa4-123">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="9caa4-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9caa4-124">Return code</span></span>                                                                                                | <span data-ttu-id="9caa4-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9caa4-125">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9caa4-126"><dt>**bHerr- \_ Protokoll \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="9caa4-126"><dt>**BHERR\_PROTOCOL\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="9caa4-127">Das angegebene Protokoll im *Adresstype* -Parameter ist für den Frame ungültig.</span><span class="sxs-lookup"><span data-stu-id="9caa4-127">The specified protocol in the *AddressType* parameter is invalid for the frame.</span></span><br/> |
| <dl> <span data-ttu-id="9caa4-128"><dt>**bWer hat einen \_ ungültigen \_ hframe**</dt></span><span class="sxs-lookup"><span data-stu-id="9caa4-128"><dt>**BHERR\_INVALID\_HFRAME**</dt></span></span> </dl>      | <span data-ttu-id="9caa4-129">Der *hframe* -Wert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9caa4-129">The *hFrame* value is invalid.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="9caa4-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9caa4-130">Remarks</span></span>

<span data-ttu-id="9caa4-131">Der **\_ adrestyp " \_ Suche nach \_ höchster** Adresse" ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="9caa4-131">The **ADDRESS\_TYPE\_FIND\_HIGHEST** address type is allowed.</span></span> <span data-ttu-id="9caa4-132">Wenn dieser Adresstyp verwendet wird, sucht die-Funktion nach der IP-Adresse von IPX, xns, IP oder Vines, bevor die Ethernet-, TokenRing-oder die f-di-Adresse zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9caa4-132">When this address type is used, the function searches for the IPX, XNS, IP, or VINES IP address before returning the ETHERNET, TOKENRING, or FDDI address.</span></span> <span data-ttu-id="9caa4-133">Diese Vorgehensweise ist nützlich für Protokolle und in Umgebungen, in denen zwei NICs unter einer einzelnen Server Adresse multiplext werden können.</span><span class="sxs-lookup"><span data-stu-id="9caa4-133">This approach is useful for protocols and in environments where two NICs can be multiplexed under a single server address.</span></span>

## <a name="requirements"></a><span data-ttu-id="9caa4-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9caa4-134">Requirements</span></span>



| <span data-ttu-id="9caa4-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9caa4-135">Requirement</span></span> | <span data-ttu-id="9caa4-136">Wert</span><span class="sxs-lookup"><span data-stu-id="9caa4-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9caa4-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9caa4-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9caa4-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9caa4-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9caa4-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9caa4-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9caa4-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9caa4-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9caa4-141">Header</span><span class="sxs-lookup"><span data-stu-id="9caa4-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="9caa4-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9caa4-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="9caa4-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9caa4-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="9caa4-144"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9caa4-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9caa4-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9caa4-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9caa4-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9caa4-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




