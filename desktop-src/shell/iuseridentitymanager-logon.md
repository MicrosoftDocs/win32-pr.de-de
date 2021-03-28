---
description: 'Iuseridentitymanager:: die Anmeldung wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.'
ms.assetid: ba146ee1-6c9c-4f97-ae90-431aa084ea16
title: 'Iuseridentitymanager:: Logon-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logon
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eee6e0555d45d3f52173fce085d19c14f2ccfe8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127829"
---
# <a name="iuseridentitymanagerlogon-method"></a><span data-ttu-id="46d2f-104">Iuseridentitymanager:: Logon-Methode</span><span class="sxs-lookup"><span data-stu-id="46d2f-104">IUserIdentityManager::Logon method</span></span>

<span data-ttu-id="46d2f-105">\[**Iuseridentitymanager:: die Anmeldung** wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="46d2f-105">\[**IUserIdentityManager::Logon** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="46d2f-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="46d2f-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="46d2f-107">Zeigt dem Benutzer eine Benutzeroberfläche an und ermöglicht dem Benutzer die Auswahl einer Benutzeridentität.</span><span class="sxs-lookup"><span data-stu-id="46d2f-107">Displays a UI to the user, allowing the user to choose a user identity.</span></span> <span data-ttu-id="46d2f-108">Bei erfolgreicher Ausführung wird die Benutzeridentität angemeldet und abgerufen.</span><span class="sxs-lookup"><span data-stu-id="46d2f-108">If successful, the user identity will be logged on and retrieved.</span></span>

## <a name="syntax"></a><span data-ttu-id="46d2f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="46d2f-109">Syntax</span></span>


```C++
HRESULT Logon(
  [in]  HWND          hwndParent,
  [in]  DWORD         dwFlags,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a><span data-ttu-id="46d2f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="46d2f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46d2f-111">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46d2f-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46d2f-112">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="46d2f-112">Type: **HWND**</span></span>

<span data-ttu-id="46d2f-113">Ein **HWND** -Wert, der ein Fenster identifiziert, das nach dem verwerfen der Anmelde Benutzeroberfläche in den Vordergrund gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="46d2f-113">An **HWND** value that identifies a window that will be brought to the foreground after the logon UI is dismissed.</span></span>

</dd> <dt>

<span data-ttu-id="46d2f-114">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46d2f-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46d2f-115">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="46d2f-115">Type: **DWORD**</span></span>

<span data-ttu-id="46d2f-116">Optionale Flags, um zu definieren, wie sich die Benutzeroberfläche verhält.</span><span class="sxs-lookup"><span data-stu-id="46d2f-116">Optional flags to define how the UI will behave.</span></span> <span data-ttu-id="46d2f-117">Legen Sie auf UIL \_ Force UI fest, \_ um die Anzeige der Benutzeroberfläche zu erzwingen, auch wenn bereits eine Identität ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="46d2f-117">Set to UIL\_FORCE\_UI to force the UI to display, even if an identity has already been chosen.</span></span>

</dd> <dt>

<span data-ttu-id="46d2f-118">*ppIdentity* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="46d2f-118">*ppIdentity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46d2f-119">Type: **[ **iuseridentity**](iuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="46d2f-119">Type: **[**IUserIdentity**](iuseridentity.md)\*\***</span></span>

<span data-ttu-id="46d2f-120">Die Adresse des Zeigers, der die ausgewählte Benutzeridentität empfängt.</span><span class="sxs-lookup"><span data-stu-id="46d2f-120">The address of the pointer that receives the chosen user identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46d2f-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46d2f-121">Return value</span></span>

<span data-ttu-id="46d2f-122">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="46d2f-122">Type: **HRESULT**</span></span>

<span data-ttu-id="46d2f-123">Das Ergebnis des Anmeldevorgangs.</span><span class="sxs-lookup"><span data-stu-id="46d2f-123">Result of the logon operation.</span></span> <span data-ttu-id="46d2f-124">Bei erfolgreicher Ausführung wird S OK zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="46d2f-124">If successful, it returns S\_OK.</span></span> <span data-ttu-id="46d2f-125">Andernfalls wird einer der folgenden Fehlercodes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="46d2f-125">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="46d2f-126">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="46d2f-126">Return code</span></span>                                                                                            | <span data-ttu-id="46d2f-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46d2f-127">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="46d2f-128"><dt>**E- \_ Benutzer \_ abgebrochen**</dt></span><span class="sxs-lookup"><span data-stu-id="46d2f-128"><dt>**E\_USER\_CANCELLED**</dt></span></span> </dl>      | <span data-ttu-id="46d2f-129">Der Benutzer hat den Anmeldevorgang von der Benutzeroberfläche abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="46d2f-129">The user canceled the logon operation from the UI.</span></span><br/>                               |
| <dl> <span data-ttu-id="46d2f-130"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="46d2f-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="46d2f-131">Die Benutzeridentität konnte nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="46d2f-131">The user identity could not be created.</span></span><br/>                                          |
| <dl> <span data-ttu-id="46d2f-132"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="46d2f-132"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="46d2f-133">Unerwarteter Vorgang.</span><span class="sxs-lookup"><span data-stu-id="46d2f-133">The operation failed unexpectedly.</span></span><br/>                                               |
| <dl> <span data-ttu-id="46d2f-134"><dt>**E- \_ Identitäten \_ deaktiviert**</dt></span><span class="sxs-lookup"><span data-stu-id="46d2f-134"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="46d2f-135">Die Identitätsverwaltung ist im System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="46d2f-135">Identity management is disabled on the system.</span></span><br/>                                   |
| <dl> <span data-ttu-id="46d2f-136"><dt>**S- \_ Identitäten \_ deaktiviert**</dt></span><span class="sxs-lookup"><span data-stu-id="46d2f-136"><dt>**S\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="46d2f-137">Die Identitätsverwaltung ist im System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="46d2f-137">Identity management is disabled on the system.</span></span><br/>                                   |
| <dl> <span data-ttu-id="46d2f-138"><dt>**E \_ Identität \_ ändern**</dt></span><span class="sxs-lookup"><span data-stu-id="46d2f-138"><dt>**E\_IDENTITY\_CHANGING**</dt></span></span> </dl>   | <span data-ttu-id="46d2f-139">Das System wechselt momentan zum Wechseln von Identitäten und kann den Vorgang nicht durchführen.</span><span class="sxs-lookup"><span data-stu-id="46d2f-139">The system is currently switching identities, and cannot complete the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="46d2f-140">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="46d2f-140">Requirements</span></span>



| <span data-ttu-id="46d2f-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46d2f-141">Requirement</span></span> | <span data-ttu-id="46d2f-142">Wert</span><span class="sxs-lookup"><span data-stu-id="46d2f-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46d2f-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46d2f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="46d2f-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46d2f-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="46d2f-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46d2f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="46d2f-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46d2f-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="46d2f-147">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="46d2f-147">End of client support</span></span><br/>    | <span data-ttu-id="46d2f-148">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="46d2f-148">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="46d2f-149">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="46d2f-149">End of server support</span></span><br/>    | <span data-ttu-id="46d2f-150">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="46d2f-150">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="46d2f-151">Header</span><span class="sxs-lookup"><span data-stu-id="46d2f-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="46d2f-152"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="46d2f-152"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="46d2f-153">IDL</span><span class="sxs-lookup"><span data-stu-id="46d2f-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46d2f-154"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="46d2f-154"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="46d2f-155">DLL</span><span class="sxs-lookup"><span data-stu-id="46d2f-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46d2f-156"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46d2f-156"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46d2f-157">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="46d2f-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46d2f-158">**Iuseridentitymanager**</span><span class="sxs-lookup"><span data-stu-id="46d2f-158">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="46d2f-159">**Iuseridentitymanager:: abmelden**</span><span class="sxs-lookup"><span data-stu-id="46d2f-159">**IUserIdentityManager::Logoff**</span></span>](iuseridentitymanager-logoff.md)
</dt> <dt>

[<span data-ttu-id="46d2f-160">**Iuseridentitymanager:: manageidentities**</span><span class="sxs-lookup"><span data-stu-id="46d2f-160">**IUserIdentityManager::ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




