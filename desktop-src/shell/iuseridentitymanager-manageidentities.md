---
description: 'Iuseridentitymanager:: manageidentities wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.'
ms.assetid: 9a5a85bd-d007-4247-859b-e402ed290785
title: 'Iuseridentitymanager:: manageidentities-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.ManageIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: b5b782a56324faf19dd1527d2cd363d26f0e337c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342438"
---
# <a name="iuseridentitymanagermanageidentities-method"></a><span data-ttu-id="d12bd-104">Iuseridentitymanager:: manageidentities-Methode</span><span class="sxs-lookup"><span data-stu-id="d12bd-104">IUserIdentityManager::ManageIdentities method</span></span>

<span data-ttu-id="d12bd-105">\[**Iuseridentitymanager:: manageidentities** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="d12bd-105">\[**IUserIdentityManager::ManageIdentities** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="d12bd-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="d12bd-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="d12bd-107">Zeigt dem Benutzer eine Benutzeroberfläche an und ermöglicht dem Benutzer die Verwaltung von Benutzer Identitäten.</span><span class="sxs-lookup"><span data-stu-id="d12bd-107">Displays a UI to the user, allowing the user to manage user identities.</span></span>

## <a name="syntax"></a><span data-ttu-id="d12bd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d12bd-108">Syntax</span></span>


```C++
HRESULT ManageIdentities(
  [in] HWND  hwndParent,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d12bd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d12bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d12bd-110">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d12bd-110">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d12bd-111">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="d12bd-111">Type: **HWND**</span></span>

<span data-ttu-id="d12bd-112">Ein **HWND** -Wert, der ein Fenster identifiziert, das nach dem verwerfen der Benutzeroberfläche in den Vordergrund gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d12bd-112">An **HWND** value that identifies a window that will be brought to the foreground after the UI is dismissed.</span></span>

</dd> <dt>

<span data-ttu-id="d12bd-113">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d12bd-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d12bd-114">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d12bd-114">Type: **DWORD**</span></span>

<span data-ttu-id="d12bd-115">Optionale Flags, um zu definieren, wie sich die Benutzeroberfläche verhält.</span><span class="sxs-lookup"><span data-stu-id="d12bd-115">Optional flags to define how the UI will behave.</span></span> <span data-ttu-id="d12bd-116">Legen Sie auf uimi \_ \_ neue \_ Identität erstellen fest, um den Benutzer zur Erstellung einer neuen Identität aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="d12bd-116">Set to UIMI\_CREATE\_NEW\_IDENTITY to prompt the user to create a new identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d12bd-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d12bd-117">Return value</span></span>

<span data-ttu-id="d12bd-118">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d12bd-118">Type: **HRESULT**</span></span>

<span data-ttu-id="d12bd-119">Das Ergebnis des Verwaltungs Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="d12bd-119">The result of the management operation.</span></span> <span data-ttu-id="d12bd-120">Bei erfolgreicher Ausführung wird S OK zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="d12bd-120">If successful, it returns S\_OK.</span></span> <span data-ttu-id="d12bd-121">Andernfalls wird einer der folgenden Fehlercodes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d12bd-121">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="d12bd-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d12bd-122">Return code</span></span>                                                                                            | <span data-ttu-id="d12bd-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d12bd-123">Description</span></span>                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="d12bd-124"><dt>**E- \_ Identitäten \_ deaktiviert**</dt></span><span class="sxs-lookup"><span data-stu-id="d12bd-124"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="d12bd-125">Die Identitätsverwaltung ist im System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d12bd-125">Identity management is disabled on the system.</span></span><br/> |
| <dl> <span data-ttu-id="d12bd-126"><dt>**E- \_ Benutzer \_ abgebrochen**</dt></span><span class="sxs-lookup"><span data-stu-id="d12bd-126"><dt>**E\_USER\_CANCELLED**</dt></span></span> </dl>      | <span data-ttu-id="d12bd-127">Der Benutzer hat das Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="d12bd-127">The user canceled the dialog.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="d12bd-128">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d12bd-128">Requirements</span></span>



| <span data-ttu-id="d12bd-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d12bd-129">Requirement</span></span> | <span data-ttu-id="d12bd-130">Wert</span><span class="sxs-lookup"><span data-stu-id="d12bd-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d12bd-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d12bd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d12bd-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d12bd-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d12bd-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d12bd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d12bd-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d12bd-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d12bd-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d12bd-135">End of client support</span></span><br/>    | <span data-ttu-id="d12bd-136">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d12bd-136">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="d12bd-137">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="d12bd-137">End of server support</span></span><br/>    | <span data-ttu-id="d12bd-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d12bd-138">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="d12bd-139">Header</span><span class="sxs-lookup"><span data-stu-id="d12bd-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d12bd-140"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="d12bd-140"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="d12bd-141">IDL</span><span class="sxs-lookup"><span data-stu-id="d12bd-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d12bd-142"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d12bd-142"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="d12bd-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d12bd-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d12bd-144"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d12bd-144"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d12bd-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d12bd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d12bd-146">**Iuseridentitymanager**</span><span class="sxs-lookup"><span data-stu-id="d12bd-146">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="d12bd-147">**Iuseridentitymanager:: LOGON**</span><span class="sxs-lookup"><span data-stu-id="d12bd-147">**IUserIdentityManager::Logon**</span></span>](iuseridentitymanager-logon.md)
</dt> <dt>

[<span data-ttu-id="d12bd-148">**Iuseridentitymanager:: abmelden**</span><span class="sxs-lookup"><span data-stu-id="d12bd-148">**IUserIdentityManager::Logoff**</span></span>](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 




