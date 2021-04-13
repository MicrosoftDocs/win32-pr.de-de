---
description: GetCookie wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: 4a743d64-9af3-43cf-9a9f-d808676ab337
title: 'Iuseridentity:: GetCookie-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 96cafb13f2c90c41e4aa6dcaaa72cf052757d0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977913"
---
# <a name="iuseridentitygetcookie-method"></a><span data-ttu-id="fe16e-104">Iuseridentity:: GetCookie-Methode</span><span class="sxs-lookup"><span data-stu-id="fe16e-104">IUserIdentity::GetCookie method</span></span>

<span data-ttu-id="fe16e-105">\[**GetCookie** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="fe16e-105">\[**GetCookie** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="fe16e-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="fe16e-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="fe16e-107">Ruft das Cookie ab, mit dem diese Benutzeridentität eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="fe16e-107">Gets the cookie used to uniquely identify this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe16e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe16e-108">Syntax</span></span>


```C++
HRESULT GetCookie(
  [out] GUID *puidCookie
);
```



## <a name="parameters"></a><span data-ttu-id="fe16e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe16e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe16e-110">*puidcookie* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fe16e-110">*puidCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe16e-111">Geben Sie Folgendes ein: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="fe16e-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="fe16e-112">Ein Zeiger auf einen _ \*GUID\*\*-Wert, der das Cookie empfängt, das zum eindeutigen Identifizieren dieser Benutzeridentität verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe16e-112">A pointer to a _ *GUID*\* value that receives the cookie used to uniquely identify this user identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe16e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe16e-113">Return value</span></span>

<span data-ttu-id="fe16e-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fe16e-114">Type: **HRESULT**</span></span>

<span data-ttu-id="fe16e-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="fe16e-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fe16e-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe16e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe16e-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fe16e-117">Requirements</span></span>



| <span data-ttu-id="fe16e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe16e-118">Requirement</span></span> | <span data-ttu-id="fe16e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fe16e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe16e-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe16e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fe16e-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe16e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fe16e-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe16e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fe16e-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe16e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fe16e-124">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="fe16e-124">End of client support</span></span><br/>    | <span data-ttu-id="fe16e-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fe16e-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="fe16e-126">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="fe16e-126">End of server support</span></span><br/>    | <span data-ttu-id="fe16e-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fe16e-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="fe16e-128">Header</span><span class="sxs-lookup"><span data-stu-id="fe16e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe16e-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe16e-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe16e-130">IDL</span><span class="sxs-lookup"><span data-stu-id="fe16e-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fe16e-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fe16e-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="fe16e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fe16e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe16e-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe16e-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe16e-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fe16e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe16e-135">**Iuseridentity**</span><span class="sxs-lookup"><span data-stu-id="fe16e-135">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="fe16e-136">**GetOrdinal**</span><span class="sxs-lookup"><span data-stu-id="fe16e-136">**GetOrdinal**</span></span>](iuseridentity2-getordinal.md)
</dt> </dl>

 

 




