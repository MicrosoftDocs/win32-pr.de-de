---
description: 'IUserIdentity2:: SetName wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.'
ms.assetid: 1c9c3beb-fa1c-4b4d-9cfd-656b97949036
title: 'IUserIdentity2:: SetName-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.SetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 0b0fd06ef4b582987e41c2343f2d4596db6b8528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980040"
---
# <a name="iuseridentity2setname-method"></a><span data-ttu-id="82a09-104">IUserIdentity2:: SetName-Methode</span><span class="sxs-lookup"><span data-stu-id="82a09-104">IUserIdentity2::SetName method</span></span>

<span data-ttu-id="82a09-105">\[**IUserIdentity2:: SetName** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="82a09-105">\[**IUserIdentity2::SetName** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="82a09-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="82a09-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="82a09-107">Legt den anzeigen amen der Identität fest.</span><span class="sxs-lookup"><span data-stu-id="82a09-107">Sets the display name of the identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="82a09-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="82a09-108">Syntax</span></span>


```C++
HRESULT SetName(
  [in] WCHAR *pszName
);
```



## <a name="parameters"></a><span data-ttu-id="82a09-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="82a09-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82a09-110">*pszName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82a09-110">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a09-111">Typ: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="82a09-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="82a09-112">Die breit Zeichen-Zeichenfolge, die den neuen Namen der Identität enthält.</span><span class="sxs-lookup"><span data-stu-id="82a09-112">The wide-character string that contains the new name of the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82a09-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82a09-113">Return value</span></span>

<span data-ttu-id="82a09-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="82a09-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="82a09-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="82a09-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="82a09-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="82a09-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="82a09-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="82a09-117">Requirements</span></span>



| <span data-ttu-id="82a09-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82a09-118">Requirement</span></span> | <span data-ttu-id="82a09-119">Wert</span><span class="sxs-lookup"><span data-stu-id="82a09-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82a09-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82a09-120">Minimum supported client</span></span><br/> | <span data-ttu-id="82a09-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82a09-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="82a09-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82a09-122">Minimum supported server</span></span><br/> | <span data-ttu-id="82a09-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82a09-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="82a09-124">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="82a09-124">End of client support</span></span><br/>    | <span data-ttu-id="82a09-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="82a09-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="82a09-126">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="82a09-126">End of server support</span></span><br/>    | <span data-ttu-id="82a09-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="82a09-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="82a09-128">Header</span><span class="sxs-lookup"><span data-stu-id="82a09-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="82a09-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="82a09-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="82a09-130">IDL</span><span class="sxs-lookup"><span data-stu-id="82a09-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="82a09-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="82a09-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="82a09-132">DLL</span><span class="sxs-lookup"><span data-stu-id="82a09-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82a09-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82a09-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82a09-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="82a09-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82a09-135">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="82a09-135">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="82a09-136">**GetName**</span><span class="sxs-lookup"><span data-stu-id="82a09-136">**GetName**</span></span>](iuseridentity-getname.md)
</dt> </dl>

 

 




