---
description: Die authzgetcentralaccesspolicycallback-Funktion ist eine Anwendungs definierte Funktion, die die zentrale Zugriffs Richtlinie abruft. Authzgetcentralaccesspolicycallback ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.
ms.assetid: 1D5831EF-ACA8-4EE9-A7C1-E1A3CB74CEC0
title: Authzgetcentralaccesspolicycallback-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzGetCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b96832fa647fde920a70ac3d6608c8ebb0048892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353225"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a><span data-ttu-id="16542-104">Authzgetcentralaccesspolicycallback-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="16542-104">AuthzGetCentralAccessPolicyCallback callback function</span></span>

<span data-ttu-id="16542-105">Die *authzgetcentralaccesspolicycallback* -Funktion ist eine Anwendungs definierte Funktion, die die zentrale Zugriffs Richtlinie abruft.</span><span class="sxs-lookup"><span data-stu-id="16542-105">The *AuthzGetCentralAccessPolicyCallback* function is an application-defined function that retrieves the central access policy.</span></span> <span data-ttu-id="16542-106">*Authzgetcentralaccesspolicycallback* ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="16542-106">*AuthzGetCentralAccessPolicyCallback* is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="16542-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="16542-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzGetCentralAccessPolicyCallback (
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PSID                        capid,
  _In_opt_ PVOID                       pArgs,
  _Out_    PBOOL                       pCentralAccessPolicyApplicable,
  _Out_    PVOID                       ppCentralAccessPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="16542-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="16542-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16542-109">" *hauthzclientcontext* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="16542-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16542-110">Handle für den Client Kontext.</span><span class="sxs-lookup"><span data-stu-id="16542-110">Handle to the client context.</span></span>

</dd> <dt>

<span data-ttu-id="16542-111">*capid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16542-111">*capid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16542-112">Die ID der abzurufenden zentralen Zugriffs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="16542-112">ID of the central access policy to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="16542-113"> Argumente \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="16542-113">*pArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="16542-114">Optionale Argumente, die über den **optionalarguments** -Member der [**Authz- \_ Zugriffs \_ Anforderungs**](/windows/desktop/api/Authz/ns-authz-authz_access_request) Struktur an die [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) -Funktion übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="16542-114">Optional arguments that were passed to the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function through the **OptionalArguments** member of the [**AUTHZ\_ACCESS\_REQUEST**](/windows/desktop/api/Authz/ns-authz-authz_access_request) structure.</span></span>

</dd> <dt>

<span data-ttu-id="16542-115">*pcentralaccesspolicyanwendbar* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="16542-115">*pCentralAccessPolicyApplicable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16542-116">Ein Zeiger auf einen booleschen Wert, den der Ressourcen-Manager verwendet, um anzugeben, ob während der Zugriffs Auswertung eine zentrale Zugriffs Richtlinie verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16542-116">Pointer to a Boolean value that the resource manager uses to indicate whether a central access policy should be used during access evaluation.</span></span>

</dd> <dt>

<span data-ttu-id="16542-117">*ppcentralaccesspolicy* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="16542-117">*ppCentralAccessPolicy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16542-118">Ein Zeiger auf die zentrale Zugriffs Richtlinie (Cap), die zum Auswerten des Zugriffs verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16542-118">Pointer to the central access policy (CAP) to be used for evaluating access.</span></span> <span data-ttu-id="16542-119">Wenn dieser Wert **null** ist, wird die Standardgrenze angewendet.</span><span class="sxs-lookup"><span data-stu-id="16542-119">If this value is **NULL**, the default CAP is applied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16542-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16542-120">Return value</span></span>

<span data-ttu-id="16542-121">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="16542-121">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="16542-122">Wenn die Funktion die Auswertung nicht ausführen kann, wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="16542-122">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="16542-123">Verwenden Sie [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) , um einen Fehler an die Access Check-Funktion zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="16542-123">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="requirements"></a><span data-ttu-id="16542-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16542-124">Requirements</span></span>



| <span data-ttu-id="16542-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16542-125">Requirement</span></span> | <span data-ttu-id="16542-126">Wert</span><span class="sxs-lookup"><span data-stu-id="16542-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="16542-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16542-127">Minimum supported client</span></span><br/> | <span data-ttu-id="16542-128">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16542-128">Windows 8 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="16542-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16542-129">Minimum supported server</span></span><br/> | <span data-ttu-id="16542-130">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16542-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="16542-131">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="16542-131">Redistributable</span></span><br/>          | <span data-ttu-id="16542-132">Windows Server 2003-Verwaltungs Tools Pack unter Windows XP</span><span class="sxs-lookup"><span data-stu-id="16542-132">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="16542-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16542-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16542-134">**Authz- \_ Zugriffs \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="16542-134">**AUTHZ\_ACCESS\_REQUEST**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[<span data-ttu-id="16542-135">**Authz- \_ Init- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="16542-135">**AUTHZ\_INIT\_INFO**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[<span data-ttu-id="16542-136">**Authzaccesscheck**</span><span class="sxs-lookup"><span data-stu-id="16542-136">**AuthzAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

