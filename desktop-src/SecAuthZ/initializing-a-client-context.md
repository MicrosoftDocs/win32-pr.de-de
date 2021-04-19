---
description: Eine Anwendung muss einen Client Kontext erstellen, bevor Sie mit der Authz-API Zugriffs Überprüfungen oder-Überwachungen durchführen kann.
ms.assetid: 82f207ff-cac4-4e9a-a9e6-ddb3f6c8b30a
title: Initialisieren eines Client Kontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be229a60a12e33ab0c2bbd3e52fc533cf29ed1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355344"
---
# <a name="initializing-a-client-context"></a><span data-ttu-id="cbae0-103">Initialisieren eines Client Kontexts</span><span class="sxs-lookup"><span data-stu-id="cbae0-103">Initializing a Client Context</span></span>

<span data-ttu-id="cbae0-104">Eine Anwendung muss einen Client Kontext erstellen, bevor Sie mit der Authz-API Zugriffs Überprüfungen oder-Überwachungen durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="cbae0-104">An application must create a client context before it can use Authz API to perform access checks or auditing.</span></span>

<span data-ttu-id="cbae0-105">Eine Anwendung muss die [**authzinitializeresourcemanager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) -Funktion zum Initialisieren des Ressourcen-Managers aufruft.</span><span class="sxs-lookup"><span data-stu-id="cbae0-105">An application must call the [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) function to initialize the resource manager.</span></span> <span data-ttu-id="cbae0-106">Die Anwendung kann dann eine von mehreren Funktionen aufzurufen, um einen Client Kontext zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cbae0-106">The application can then call one of several functions to create a client context.</span></span> <span data-ttu-id="cbae0-107">Wenn Sie Zugriffs Überprüfungen oder die Überwachung Remote ausführen, müssen Sie außerdem die [**authzinitializeremoteresourcemanager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="cbae0-107">Additionally, if you are performing access checks or auditing remotely, you must use the [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) function.</span></span>

