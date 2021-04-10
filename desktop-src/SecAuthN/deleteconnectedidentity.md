---
description: Löscht die Benutzer Anmelde Informationen, die für die verbundene Identität verwendet werden.
ms.assetid: EB32832D-9A8C-4CEB-897A-7E9D24FF84DD
title: Deleteconnectedidentity-Funktion (indentitystore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteConnectedIdentity
api_type:
- HeaderDef
api_location:
- Indentitystore.h
ms.openlocfilehash: 8079985f916e996a56b4203ad6ad065c1b7664e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041610"
---
# <a name="deleteconnectedidentity-function"></a><span data-ttu-id="e9cdd-103">Deleteconnectedidentity-Funktion</span><span class="sxs-lookup"><span data-stu-id="e9cdd-103">DeleteConnectedIdentity function</span></span>

<span data-ttu-id="e9cdd-104">Löscht die Benutzer Anmelde Informationen, die für die verbundene Identität verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-104">Deletes the user credential used for the connected identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9cdd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9cdd-105">Syntax</span></span>


```C++
SEC_ENTRY DeleteConnectedIdentity(
  _In_     PVOID  ProviderHandle,
  _In_opt_ HANDLE UserToken,
  _In_     PSID   UserSid,
  _In_     PWSTR  IdentityUserName
);
```



## <a name="parameters"></a><span data-ttu-id="e9cdd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9cdd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9cdd-107">*ProviderHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9cdd-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9cdd-108">Handle des Identitäts Anbieters.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-108">Identity provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="e9cdd-109">*UserToken* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e9cdd-109">*UserToken* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9cdd-110">Token des verbundenen Benutzers, dessen Konto in ein lokales Konto konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-110">Token of the connected user whose account is going to be converted to a local account.</span></span> <span data-ttu-id="e9cdd-111">Wenn *userToken* nicht **null** ist, verwendet der Identitäts Anbieter dieses Token, um das Benutzerprofil zu laden und verbundene Zustände zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-111">If *UserToken* is not **NULL**, the identity provider uses this token to load the user profile and clean up connected states.</span></span> <span data-ttu-id="e9cdd-112">Wenn *userToken* auf **null** festgelegt ist, erzwingt LSA die Trennung der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-112">If *UserToken* is **NULL**, LSA is forcing the disconnection.</span></span> <span data-ttu-id="e9cdd-113">Der Identitäts Anbieter sollte alle globalen verbundenen Zustände für diesen Benutzer bereinigen, aber der Anbieter muss keine verbundenen Zustände im Benutzerprofil bereinigen.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-113">The identity provider should clean up any global connected states on this user, but the provider does not have to clean up connected states in the user profile.</span></span>

</dd> <dt>

<span data-ttu-id="e9cdd-114">*UserSID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9cdd-114">*UserSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9cdd-115">Die primäre SID des verbundenen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-115">The primary SID of the connected user.</span></span> <span data-ttu-id="e9cdd-116">Wenn *userToken* nicht **null** ist, ist dieser Parameter die Benutzer-SID des Tokens.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-116">If *UserToken* is not **NULL**, this parameter is the user SID of the token.</span></span> <span data-ttu-id="e9cdd-117">Wenn *userToken* **null** ist, wird dieser Parameter zum Identifizieren des verbundenen Benutzers und zum Bereinigen der Global verbundenen Zustände dieses Benutzers verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-117">If *UserToken* is **NULL**, this parameter is used to identify the connected user and clean up global connected states of that user.</span></span>

</dd> <dt>

<span data-ttu-id="e9cdd-118">*Identityusername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9cdd-118">*IdentityUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9cdd-119">Der Benutzername der Identität.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-119">The user name of the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9cdd-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9cdd-120">Return value</span></span>

<span data-ttu-id="e9cdd-121">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion sec \_ E \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-121">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="e9cdd-122">Wenn die Funktion fehlschlägt, gibt die Funktion möglicherweise einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-122">If the function fails, the function may return one of the following error codes.</span></span>



| <span data-ttu-id="e9cdd-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9cdd-123">Return value</span></span>                                                                                               | <span data-ttu-id="e9cdd-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9cdd-124">Description</span></span>                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e9cdd-125"><dt>\_ungültiger \_ Parameter.</dt></span><span class="sxs-lookup"><span data-stu-id="e9cdd-125"><dt>STATUS\_INVALID\_PARAMETER</dt></span></span> </dl>      | <span data-ttu-id="e9cdd-126">Ein Parameter ist nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-126">A parameter is not valid.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="e9cdd-127"><dt>Status " \_ kein \_ solcher \_ Benutzer"</dt></span><span class="sxs-lookup"><span data-stu-id="e9cdd-127"><dt>STATUS\_NO\_SUCH\_USER</dt></span></span> </dl>          | <span data-ttu-id="e9cdd-128">Der von *UserSID* identifizierte Benutzer ist nicht vorhanden, ist zurzeit nicht verbunden, oder es ist keine Identität vorhanden, deren Benutzername mit *identityusername* übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-128">The user identified by *UserSid* does not exist, is not currently connected, or there is no identity whose user name matches *IdentityUserName*.</span></span><br/> |
| <dl> <span data-ttu-id="e9cdd-129"><dt>\_nicht genügend \_ Ressourcen.</dt></span><span class="sxs-lookup"><span data-stu-id="e9cdd-129"><dt>STATUS\_INSUFFICIENT\_RESOURCES</dt></span></span> </dl> | <span data-ttu-id="e9cdd-130">Es ist nicht genügend Arbeitsspeicher vorhanden, um die Anforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-130">There is not enough memory to process the request.</span></span><br/>                                                                                               |



 

## <a name="requirements"></a><span data-ttu-id="e9cdd-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9cdd-131">Requirements</span></span>



| <span data-ttu-id="e9cdd-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9cdd-132">Requirement</span></span> | <span data-ttu-id="e9cdd-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e9cdd-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9cdd-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9cdd-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e9cdd-135">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9cdd-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="e9cdd-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9cdd-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e9cdd-137">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9cdd-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9cdd-138">Header</span><span class="sxs-lookup"><span data-stu-id="e9cdd-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9cdd-139"><dt>Indentitystore. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9cdd-139"><dt>Indentitystore.h</dt></span></span> </dl> |



 

 




