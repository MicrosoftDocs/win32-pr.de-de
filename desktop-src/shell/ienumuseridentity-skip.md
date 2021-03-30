---
description: 'Iendumuseridentity:: Skip wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.'
ms.assetid: bb19ae50-b384-48fb-9272-15e3e3eaa9d0
title: 'Ienumumuseridentity:: Skip-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Skip
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: cedd4f3c6e9736e26cbf8d58f27f805f0f5d33a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994599"
---
# <a name="ienumuseridentityskip-method"></a><span data-ttu-id="1673d-104">Ienumumuseridentity:: Skip-Methode</span><span class="sxs-lookup"><span data-stu-id="1673d-104">IEnumUserIdentity::Skip method</span></span>

<span data-ttu-id="1673d-105">\[**Iendumuseridentity:: Skip** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="1673d-105">\[**IEnumUserIdentity::Skip** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="1673d-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="1673d-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="1673d-107">Überspringt eine angegebene Anzahl von Benutzer Identitäts Schnittstellen in der-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="1673d-107">Skips a given number of user identity interfaces in the enumeration.</span></span> <span data-ttu-id="1673d-108">Wird beim Abrufen von Schnittstellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="1673d-108">Used when retrieving interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="1673d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1673d-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="1673d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1673d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1673d-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1673d-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1673d-112">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="1673d-112">Type: **ULONG**</span></span>

<span data-ttu-id="1673d-113">Die Anzahl der zu überspringenden Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="1673d-113">The number of interfaces to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1673d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1673d-114">Return value</span></span>

<span data-ttu-id="1673d-115">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1673d-115">Type: **HRESULT**</span></span>

<span data-ttu-id="1673d-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="1673d-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1673d-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1673d-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1673d-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1673d-118">Remarks</span></span>

<span data-ttu-id="1673d-119">[**Ienumumuseridentity**](ienumuseridentity.md) behält eine interne Anzahl bei, die angibt, welche Schnittstelle als nächstes abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1673d-119">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="1673d-120">Um diese Anzahl zu erhöhen, ohne Schnittstellen abzurufen, rufen Sie diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="1673d-120">To increment this count without retrieving interfaces, call this method.</span></span> <span data-ttu-id="1673d-121">Um die Anzahl zurückzusetzen, nennen Sie [**ienumumuseridentity:: Reset**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="1673d-121">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1673d-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1673d-122">Requirements</span></span>



| <span data-ttu-id="1673d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1673d-123">Requirement</span></span> | <span data-ttu-id="1673d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1673d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1673d-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1673d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1673d-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1673d-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1673d-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1673d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1673d-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1673d-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1673d-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1673d-129">End of client support</span></span><br/>    | <span data-ttu-id="1673d-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1673d-130">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="1673d-131">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="1673d-131">End of server support</span></span><br/>    | <span data-ttu-id="1673d-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1673d-132">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="1673d-133">Header</span><span class="sxs-lookup"><span data-stu-id="1673d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1673d-134"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="1673d-134"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="1673d-135">IDL</span><span class="sxs-lookup"><span data-stu-id="1673d-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1673d-136"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1673d-136"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="1673d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1673d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1673d-138"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1673d-138"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1673d-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1673d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1673d-140">**Iumumuseridentity**</span><span class="sxs-lookup"><span data-stu-id="1673d-140">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="1673d-141">**Ienumumuseridentity:: Reset**</span><span class="sxs-lookup"><span data-stu-id="1673d-141">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="1673d-142">**Ienumumuseridentity:: Next**</span><span class="sxs-lookup"><span data-stu-id="1673d-142">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> <dt>

[<span data-ttu-id="1673d-143">**Iendumuseridentity:: GetCount**</span><span class="sxs-lookup"><span data-stu-id="1673d-143">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> </dl>

 

 




