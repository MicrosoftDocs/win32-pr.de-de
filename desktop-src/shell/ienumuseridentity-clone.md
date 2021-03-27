---
description: 'Ienumumuseridentity:: Clone wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.'
ms.assetid: dde9afca-db8d-41ba-afa0-94eadecb695b
title: 'Ienumumuseridentity:: Clone-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Clone
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: ebdec426fe7ab591c801c00b637211e903cf5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994614"
---
# <a name="ienumuseridentityclone-method"></a><span data-ttu-id="d06fb-104">Ienumumuseridentity:: Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="d06fb-104">IEnumUserIdentity::Clone method</span></span>

<span data-ttu-id="d06fb-105">\[**Ienumumuseridentity:: Clone** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="d06fb-105">\[**IEnumUserIdentity::Clone** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="d06fb-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="d06fb-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="d06fb-107">Ruft eine Kopie der aktuellen Enumeration ab.</span><span class="sxs-lookup"><span data-stu-id="d06fb-107">Gets a copy of the current enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="d06fb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d06fb-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumUserIdentity **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="d06fb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d06fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d06fb-110">*ppum* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d06fb-110">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d06fb-111">Typ: **[ **iumumuseridentity**](ienumuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d06fb-111">Type: **[**IEnumUserIdentity**](ienumuseridentity.md)\*\***</span></span>

<span data-ttu-id="d06fb-112">Die Adresse eines Zeigers, der eine Kopie dieser Enumeration empfängt.</span><span class="sxs-lookup"><span data-stu-id="d06fb-112">The address of a pointer that receives a copy of this enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d06fb-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d06fb-113">Return value</span></span>

<span data-ttu-id="d06fb-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d06fb-114">Type: **HRESULT**</span></span>

<span data-ttu-id="d06fb-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d06fb-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d06fb-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d06fb-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d06fb-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d06fb-117">Remarks</span></span>

<span data-ttu-id="d06fb-118">[**Ienumumuseridentity**](ienumuseridentity.md) behält eine interne Anzahl bei, die angibt, welche Schnittstelle als nächstes abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d06fb-118">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="d06fb-119">Der Wert dieser Anzahl wird auf die von *ppum* empfangene Schnittstelle angewendet.</span><span class="sxs-lookup"><span data-stu-id="d06fb-119">The value of this count will be applied to the interface received by *ppenum*.</span></span> <span data-ttu-id="d06fb-120">Um die Anzahl zurückzusetzen, nennen Sie [**ienumumuseridentity:: Reset**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="d06fb-120">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d06fb-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d06fb-121">Requirements</span></span>



| <span data-ttu-id="d06fb-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d06fb-122">Requirement</span></span> | <span data-ttu-id="d06fb-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d06fb-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d06fb-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d06fb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d06fb-125">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d06fb-125">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d06fb-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d06fb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d06fb-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d06fb-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d06fb-128">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d06fb-128">End of client support</span></span><br/>    | <span data-ttu-id="d06fb-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d06fb-129">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="d06fb-130">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="d06fb-130">End of server support</span></span><br/>    | <span data-ttu-id="d06fb-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d06fb-131">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="d06fb-132">Header</span><span class="sxs-lookup"><span data-stu-id="d06fb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d06fb-133"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="d06fb-133"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="d06fb-134">IDL</span><span class="sxs-lookup"><span data-stu-id="d06fb-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d06fb-135"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d06fb-135"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="d06fb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d06fb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d06fb-137"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d06fb-137"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d06fb-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d06fb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d06fb-139">**Iumumuseridentity**</span><span class="sxs-lookup"><span data-stu-id="d06fb-139">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="d06fb-140">**Ienumumuseridentity:: Reset**</span><span class="sxs-lookup"><span data-stu-id="d06fb-140">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> </dl>

 

 




