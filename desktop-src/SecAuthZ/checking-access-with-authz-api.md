---
description: Anwendungen bestimmen, ob der Zugriff auf Sicherungs fähige Objekte durch Aufrufen der authzaccesscheck-Funktion gewährt werden soll.
ms.assetid: dad0a102-08ed-4cd2-bef5-87bc48fc7fc2
title: Überprüfen des Zugriffs mit der Authz-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e129b690a7c1f701b5f669a8f0705c5a5e9a2eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862851"
---
# <a name="checking-access-with-authz-api"></a><span data-ttu-id="26d69-103">Überprüfen des Zugriffs mit der Authz-API</span><span class="sxs-lookup"><span data-stu-id="26d69-103">Checking Access with Authz API</span></span>

<span data-ttu-id="26d69-104">Anwendungen bestimmen, ob der Zugriff auf Sicherungs fähige Objekte durch Aufrufen der [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) -Funktion gewährt werden soll.</span><span class="sxs-lookup"><span data-stu-id="26d69-104">Applications determine whether to grant access to securable objects by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span>

<span data-ttu-id="26d69-105">Die [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) -Funktion nimmt sowohl [**Authz- \_ zugriffsanforderungs \_**](/windows/desktop/api/Authz/ns-authz-authz_access_request) -als auch [**Sicherheits \_ deskriptorstrukturen**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) als Parameter an.</span><span class="sxs-lookup"><span data-stu-id="26d69-105">The [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function takes both [**AUTHZ\_ACCESS\_REQUEST**](/windows/desktop/api/Authz/ns-authz-authz_access_request) and [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) structures as parameters.</span></span> <span data-ttu-id="26d69-106">Die **Authz- \_ Zugriffs \_ Anforderungs** Struktur gibt eine angeforderte Zugriffsebene an.</span><span class="sxs-lookup"><span data-stu-id="26d69-106">The **AUTHZ\_ACCESS\_REQUEST** structure specifies a level of access requested.</span></span> <span data-ttu-id="26d69-107">Die **authzaccesscheck** -Funktion wertet den angeforderten Zugriff anhand der angegebenen **Sicherheits \_ Beschreibung** für einen angegebenen Client Kontext aus.</span><span class="sxs-lookup"><span data-stu-id="26d69-107">The **AuthzAccessCheck** function evaluates the requested access against the specified **SECURITY\_DESCRIPTOR** for a specified client context.</span></span> <span data-ttu-id="26d69-108">Informationen dazu, wie ein Sicherheits Deskriptor den Zugriff auf ein Objekt steuert, finden Sie unter [Steuern des Zugriffs auf ein Objekt durch DACLs](how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="26d69-108">For information about how a security descriptor controls access to an object, see [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="26d69-109">Attribut Variablen müssen in Form eines Ausdrucks vorliegen, wenn Sie mit logischen Operatoren verwendet werden. Andernfalls werden Sie als UNKNOWN ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="26d69-109">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="callback-function"></a><span data-ttu-id="26d69-110">Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="26d69-110">Callback Function</span></span>

<span data-ttu-id="26d69-111">Wenn die [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) der [**Sicherheits \_ Beschreibung**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) des zu überprüfenden Objekts alle Rückruf [*Zugriffs Steuerungs Einträge*](/windows/desktop/SecGloss/a-gly) (ACEs) enthält, ruft [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) die [**authzaccesscheckcallback**](authzaccesscheckcallback.md) -Funktion für jeden Rückruf-ACE auf, der in der DACL enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="26d69-111">If the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) of the object to be checked contains any callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) calls the [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) function for each callback ACE contained in the DACL.</span></span> <span data-ttu-id="26d69-112">Ein Rückruf-ACE ist eine beliebige ACE-Struktur, deren ACE-Typ das Wort "Callback" enthält.</span><span class="sxs-lookup"><span data-stu-id="26d69-112">A callback ACE is any ACE structure whose ACE type contains the word "callback."</span></span> <span data-ttu-id="26d69-113">Die **authzaccesscheckcallback** -Funktion ist eine Anwendungs definierte Funktion, die registriert werden muss, wenn der Ressourcen-Manager durch Aufrufen der [**authzinitializeresourcemanager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) -Funktion initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="26d69-113">The **AuthzAccessCheckCallback** function is an application-defined function that must be registered when the resource manager is initialized by calling the [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) function.</span></span>

<span data-ttu-id="26d69-114">Eine Rückruffunktion ermöglicht es einer Anwendung, Geschäftslogik zu definieren, die zur Laufzeit ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="26d69-114">A callback function allows an application to define business logic to be evaluated at runtime.</span></span> <span data-ttu-id="26d69-115">Wenn die [**authzaccesscheckcallback**](authzaccesscheckcallback.md) -Funktion aufgerufen wird, wird der Rückruf-ACE, der den Aufruf ausgelöst hat, zur Auswertung an die Rückruffunktion übermittelt.</span><span class="sxs-lookup"><span data-stu-id="26d69-115">When the [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) function is called, the callback ACE that caused the call is passed to the callback function for evaluation.</span></span> <span data-ttu-id="26d69-116">Wenn die von der Anwendung definierte Logik als **true** ausgewertet wird, ist der Rückruf-ACE in der Zugriffs Überprüfung enthalten.</span><span class="sxs-lookup"><span data-stu-id="26d69-116">If the application-defined logic evaluates as **TRUE**, then the callback ACE is included in the access check.</span></span> <span data-ttu-id="26d69-117">Andernfalls wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="26d69-117">Otherwise, it is ignored.</span></span>

## <a name="caching-access-results"></a><span data-ttu-id="26d69-118">Caching-Zugriffs Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="26d69-118">Caching Access Results</span></span>

<span data-ttu-id="26d69-119">Die Ergebnisse einer Zugriffs Überprüfung können zwischengespeichert und in zukünftigen Aufrufen der [**authzcachedaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) -Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26d69-119">The results of an access check can be cached and used in future calls to the [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) function.</span></span> <span data-ttu-id="26d69-120">Weitere Informationen zum Zwischenspeichern von Zugriffs Überprüfungen, einschließlich eines Beispiels, finden Sie unter [Caching Access Checks](caching-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="26d69-120">For more information about caching access checks, including an example, see [Caching Access Checks](caching-access-checks.md).</span></span>

## <a name="example"></a><span data-ttu-id="26d69-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="26d69-121">Example</span></span>

<span data-ttu-id="26d69-122">Im folgenden Beispiel wird eine [**Sicherheits \_ Beschreibung**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) erstellt, die **Lese \_** Zugriff auf integrierte Administratoren ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="26d69-122">The following example creates a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) that allows **READ\_CONTROL** access to built-in administrators.</span></span> <span data-ttu-id="26d69-123">Diese Sicherheits Beschreibung wird verwendet, um den Zugriff für den Client zu überprüfen, der durch den Client Kontext angegeben wird, der im Beispiel unter [Initialisieren eines Client Kontexts](initializing-a-client-context.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="26d69-123">It uses that security descriptor to check access for the client specified by the client context created in the example in [Initializing a Client Context](initializing-a-client-context.md).</span></span>


```C++
BOOL CheckAccess(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{
    #define MY_MAX 4096


    PSECURITY_DESCRIPTOR    pSecurityDescriptor = NULL;
    ULONG                    cbSecurityDescriptorSize = 0;
    AUTHZ_ACCESS_REQUEST    Request;
    CHAR                    ReplyBuffer[MY_MAX];
    PAUTHZ_ACCESS_REPLY        pReply = (PAUTHZ_ACCESS_REPLY)ReplyBuffer;
    DWORD                    AuthzError =0;

    //Allocate memory for the access request structure.
    RtlZeroMemory(&Request, sizeof(AUTHZ_ACCESS_REQUEST));

    //Set up the access request structure.
    Request.DesiredAccess = READ_CONTROL;
    
    //Allocate memory for the access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the access reply structure.
    pReply->ResultListLength = 1;
    pReply->Error = (PDWORD) ((PCHAR) pReply + sizeof(AUTHZ_ACCESS_REPLY));
    pReply->GrantedAccessMask = (PACCESS_MASK) (pReply->Error + pReply->ResultListLength);
    pReply->SaclEvaluationResults = NULL;

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

    //Call AuthzAccessCheck.
    if(!AuthzAccessCheck(
        0,
        hClientContext,
        &Request,
        NULL,
        pSecurityDescriptor,
        NULL,
        0,
        pReply,
        NULL))
    {
        printf_s("AuthzAccessCheck failed with %d\n", GetLastError());
        
    LocalFree(pSecurityDescriptor);
    
        return FALSE;
    }


    //Print results.
    if(*pReply->GrantedAccessMask & READ_CONTROL)
    {
        printf_s("Access granted.\n");
    }
    else
    {
        printf_s("Access denied.\n");
    }

  LocalFree(pSecurityDescriptor);
    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="26d69-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26d69-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26d69-125">Hinzufügen von SIDs zu einem Client Kontext</span><span class="sxs-lookup"><span data-stu-id="26d69-125">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="26d69-126">Caching-Zugriffs Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="26d69-126">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="26d69-127">Initialisieren eines Client Kontexts</span><span class="sxs-lookup"><span data-stu-id="26d69-127">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="26d69-128">Abfragen eines Client Kontexts</span><span class="sxs-lookup"><span data-stu-id="26d69-128">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
