---
description: 'Ienumumuseridentity:: Next wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.'
ms.assetid: 2c8dfe36-c1bb-49f8-8847-f355cfab2984
title: 'Ienumumuseridentity:: Next-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Next
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 763b2b4a612596c5f02a9826ad2e9c09ab8e4b0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994607"
---
# <a name="ienumuseridentitynext-method"></a><span data-ttu-id="98484-104">Ienumumuseridentity:: Next-Methode</span><span class="sxs-lookup"><span data-stu-id="98484-104">IEnumUserIdentity::Next method</span></span>

<span data-ttu-id="98484-105">\[**Ienumumuseridentity:: Next** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="98484-105">\[**IEnumUserIdentity::Next** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="98484-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="98484-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="98484-107">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="98484-107">Deprecated.</span></span> <span data-ttu-id="98484-108">Ruft ein Array von Benutzer Identitäts Schnittstellen aus der-Enumeration ab.</span><span class="sxs-lookup"><span data-stu-id="98484-108">Retrieves an array of user identity interfaces from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="98484-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="98484-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG    celt,
  [out] IUnknown **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="98484-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="98484-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98484-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98484-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98484-112">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="98484-112">Type: **ULONG**</span></span>

<span data-ttu-id="98484-113">Ein **ulong** -Wert, der die Anzahl der abzurufenden Schnittstellen darstellt.</span><span class="sxs-lookup"><span data-stu-id="98484-113">A **ULONG** value that represents the number of interfaces to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="98484-114">*rgelt* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="98484-114">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98484-115">Typ: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="98484-115">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="98484-116">Die Adresse eines Zeigers, der die Schnittstellen empfängt.</span><span class="sxs-lookup"><span data-stu-id="98484-116">The address of a pointer that receives the interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="98484-117">*pceltfetch* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="98484-117">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98484-118">Typ: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="98484-118">Type: \**ULONG\** _</span></span>

<span data-ttu-id="98484-119">Die Adresse eines Zeigers, der die Anzahl der erfolgreich abgerufenen Schnittstellen empfängt.</span><span class="sxs-lookup"><span data-stu-id="98484-119">The address of a pointer that receives the number of interfaces successfully retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98484-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98484-120">Return value</span></span>

<span data-ttu-id="98484-121">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="98484-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="98484-122">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="98484-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="98484-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="98484-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="98484-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98484-124">Remarks</span></span>

<span data-ttu-id="98484-125">[**Ienumumuseridentity**](ienumuseridentity.md) behält eine interne Anzahl bei, die angibt, welche Schnittstelle als nächstes abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="98484-125">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="98484-126">Bei mehreren Aufrufen dieser Methode wird diese Anzahl nicht zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="98484-126">Multiple calls to this method will not reset this count.</span></span> <span data-ttu-id="98484-127">Um die Anzahl zurückzusetzen, nennen Sie [**ienumumuseridentity:: Reset**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="98484-127">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span> <span data-ttu-id="98484-128">Um die Anzahl zu erhöhen, ohne Schnittstellen abzurufen, rufen Sie [**ienumumuseridentity:: Skip**](ienumuseridentity-skip.md)auf.</span><span class="sxs-lookup"><span data-stu-id="98484-128">To increment the count without retrieving interfaces, call [**IEnumUserIdentity::Skip**](ienumuseridentity-skip.md).</span></span>

<span data-ttu-id="98484-129">Der Wert von " *celt* " sollte nicht den Wert überschreiten, der von " [**ienumumuseridentity:: GetCount**](ienumuseridentity-getcount.md)" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="98484-129">The value of *celt* should not exceed the value returned by [**IEnumUserIdentity::GetCount**](ienumuseridentity-getcount.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98484-130">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="98484-130">Requirements</span></span>



| <span data-ttu-id="98484-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98484-131">Requirement</span></span> | <span data-ttu-id="98484-132">Wert</span><span class="sxs-lookup"><span data-stu-id="98484-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98484-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98484-133">Minimum supported client</span></span><br/> | <span data-ttu-id="98484-134">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98484-134">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="98484-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98484-135">Minimum supported server</span></span><br/> | <span data-ttu-id="98484-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98484-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="98484-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="98484-137">End of client support</span></span><br/>    | <span data-ttu-id="98484-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="98484-138">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="98484-139">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="98484-139">End of server support</span></span><br/>    | <span data-ttu-id="98484-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="98484-140">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="98484-141">Header</span><span class="sxs-lookup"><span data-stu-id="98484-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="98484-142"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="98484-142"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="98484-143">IDL</span><span class="sxs-lookup"><span data-stu-id="98484-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="98484-144"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="98484-144"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="98484-145">DLL</span><span class="sxs-lookup"><span data-stu-id="98484-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98484-146"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98484-146"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98484-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="98484-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98484-148">**Iumumuseridentity**</span><span class="sxs-lookup"><span data-stu-id="98484-148">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="98484-149">**Iendumuseridentity:: Skip**</span><span class="sxs-lookup"><span data-stu-id="98484-149">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="98484-150">**Ienumumuseridentity:: Reset**</span><span class="sxs-lookup"><span data-stu-id="98484-150">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="98484-151">**Iendumuseridentity:: GetCount**</span><span class="sxs-lookup"><span data-stu-id="98484-151">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> </dl>

 

 
