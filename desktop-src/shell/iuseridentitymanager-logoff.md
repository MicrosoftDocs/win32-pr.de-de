---
description: Die Abmeldung wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: e03fb15c-47d3-40ba-ae70-b7b0ba010004
title: 'Iuseridentitymanager:: Logoff-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logoff
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 4266e6116e43b7b792c3040d7c86a60037ca4c44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104976992"
---
# <a name="iuseridentitymanagerlogoff-method"></a><span data-ttu-id="b1b7e-104">Iuseridentitymanager:: Logoff-Methode</span><span class="sxs-lookup"><span data-stu-id="b1b7e-104">IUserIdentityManager::Logoff method</span></span>

<span data-ttu-id="b1b7e-105">\[Die Abmeldung **wird nicht** unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="b1b7e-105">\[**Logoff** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="b1b7e-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="b1b7e-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="b1b7e-107">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b1b7e-107">Deprecated.</span></span> <span data-ttu-id="b1b7e-108">Melden Sie sich von der aktuellen Identität ab.</span><span class="sxs-lookup"><span data-stu-id="b1b7e-108">Log off the current identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1b7e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1b7e-109">Syntax</span></span>


```C++
HRESULT Logoff(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a><span data-ttu-id="b1b7e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1b7e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1b7e-111">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1b7e-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1b7e-112">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="b1b7e-112">Type: **HWND**</span></span>

<span data-ttu-id="b1b7e-113">Ein **HWND** -Wert, der ein Fenster identifiziert, das nach Abschluss der Abmeldung in den Vordergrund gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b1b7e-113">An **HWND** value that identifies a window that will be brought into the foreground when the logoff is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1b7e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1b7e-114">Return value</span></span>

<span data-ttu-id="b1b7e-115">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b1b7e-115">Type: **HRESULT**</span></span>

<span data-ttu-id="b1b7e-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b1b7e-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b1b7e-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b1b7e-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1b7e-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b1b7e-118">Requirements</span></span>



| <span data-ttu-id="b1b7e-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1b7e-119">Requirement</span></span> | <span data-ttu-id="b1b7e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b1b7e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1b7e-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1b7e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b1b7e-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1b7e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b1b7e-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1b7e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b1b7e-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1b7e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b1b7e-125">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b1b7e-125">End of client support</span></span><br/>    | <span data-ttu-id="b1b7e-126">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b1b7e-126">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="b1b7e-127">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b1b7e-127">End of server support</span></span><br/>    | <span data-ttu-id="b1b7e-128">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b1b7e-128">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="b1b7e-129">Header</span><span class="sxs-lookup"><span data-stu-id="b1b7e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1b7e-130"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1b7e-130"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1b7e-131">IDL</span><span class="sxs-lookup"><span data-stu-id="b1b7e-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b1b7e-132"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b1b7e-132"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="b1b7e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b1b7e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1b7e-134"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1b7e-134"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1b7e-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b1b7e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1b7e-136">**Iuseridentitymanager**</span><span class="sxs-lookup"><span data-stu-id="b1b7e-136">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="b1b7e-137">**Iuseridentitymanager:: LOGON**</span><span class="sxs-lookup"><span data-stu-id="b1b7e-137">**IUserIdentityManager::Logon**</span></span>](iuseridentitymanager-logon.md)
</dt> <dt>

[<span data-ttu-id="b1b7e-138">**Iuseridentitymanager:: manageidentities**</span><span class="sxs-lookup"><span data-stu-id="b1b7e-138">**IUserIdentityManager::ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




