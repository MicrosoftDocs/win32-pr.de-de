---
description: Getorion wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: 20b1c1d0-b09f-43a8-9026-9cdbac28c108
title: 'IUserIdentity2:: getordin-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.GetOrdinal
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f5a7e875e92342363722858b3ac714171cb547b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980048"
---
# <a name="iuseridentity2getordinal-method"></a><span data-ttu-id="bd7e1-104">IUserIdentity2:: getordindiningmethode</span><span class="sxs-lookup"><span data-stu-id="bd7e1-104">IUserIdentity2::GetOrdinal method</span></span>

<span data-ttu-id="bd7e1-105">\[**Getorion** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="bd7e1-105">\[**GetOrdinal** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="bd7e1-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="bd7e1-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="bd7e1-107">Ruft die Ordinalzahl für diese Identität ab.</span><span class="sxs-lookup"><span data-stu-id="bd7e1-107">Gets the ordinal number for this identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd7e1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd7e1-108">Syntax</span></span>


```C++
HRESULT GetOrdinal(
  [out] DWORD *dwOrdinal
);
```



## <a name="parameters"></a><span data-ttu-id="bd7e1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd7e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd7e1-110">*dwordinon* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bd7e1-110">*dwOrdinal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd7e1-111">Typ: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="bd7e1-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="bd7e1-112">Ein Zeiger auf einen _ \*DWORD\*\*-Wert, der die Ordinalzahl für diese Identität empfängt.</span><span class="sxs-lookup"><span data-stu-id="bd7e1-112">A pointer to a _ *DWORD*\* value that receives the ordinal number for this identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd7e1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd7e1-113">Return value</span></span>

<span data-ttu-id="bd7e1-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bd7e1-114">Type: **HRESULT**</span></span>

<span data-ttu-id="bd7e1-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="bd7e1-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bd7e1-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd7e1-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd7e1-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd7e1-117">Remarks</span></span>

<span data-ttu-id="bd7e1-118">Die Ordinalzahl bestimmt die Reihenfolge der Identitäten in der Identitäts Liste, bleibt jedoch möglicherweise nicht während der Vorgänge für die Identitäten erhalten.</span><span class="sxs-lookup"><span data-stu-id="bd7e1-118">The ordinal determines the order of the identities in the identity list, but may not persist throughout operations on the identities.</span></span> <span data-ttu-id="bd7e1-119">Um einen eindeutigen Wert für eine Identität abzurufen, nennen Sie [**GetCookie**](iuseridentity-getcookie.md).</span><span class="sxs-lookup"><span data-stu-id="bd7e1-119">To get a unique value for an identity, call [**GetCookie**](iuseridentity-getcookie.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd7e1-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="bd7e1-120">Requirements</span></span>



| <span data-ttu-id="bd7e1-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd7e1-121">Requirement</span></span> | <span data-ttu-id="bd7e1-122">Wert</span><span class="sxs-lookup"><span data-stu-id="bd7e1-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd7e1-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd7e1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bd7e1-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd7e1-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bd7e1-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd7e1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bd7e1-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd7e1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bd7e1-127">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="bd7e1-127">End of client support</span></span><br/>    | <span data-ttu-id="bd7e1-128">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bd7e1-128">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="bd7e1-129">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="bd7e1-129">End of server support</span></span><br/>    | <span data-ttu-id="bd7e1-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bd7e1-130">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="bd7e1-131">Header</span><span class="sxs-lookup"><span data-stu-id="bd7e1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd7e1-132"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd7e1-132"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="bd7e1-133">IDL</span><span class="sxs-lookup"><span data-stu-id="bd7e1-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bd7e1-134"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bd7e1-134"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="bd7e1-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bd7e1-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd7e1-136"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd7e1-136"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd7e1-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bd7e1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd7e1-138">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="bd7e1-138">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="bd7e1-139">**GetCookie**</span><span class="sxs-lookup"><span data-stu-id="bd7e1-139">**GetCookie**</span></span>](iuseridentity-getcookie.md)
</dt> </dl>

 

 