<span data-ttu-id="cbae0-108">Um einen Client Kontext zu erstellen, der auf einem vorhandenen Client Kontext basiert, rufen Sie die [**authzinitializecontextfromauthzcontext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="cbae0-108">To create a client context based on an existing client context, call the [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) function.</span></span>

<span data-ttu-id="cbae0-109">Die [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) -Funktion erstellt mithilfe der Informationen in einem Anmelde Token einen neuen Client Kontext.</span><span class="sxs-lookup"><span data-stu-id="cbae0-109">The [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function creates a new client context by using information in a logon token.</span></span> <span data-ttu-id="cbae0-110">Die [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) -Funktion erstellt mithilfe der angegebenen [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid)einen neuen Client Kontext.</span><span class="sxs-lookup"><span data-stu-id="cbae0-110">The [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) function creates a new client context by using the specified [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid).</span></span>

<span data-ttu-id="cbae0-111">Wenn möglich, wird anstelle von [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)die [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="cbae0-111">If possible, call the [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function instead of [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid).</span></span> <span data-ttu-id="cbae0-112">**AuthzInitializeContextFromSid** versucht, die in einem Anmelde Token verfügbaren Informationen abzurufen, wenn der Client tatsächlich angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="cbae0-112">**AuthzInitializeContextFromSid** attempts to retrieve the information available in a logon token had the client actually logged on.</span></span> <span data-ttu-id="cbae0-113">Ein tatsächliches Anmelde Token bietet weitere Informationen, wie z. b. den Anmeldetyp und die Anmelde Eigenschaften, und gibt das Verhalten des Authentifizierungs Pakets an, das für die Anmeldung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cbae0-113">An actual logon token provides more information, such as logon type and logon properties, and reflects the behavior of the authentication package used for the logon.</span></span> <span data-ttu-id="cbae0-114">Der von **AuthzInitializeContextFromToken** erstellte Client Kontext verwendet ein Anmelde Token, und der resultierende Client Kontext ist ausführender und präziser als ein von **AuthzInitializeContextFromSid** erstellter Client Kontext.</span><span class="sxs-lookup"><span data-stu-id="cbae0-114">The client context created by **AuthzInitializeContextFromToken** uses a logon token, and the resulting client context is more complete and accurate than a client context created by **AuthzInitializeContextFromSid**.</span></span>

> [!Note]  
> <span data-ttu-id="cbae0-115">Sicherheits Attribut Variablen müssen im Client Kontext vorhanden sein, wenn in einem bedingten Ausdruck darauf verwiesen wird. Andernfalls wird der Ausdruck für den bedingten Ausdruck, der auf ihn verweist, als unbekannt ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="cbae0-115">Security attribute variables must be present in the client context if referred to in a conditional expression; otherwise, the conditional expression term referencing them will be evaluated as unknown.</span></span> <span data-ttu-id="cbae0-116">Weitere Informationen zu bedingten Ausdrücken finden Sie im Thema [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) .</span><span class="sxs-lookup"><span data-stu-id="cbae0-116">For more information on conditional expressions, see the [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) topic.</span></span>

 

## <a name="example"></a><span data-ttu-id="cbae0-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cbae0-117">Example</span></span>

<span data-ttu-id="cbae0-118">Im folgenden Beispiel wird der Authz-Ressourcen-Manager initialisiert und die [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) -Funktion aufgerufen, um einen Client Kontext aus dem Anmelde Token zu erstellen, das dem aktuellen Prozess zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cbae0-118">The following example initializes the Authz resource manager and calls the [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function to create a client context from the logon token associated with the current process.</span></span>


```C++
BOOL AuthzInitFromToken(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{

    HANDLE                            hToken = NULL;
    LUID                            Luid = {0, 0};

    
    ULONG                            uFlags = 0;


    //Initialize Resource Manager
    if(!AuthzInitializeResourceManager(
        AUTHZ_RM_FLAG_NO_AUDIT,
        NULL,
        NULL,
        NULL,
        L"My Resource Manager",
        &g_hResourceManager
        ))
    {
        printf_s("AuthzInitializeResourceManager failed with %d\n", GetLastError);
        return FALSE;
    }
    

    //Get the current token.

    if(!OpenProcessToken(GetCurrentProcess(), TOKEN_ALL_ACCESS, &hToken))
    {
        printf_s("OpenProcessToken failed with %d\n", GetLastError);
        return FALSE;
    }


    //Initialize the client context

    if(!AuthzInitializeContextFromToken(
        0,
        hToken,
        g_hResourceManager,
        NULL,
        Luid,
        NULL,
        phClientContext
        ))
    {    
        printf_s("AuthzInitializeContextFromToken failed with %d\n", GetLastError);
        return FALSE;
    }

    
    printf_s("Initialized client context. \n");
    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="cbae0-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cbae0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbae0-120">Hinzufügen von SIDs zu einem Client Kontext</span><span class="sxs-lookup"><span data-stu-id="cbae0-120">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="cbae0-121">Caching-Zugriffs Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="cbae0-121">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="cbae0-122">Überprüfen des Zugriffs mit der Authz-API</span><span class="sxs-lookup"><span data-stu-id="cbae0-122">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="cbae0-123">Funktionsweise von Access Check</span><span class="sxs-lookup"><span data-stu-id="cbae0-123">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="cbae0-124">Abfragen eines Client Kontexts</span><span class="sxs-lookup"><span data-stu-id="cbae0-124">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="cbae0-125">Sicherheits Deskriptor-Definitions Sprache für bedingte ACEs</span><span class="sxs-lookup"><span data-stu-id="cbae0-125">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[<span data-ttu-id="cbae0-126">**Authzinitializeremoteresourcemanager**</span><span class="sxs-lookup"><span data-stu-id="cbae0-126">**AuthzInitializeRemoteResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[<span data-ttu-id="cbae0-127">**Authzinitializeresourcemanager**</span><span class="sxs-lookup"><span data-stu-id="cbae0-127">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



