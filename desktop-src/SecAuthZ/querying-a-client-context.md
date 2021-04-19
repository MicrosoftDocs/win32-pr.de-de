---
description: Anwendungen können die AuthZGetInformationFromContext-Funktion aufrufen, um Informationen über einen vorhandenen Client Kontext abzufragen.
ms.assetid: 32655e54-499e-439e-8d4f-f2b4eaa0b184
title: Abfragen eines Client Kontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101c35466e675d9ecba942089bbe7b5e82cffd90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359893"
---
# <a name="querying-a-client-context"></a><span data-ttu-id="ef3cc-103">Abfragen eines Client Kontexts</span><span class="sxs-lookup"><span data-stu-id="ef3cc-103">Querying a Client Context</span></span>

<span data-ttu-id="ef3cc-104">Anwendungen können die [**AuthZGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) -Funktion aufrufen, um Informationen über einen vorhandenen Client Kontext abzufragen.</span><span class="sxs-lookup"><span data-stu-id="ef3cc-104">Applications can call the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function to query information about an existing client context.</span></span>

<span data-ttu-id="ef3cc-105">Der *infoclass* -Parameter der [**AuthZGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) -Funktion nimmt einen Wert aus der [**Authz- \_ Kontext \_ Informations \_ Klassen**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) -Enumeration an, der angibt, welche Art von Informationen die Funktion abfragt.</span><span class="sxs-lookup"><span data-stu-id="ef3cc-105">The *InfoClass* parameter of the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function takes a value from the [**AUTHZ\_CONTEXT\_INFORMATION\_CLASS**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) enumeration that specifies what type of information the function queries.</span></span>

<span data-ttu-id="ef3cc-106">Sicherheits Attribut Variablen müssen im Client Kontext vorhanden sein, wenn in einem bedingten Ausdruck darauf verwiesen wird. Andernfalls wird der Ausdruck für den bedingten Ausdruck, der auf ihn verweist, als unbekannt ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="ef3cc-106">Security attribute variables must be present in the client context if referred to in a conditional expression; otherwise, the conditional expression term referencing them will be evaluated as unknown.</span></span> <span data-ttu-id="ef3cc-107">Weitere Informationen zu bedingten Ausdrücken finden Sie im Thema [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) .</span><span class="sxs-lookup"><span data-stu-id="ef3cc-107">For more information on conditional expressions, see the [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) topic.</span></span>

## <a name="example"></a><span data-ttu-id="ef3cc-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ef3cc-108">Example</span></span>

<span data-ttu-id="ef3cc-109">Im folgenden Beispiel wird der Client Kontext, der im Beispiel erstellt wurde, von der [Initialisierung eines Client Kontexts](initializing-a-client-context.md) abgefragt, um die Liste der [**SIDs**](/windows/desktop/api/Winnt/ns-winnt-sid) der diesem Client Kontext zugeordneten Gruppen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ef3cc-109">The following example queries the client context created in the example from [Initializing a Client Context](initializing-a-client-context.md) to retrieve the list of [**SIDs**](/windows/desktop/api/Winnt/ns-winnt-sid) of groups associated with that client context.</span></span>


```C++
BOOL GetGroupsFromContext(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{

    DWORD                cbSize = 0;
    PTOKEN_GROUPS        pTokenGroups=NULL;
    LPTSTR                StringSid = NULL;
    BOOL                bResult = FALSE;
    int i = 0;

    //Call the AuthzGetInformationFromContext function with a NULL output buffer to get the required buffer size.
    AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, 0, &cbSize, NULL);
    
        
    

    //Allocate the buffer for the TOKEN_GROUPS structure.
    pTokenGroups = (PTOKEN_GROUPS)malloc(cbSize);
    if (!pTokenGroups)
        return FALSE;

    //Get the SIDs of groups associated with the client context. 
    if(!AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, cbSize, &cbSize, pTokenGroups))
    {    
        printf_s("AuthzGetInformationFromContext failed with %d\n", GetLastError);
        free(pTokenGroups);
        return FALSE;
    }

    //Enumerate and display the group SIDs.
    for (i=pTokenGroups->GroupCount-1; i >= 0; --i)
    {
        //Convert a SID to a string.
        if(!ConvertSidToStringSid(
            pTokenGroups->Groups[i].Sid,
            &StringSid
            ))
        {
            LocalFree(StringSid);
            return FALSE;
        }


        wprintf_s(L"%s \n", StringSid);
        
    }

    free(pTokenGroups);

    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="ef3cc-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef3cc-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef3cc-111">Hinzufügen von SIDs zu einem Client Kontext</span><span class="sxs-lookup"><span data-stu-id="ef3cc-111">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="ef3cc-112">Caching-Zugriffs Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="ef3cc-112">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="ef3cc-113">Überprüfen des Zugriffs mit der Authz-API</span><span class="sxs-lookup"><span data-stu-id="ef3cc-113">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="ef3cc-114">Funktionsweise von Access Check</span><span class="sxs-lookup"><span data-stu-id="ef3cc-114">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="ef3cc-115">Initialisieren eines Client Kontexts</span><span class="sxs-lookup"><span data-stu-id="ef3cc-115">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="ef3cc-116">Sicherheits Deskriptor-Definitions Sprache für bedingte ACEs</span><span class="sxs-lookup"><span data-stu-id="ef3cc-116">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 



