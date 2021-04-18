---
description: 'Iuseridentity:: GetName wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.'
ms.assetid: 4db24dd2-d2b8-4a58-9c16-0e721bc195da
title: 'Iuseridentity:: GetName-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 88c0a3d08ff917c2cc9fd59f15e4c23fc22fc79d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979488"
---
# <a name="iuseridentitygetname-method"></a><span data-ttu-id="5408a-104">Iuseridentity:: GetName-Methode</span><span class="sxs-lookup"><span data-stu-id="5408a-104">IUserIdentity::GetName method</span></span>

<span data-ttu-id="5408a-105">\[**Iuseridentity:: GetName** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="5408a-105">\[**IUserIdentity::GetName** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="5408a-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="5408a-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="5408a-107">Ruft den Namen ab, der dieser Benutzeridentität zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5408a-107">Gets the name associated with this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="5408a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5408a-108">Syntax</span></span>


```C++
HRESULT GetName(
  [in] WCHAR *pszName,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a><span data-ttu-id="5408a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5408a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5408a-110">*pszName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5408a-110">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5408a-111">Typ: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="5408a-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="5408a-112">Ein Zeiger auf eine breit Zeichen-Zeichenfolge, die den Namen dieser Benutzeridentität empfängt.</span><span class="sxs-lookup"><span data-stu-id="5408a-112">A pointer to a wide-character string that receives the name of this user identity.</span></span>

</dd> <dt>

<span data-ttu-id="5408a-113">_ulBuffSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5408a-113">_ulBuffSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5408a-114">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="5408a-114">Type: **ULONG**</span></span>

<span data-ttu-id="5408a-115">Ein-Wert, der die Größe von *pszName* angibt.</span><span class="sxs-lookup"><span data-stu-id="5408a-115">A value that specifies the size of *pszName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5408a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5408a-116">Return value</span></span>

<span data-ttu-id="5408a-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5408a-117">Type: **HRESULT**</span></span>

<span data-ttu-id="5408a-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5408a-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5408a-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5408a-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5408a-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5408a-120">Requirements</span></span>



| <span data-ttu-id="5408a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5408a-121">Requirement</span></span> | <span data-ttu-id="5408a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5408a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5408a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5408a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5408a-124">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5408a-124">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5408a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5408a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5408a-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5408a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5408a-127">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="5408a-127">End of client support</span></span><br/>    | <span data-ttu-id="5408a-128">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5408a-128">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="5408a-129">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="5408a-129">End of server support</span></span><br/>    | <span data-ttu-id="5408a-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5408a-130">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="5408a-131">Header</span><span class="sxs-lookup"><span data-stu-id="5408a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5408a-132"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="5408a-132"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="5408a-133">IDL</span><span class="sxs-lookup"><span data-stu-id="5408a-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5408a-134"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5408a-134"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="5408a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5408a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5408a-136"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5408a-136"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5408a-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5408a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5408a-138">**Iuseridentity**</span><span class="sxs-lookup"><span data-stu-id="5408a-138">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="5408a-139">**SetName**</span><span class="sxs-lookup"><span data-stu-id="5408a-139">**SetName**</span></span>](iuseridentity2-setname.md)
</dt> </dl>

 

 




