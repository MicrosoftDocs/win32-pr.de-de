---
description: "\"GetCount\" wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop."
ms.assetid: 1fe39f2d-f95e-4436-a780-40fe8bd41b74
title: 'Ienumumuseridentity:: GetCount-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.GetCount
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 43355a9585fc4099c8649f7df506ff3495a53944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345388"
---
# <a name="ienumuseridentitygetcount-method"></a><span data-ttu-id="4f8ba-104">Ienumumuseridentity:: GetCount-Methode</span><span class="sxs-lookup"><span data-stu-id="4f8ba-104">IEnumUserIdentity::GetCount method</span></span>

<span data-ttu-id="4f8ba-105">\[" **GetCount** " wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="4f8ba-105">\[**GetCount** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="4f8ba-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="4f8ba-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="4f8ba-107">Ruft die Anzahl der Benutzer Identitäten ab, die sich zurzeit im System befinden.</span><span class="sxs-lookup"><span data-stu-id="4f8ba-107">Gets the count of user identities currently on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f8ba-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f8ba-108">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pnCount
);
```



## <a name="parameters"></a><span data-ttu-id="4f8ba-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f8ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f8ba-110">*pnCount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4f8ba-110">*pnCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f8ba-111">Typ: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="4f8ba-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="4f8ba-112">Zeiger auf ein _ \*ulong\*\*-Wert, der die Anzahl empfängt.</span><span class="sxs-lookup"><span data-stu-id="4f8ba-112">Pointer to a _ *ULONG*\* that receives the count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f8ba-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f8ba-113">Return value</span></span>

<span data-ttu-id="4f8ba-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4f8ba-114">Type: **HRESULT**</span></span>

<span data-ttu-id="4f8ba-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="4f8ba-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4f8ba-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f8ba-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f8ba-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f8ba-117">Remarks</span></span>

<span data-ttu-id="4f8ba-118">Wenn die Unterstützung für mehrere Benutzer Identitäten deaktiviert ist, erhält *pnCount* den Wert 1.</span><span class="sxs-lookup"><span data-stu-id="4f8ba-118">If support for multiple user identities is disabled, *pnCount* will receive a value of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f8ba-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4f8ba-119">Requirements</span></span>



| <span data-ttu-id="4f8ba-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f8ba-120">Requirement</span></span> | <span data-ttu-id="4f8ba-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4f8ba-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f8ba-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f8ba-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4f8ba-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f8ba-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4f8ba-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f8ba-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4f8ba-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f8ba-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4f8ba-126">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4f8ba-126">End of client support</span></span><br/>    | <span data-ttu-id="4f8ba-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4f8ba-127">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="4f8ba-128">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="4f8ba-128">End of server support</span></span><br/>    | <span data-ttu-id="4f8ba-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4f8ba-129">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="4f8ba-130">Header</span><span class="sxs-lookup"><span data-stu-id="4f8ba-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f8ba-131"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f8ba-131"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f8ba-132">IDL</span><span class="sxs-lookup"><span data-stu-id="4f8ba-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4f8ba-133"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4f8ba-133"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="4f8ba-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4f8ba-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f8ba-135"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f8ba-135"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f8ba-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4f8ba-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f8ba-137">**Iumumuseridentity**</span><span class="sxs-lookup"><span data-stu-id="4f8ba-137">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="4f8ba-138">**Iendumuseridentity:: Skip**</span><span class="sxs-lookup"><span data-stu-id="4f8ba-138">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="4f8ba-139">**Ienumumuseridentity:: Reset**</span><span class="sxs-lookup"><span data-stu-id="4f8ba-139">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="4f8ba-140">**Ienumumuseridentity:: Next**</span><span class="sxs-lookup"><span data-stu-id="4f8ba-140">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> </dl>

 

 




