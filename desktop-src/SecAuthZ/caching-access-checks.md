---
description: Wenn eine Anwendung eine Zugriffs Überprüfung durch Aufrufen der authzaccesscheck-Funktion durchführt, können die Ergebnisse dieser Zugriffs Überprüfung zwischengespeichert werden.
ms.assetid: d79a5683-6c67-487f-b9a6-4e80da38b827
title: Caching-Zugriffs Überprüfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 967e0a5398d93c1715d7d08e5c7c75695e4120ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350588"
---
# <a name="caching-access-checks"></a><span data-ttu-id="648e4-103">Caching-Zugriffs Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="648e4-103">Caching Access Checks</span></span>

<span data-ttu-id="648e4-104">Wenn eine Anwendung eine Zugriffs Überprüfung durch Aufrufen der [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) -Funktion durchführt, können die Ergebnisse dieser Zugriffs Überprüfung zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="648e4-104">When an application performs an access check by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function, the results of that access check can be cached.</span></span> <span data-ttu-id="648e4-105">Wenn der *pauthzhandle* -Parameter der [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) -Funktion nicht **null** ist, führt die Funktion eine separate Zugriffs Überprüfung durch, wobei die angeforderte [**Zugriffs \_ Maske**](access-mask.md) den **maximal \_ zulässigen** Wert hat, und speichert die Ergebnisse dieser Überprüfung zwischen.</span><span class="sxs-lookup"><span data-stu-id="648e4-105">When the *pAuthzHandle* parameter of the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function is not **NULL**, the function performs a separate access check, with a requested [**ACCESS\_MASK**](access-mask.md) of **MAXIMUM\_ALLOWED**, and caches the results of that check.</span></span> <span data-ttu-id="648e4-106">Ein Handle für die Ergebnisse dieser Überprüfung kann dann als *authzhandle* -Parameter an die [**authzcachedaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) -Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="648e4-106">A handle to the results of that check can then be passed as the *AuthzHandle* parameter to the [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) function.</span></span> <span data-ttu-id="648e4-107">Dies ermöglicht eine schnellere Zugriffs Überprüfung für einen bestimmten Client und [*Sicherheits Deskriptoren*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="648e4-107">This allows faster access checking for a given client and [*security descriptors*](/windows/desktop/SecGloss/s-gly).</span></span>

<span data-ttu-id="648e4-108">Nur der statische Teil einer Zugriffs Überprüfung kann zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="648e4-108">Only the static portion of an access check can be cached.</span></span> <span data-ttu-id="648e4-109">Alle Rückruf- [*Zugriffs Steuerungs Einträge*](/windows/desktop/SecGloss/a-gly) (ACEs) oder ACEs, die die **Prinzipal- \_ Self** -sid enthalten, müssen für jede Zugriffs Überprüfung ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="648e4-109">Any callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) or ACEs that contain the **PRINCIPAL\_SELF** SID must be evaluated for each access check.</span></span>

<span data-ttu-id="648e4-110">Attribut Variablen müssen in Form eines Ausdrucks vorliegen, wenn Sie mit logischen Operatoren verwendet werden. Andernfalls werden Sie als UNKNOWN ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="648e4-110">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="example"></a><span data-ttu-id="648e4-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="648e4-111">Example</span></span>

<span data-ttu-id="648e4-112">Im folgenden Beispiel wird der Zugriff auf ein zwischengespeichertes Ergebnis einer vorherigen Zugriffs Überprüfung überprüft.</span><span class="sxs-lookup"><span data-stu-id="648e4-112">The following example checks access against a cached result from a previous access check.</span></span> <span data-ttu-id="648e4-113">Die vorherige Zugriffs Überprüfung wurde im Beispiel für das [Überprüfen des Zugriffs mit der Authz-API](checking-access-with-authz-api.md)durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="648e4-113">The previous access check was performed in the example in [Checking Access with Authz API](checking-access-with-authz-api.md).</span></span>


