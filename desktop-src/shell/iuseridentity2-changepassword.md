---
description: ChangePassword wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: 'IUserIdentity2:: ChangePassword-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.ChangePassword
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: dd4b858924e4b042b3d7a0636d90eb582e9506df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977889"
---
# <a name="iuseridentity2changepassword-method"></a><span data-ttu-id="2329d-104">IUserIdentity2:: ChangePassword-Methode</span><span class="sxs-lookup"><span data-stu-id="2329d-104">IUserIdentity2::ChangePassword method</span></span>

<span data-ttu-id="2329d-105">\[**ChangePassword** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="2329d-105">\[**ChangePassword** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="2329d-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="2329d-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="2329d-107">Legt ein neues Kennwort für die Identität fest.</span><span class="sxs-lookup"><span data-stu-id="2329d-107">Sets a new password for the identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="2329d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2329d-108">Syntax</span></span>


```C++
HRESULT ChangePassword(
  [in] WCHAR *szOldPass,
  [in] WCHAR *szNewPass
);
```



## <a name="parameters"></a><span data-ttu-id="2329d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2329d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2329d-110">*szoldpass* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2329d-110">*szOldPass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2329d-111">Typ: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="2329d-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="2329d-112">Die Zeichenfolge mit breit Zeichen, die das Kennwort enthält, das derzeit der Identität zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2329d-112">The wide-character string that contains the password currently associated with the identity.</span></span>

</dd> <dt>

<span data-ttu-id="2329d-113">_szNewPass \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2329d-113">_szNewPass\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2329d-114">Typ: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="2329d-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="2329d-115">Die Zeichenfolge mit breit Zeichen, die das neue Kennwort enthält, das der Identität zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2329d-115">The wide-character string that contains the new password to be associated with the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2329d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2329d-116">Return value</span></span>

<span data-ttu-id="2329d-117">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2329d-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2329d-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2329d-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2329d-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2329d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2329d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2329d-120">Remarks</span></span>

<span data-ttu-id="2329d-121">Der Wert von *szoldpass* muss mit dem aktuellen Kennwort der Identität für den anzuwendenden *sznewpass* -Wert identisch sein.</span><span class="sxs-lookup"><span data-stu-id="2329d-121">The value of *szOldPass* must match the current password of the identity for *szNewPass* to be applied.</span></span> <span data-ttu-id="2329d-122">Ein falscher Wert von *szoldpass* führt zu einem Rückgabewert von E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="2329d-122">An incorrect value of *szOldPass* will result in a return value of E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2329d-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2329d-123">Requirements</span></span>



| <span data-ttu-id="2329d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2329d-124">Requirement</span></span> | <span data-ttu-id="2329d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2329d-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2329d-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2329d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2329d-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2329d-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2329d-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2329d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2329d-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2329d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2329d-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="2329d-130">End of client support</span></span><br/>    | <span data-ttu-id="2329d-131">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2329d-131">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="2329d-132">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="2329d-132">End of server support</span></span><br/>    | <span data-ttu-id="2329d-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2329d-133">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="2329d-134">Header</span><span class="sxs-lookup"><span data-stu-id="2329d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2329d-135"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="2329d-135"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="2329d-136">IDL</span><span class="sxs-lookup"><span data-stu-id="2329d-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2329d-137"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2329d-137"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="2329d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2329d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2329d-139"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2329d-139"><dt>Msident.dll</dt></span></span> </dl> |



 

 




