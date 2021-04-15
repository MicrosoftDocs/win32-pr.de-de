---
description: Getidentityfolder wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: cd3370a2-b393-4cb9-ad9c-a46086987aaa
title: 'Iuseridentity:: getidentityfolder-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetIdentityFolder
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 9f2644570bb7ccc2ae5bee8a37d4471ffb65861a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977904"
---
# <a name="iuseridentitygetidentityfolder-method"></a><span data-ttu-id="81a65-104">Iuseridentity:: getidentityfolder-Methode</span><span class="sxs-lookup"><span data-stu-id="81a65-104">IUserIdentity::GetIdentityFolder method</span></span>

<span data-ttu-id="81a65-105">\[**Getidentityfolder** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="81a65-105">\[**GetIdentityFolder** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="81a65-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="81a65-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="81a65-107">Ruft den Datei Ordner ab, der dieser Identität zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="81a65-107">Gets the file folder associated with this identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="81a65-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="81a65-108">Syntax</span></span>


```C++
HRESULT GetIdentityFolder(
  [in] DWORD dwFlags,
  [in] WCHAR *pszPath,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a><span data-ttu-id="81a65-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="81a65-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81a65-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81a65-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a65-111">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="81a65-111">Type: **DWORD**</span></span>

<span data-ttu-id="81a65-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="81a65-112">Required.</span></span> <span data-ttu-id="81a65-113">Ein-Wert, der angibt, ob der dieser Identität zugeordnete Ordner roamingbasiert.</span><span class="sxs-lookup"><span data-stu-id="81a65-113">A value that specifies whether the folder associated with this identity is roaming.</span></span> <span data-ttu-id="81a65-114">Muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="81a65-114">Must be one of the following values.</span></span>

<dt>



 <span data-ttu-id="81a65-115">(GIF \_ \_roamingordner)</span><span class="sxs-lookup"><span data-stu-id="81a65-115">(GIF\_ROAMING\_FOLDER)</span></span>


</dt> <dd>

<span data-ttu-id="81a65-116">Der Ordner ist Roaming.</span><span class="sxs-lookup"><span data-stu-id="81a65-116">The folder is roaming.</span></span>

</dd> <dt>



 <span data-ttu-id="81a65-117">(GIF \_ nicht \_ \_ roamingordner)</span><span class="sxs-lookup"><span data-stu-id="81a65-117">(GIF\_NON\_ROAMING\_FOLDER)</span></span>


</dt> <dd>

<span data-ttu-id="81a65-118">Der Ordner ist "local".</span><span class="sxs-lookup"><span data-stu-id="81a65-118">The folder is local.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="81a65-119">*pszpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81a65-119">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a65-120">Typ: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="81a65-120">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="81a65-121">Ein Zeiger auf eine breit Zeichen-Zeichenfolge, die den Ordner Pfad empfängt.</span><span class="sxs-lookup"><span data-stu-id="81a65-121">A pointer to a wide-character string that receives the folder path.</span></span>

</dd> <dt>

<span data-ttu-id="81a65-122">_ulBuffSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81a65-122">_ulBuffSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a65-123">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="81a65-123">Type: **ULONG**</span></span>

<span data-ttu-id="81a65-124">Ein-Wert, der die Größe von *pszpath* angibt.</span><span class="sxs-lookup"><span data-stu-id="81a65-124">A value that specifies the size of *pszPath*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81a65-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81a65-125">Return value</span></span>

<span data-ttu-id="81a65-126">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="81a65-126">Type: **HRESULT**</span></span>

<span data-ttu-id="81a65-127">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="81a65-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="81a65-128">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="81a65-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="81a65-129">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="81a65-129">Requirements</span></span>



| <span data-ttu-id="81a65-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81a65-130">Requirement</span></span> | <span data-ttu-id="81a65-131">Wert</span><span class="sxs-lookup"><span data-stu-id="81a65-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81a65-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81a65-132">Minimum supported client</span></span><br/> | <span data-ttu-id="81a65-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81a65-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="81a65-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81a65-134">Minimum supported server</span></span><br/> | <span data-ttu-id="81a65-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81a65-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="81a65-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="81a65-136">End of client support</span></span><br/>    | <span data-ttu-id="81a65-137">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="81a65-137">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="81a65-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="81a65-138">End of server support</span></span><br/>    | <span data-ttu-id="81a65-139">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="81a65-139">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="81a65-140">Header</span><span class="sxs-lookup"><span data-stu-id="81a65-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="81a65-141"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="81a65-141"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="81a65-142">IDL</span><span class="sxs-lookup"><span data-stu-id="81a65-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="81a65-143"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="81a65-143"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="81a65-144">DLL</span><span class="sxs-lookup"><span data-stu-id="81a65-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81a65-145"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81a65-145"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81a65-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="81a65-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81a65-147">**Iuseridentity**</span><span class="sxs-lookup"><span data-stu-id="81a65-147">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="81a65-148">**Iuseridentity:: openidentityregkey**</span><span class="sxs-lookup"><span data-stu-id="81a65-148">**IUserIdentity::OpenIdentityRegKey**</span></span>](iuseridentity-openidentityregkey.md)
</dt> </dl>

 

 




