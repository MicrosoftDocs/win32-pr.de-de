---
description: Eine Anwendungs definierte Funktion, die Rückruf-Zugriffs Steuerungs Einträge (ACEs) während einer Zugriffs Überprüfung behandelt.
ms.assetid: e8a510e6-0739-4765-ad07-3bcb1b9c905c
title: Authzaccesscheckcallback-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzAccessCheckCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 82e100092dd7c59e9cc689aa8723365fae8bed29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218836"
---
# <a name="authzaccesscheckcallback-callback-function"></a><span data-ttu-id="f4323-103">Authzaccesscheckcallback-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="f4323-103">AuthzAccessCheckCallback callback function</span></span>

<span data-ttu-id="f4323-104">Die **authzaccesscheckcallback** -Funktion ist eine Anwendungs definierte Funktion, die Rückruf- [*Zugriffs Steuerungs Einträge*](/windows/desktop/SecGloss/a-gly) (ACEs) während einer Zugriffs Überprüfung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f4323-104">The **AuthzAccessCheckCallback** function is an application-defined function that handles callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) during an access check.</span></span> <span data-ttu-id="f4323-105">**Authzaccesscheckcallback** ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="f4323-105">**AuthzAccessCheckCallback** is a placeholder for the application-defined function name.</span></span> <span data-ttu-id="f4323-106">Die Anwendung registriert diesen Rückruf durch Aufrufen von [**authzinitializeresourcemanager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).</span><span class="sxs-lookup"><span data-stu-id="f4323-106">The application registers this callback by calling [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).</span></span>

## <a name="syntax"></a><span data-ttu-id="f4323-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4323-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzAccessCheckCallback(
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PACE_HEADER                 pAce,
  _In_opt_ PVOID                       pArgs,
  _Inout_  PBOOL                       pbAceApplicable
);
```



## <a name="parameters"></a><span data-ttu-id="f4323-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4323-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4323-109">" *hauthzclientcontext* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="f4323-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4323-110">Ein Handle für einen Client Kontext.</span><span class="sxs-lookup"><span data-stu-id="f4323-110">A handle to a client context.</span></span>

</dd> <dt>

<span data-ttu-id="f4323-111">*Geschwindigkeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4323-111">*pAce* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4323-112">Ein Zeiger auf den ACE, der für die Aufnahme in den Rückruf der [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) -Funktion ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4323-112">A pointer to the ACE to evaluate for inclusion in the call to the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span>

</dd> <dt>

<span data-ttu-id="f4323-113"> Argumente \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f4323-113">*pArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f4323-114">Daten, die im *dynamicgrouparser* -Parameter des Aufrufes [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) oder [**authzcachedaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="f4323-114">Data passed in the *DynamicGroupArgs* parameter of the call to [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) or [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).</span></span>

</dd> <dt>

<span data-ttu-id="f4323-115">*pbaceanwendbar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f4323-115">*pbAceApplicable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4323-116">Ein Zeiger auf eine boolesche Variable, die die Ergebnisse der Auswertung der von der Anwendung definierten Logik empfängt.</span><span class="sxs-lookup"><span data-stu-id="f4323-116">A pointer to a Boolean variable that receives the results of the evaluation of the logic defined by the application.</span></span>

<span data-ttu-id="f4323-117">Die Ergebnisse sind **true** , wenn die Logik festlegt, dass der ACE anwendbar ist und in den [**callzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)-Befehl eingeschlossen wird. Andernfalls sind die Ergebnisse **false**.</span><span class="sxs-lookup"><span data-stu-id="f4323-117">The results are **TRUE** if the logic determines that the ACE is applicable and will be included in the call to [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); otherwise, the results are **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4323-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4323-118">Return value</span></span>

<span data-ttu-id="f4323-119">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="f4323-119">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="f4323-120">Wenn die Funktion die Auswertung nicht ausführen kann, wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f4323-120">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="f4323-121">Verwenden Sie [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) , um einen Fehler an die Access Check-Funktion zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="f4323-121">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4323-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4323-122">Remarks</span></span>

<span data-ttu-id="f4323-123">Sicherheits Attribut Variablen müssen im Client Kontext vorhanden sein, wenn Sie in einem bedingten Ausdruck referenziert werden. andernfalls wird der Ausdruck für den bedingten Ausdruck, der auf Sie verweist, zu "unknown" ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="f4323-123">Security attribute variables must be present in the client context if referred to in a conditional expression, otherwise the conditional expression term referencing them will evaluate to unknown.</span></span>

<span data-ttu-id="f4323-124">Weitere Informationen finden Sie unter [Funktionsweise von Access Check Works](how-dacls-control-access-to-an-object.md) und [zentralisierte Autorisierungs Richtlinien](centralized-authorization-policy.md) .</span><span class="sxs-lookup"><span data-stu-id="f4323-124">For more information, see the [How AccessCheck Works](how-dacls-control-access-to-an-object.md) and [Centralized Authorization Policy](centralized-authorization-policy.md) overviews.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4323-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4323-125">Requirements</span></span>



| <span data-ttu-id="f4323-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4323-126">Requirement</span></span> | <span data-ttu-id="f4323-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f4323-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="f4323-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4323-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f4323-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4323-129">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f4323-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4323-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f4323-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4323-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="f4323-132">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f4323-132">Redistributable</span></span><br/>          | <span data-ttu-id="f4323-133">Windows Server 2003-Verwaltungs Tools Pack unter Windows XP</span><span class="sxs-lookup"><span data-stu-id="f4323-133">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4323-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4323-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4323-135">Grundlegende Access Control Funktionen</span><span class="sxs-lookup"><span data-stu-id="f4323-135">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="f4323-136">Zentralisierte Autorisierungs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f4323-136">Centralized Authorization Policy</span></span>](centralized-authorization-policy.md)
</dt> <dt>

[<span data-ttu-id="f4323-137">Funktionsweise von Access Check</span><span class="sxs-lookup"><span data-stu-id="f4323-137">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="f4323-138">**Authzaccesscheck**</span><span class="sxs-lookup"><span data-stu-id="f4323-138">**AuthzAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> <dt>

[<span data-ttu-id="f4323-139">**Authzcachedaccesscheck**</span><span class="sxs-lookup"><span data-stu-id="f4323-139">**AuthzCachedAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[<span data-ttu-id="f4323-140">**Authzinitializeremoteresourcemanager**</span><span class="sxs-lookup"><span data-stu-id="f4323-140">**AuthzInitializeRemoteResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[<span data-ttu-id="f4323-141">**Authzinitializeresourcemanager**</span><span class="sxs-lookup"><span data-stu-id="f4323-141">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