```C++
BOOL CheckCachedAccess(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{
    #define MY_MAX 4096


    PSECURITY_DESCRIPTOR                pSecurityDescriptor = NULL;
    ULONG                                cbSecurityDescriptorSize = 0;
    AUTHZ_ACCESS_REQUEST                Request;
    CHAR                                ReplyBuffer[MY_MAX];
    CHAR                                CachedReplyBuffer[MY_MAX];
    PAUTHZ_ACCESS_REPLY                    pReply = (PAUTHZ_ACCESS_REPLY)ReplyBuffer;
    PAUTHZ_ACCESS_REPLY                    pCachedReply = (PAUTHZ_ACCESS_REPLY)CachedReplyBuffer;
    DWORD                                AuthzError =0;
    AUTHZ_ACCESS_CHECK_RESULTS_HANDLE    hCached;

    //Allocate memory for the access request structure.
    RtlZeroMemory(&Request, sizeof(AUTHZ_ACCESS_REQUEST));

    //Set up the access request structure.
    Request.DesiredAccess = READ_CONTROL;
    
    //Allocate memory for the initial access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the access reply structure.
    pReply->ResultListLength = 1;
    pReply->Error = (PDWORD) ((PCHAR) pReply + sizeof(AUTHZ_ACCESS_REPLY));
    pReply->GrantedAccessMask = (PACCESS_MASK) (pReply->Error + pReply->ResultListLength);
    pReply->SaclEvaluationResults = NULL;

    //Allocate memory for the cached access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the cached access reply structure.
    pCachedReply->ResultListLength = 1;
    pCachedReply->Error = (PDWORD) ((PCHAR) pCachedReply + sizeof(AUTHZ_ACCESS_REPLY));
    pCachedReply->GrantedAccessMask = (PACCESS_MASK) (pCachedReply->Error + pCachedReply->ResultListLength);
    pCachedReply->SaclEvaluationResults = NULL;

    //Create security descriptor.
    if(!ConvertStringSecurityDescriptorToSecurityDescriptor(
        L"O:LAG:BAD:(A;;RC;;;BA)",
        SDDL_REVISION_1,
        &pSecurityDescriptor,
        NULL))
    {
        printf_s("ConvertStringSecurityDescriptorToSecurityDescriptor failed with %d\n", GetLastError()); 
        return FALSE;
    }

    //Call AuthzAccessCheck and cache results.
    if(!AuthzAccessCheck(
        0,
        hClientContext,
        &Request,
        NULL,
        pSecurityDescriptor,
        NULL,
        0,
        pReply,
        &hCached))
    {
        printf_s("AuthzAccessCheck failed with %d\n", GetLastError());
        
    LocalFree(pSecurityDescriptor);
        
        return FALSE;
    }

    //Call AuthzCachedAccessCheck with the cached result from the previous call.
    if(!AuthzCachedAccessCheck(
        0,
        hCached,
        &Request,
        NULL,
        pCachedReply))
    {
        printf_s("AuthzCachedAccessCheck failed with %d\n", GetLastError());
        
        LocalFree(pSecurityDescriptor);
    AuthzFreeHandle(hCached);
    
        return FALSE;
    }

    //Print results.
    if(*pCachedReply->GrantedAccessMask & READ_CONTROL)
    {
        printf_s("Access granted.\n");
    }
    else
    {
        printf_s("Access denied.\n");
    }


  LocalFree(pSecurityDescriptor);
  AuthzFreeHandle(hCached);
    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="648e4-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="648e4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="648e4-115">Hinzufügen von SIDs zu einem Client Kontext</span><span class="sxs-lookup"><span data-stu-id="648e4-115">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="648e4-116">Überprüfen des Zugriffs mit der Authz-API</span><span class="sxs-lookup"><span data-stu-id="648e4-116">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="648e4-117">Initialisieren eines Client Kontexts</span><span class="sxs-lookup"><span data-stu-id="648e4-117">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="648e4-118">Abfragen eines Client Kontexts</span><span class="sxs-lookup"><span data-stu-id="648e4-118">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
