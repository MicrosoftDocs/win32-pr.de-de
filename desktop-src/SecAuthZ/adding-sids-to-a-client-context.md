---
description: Eine Anwendung kann einem vorhandenen Client Kontext Sicherheits-IDs (SIDs) hinzufügen, indem Sie die AuthzAddSidsToContext-Funktion aufrufen.
ms.assetid: d49ce47b-e91a-452b-b423-07e8d282d28a
title: Hinzufügen von SIDs zu einem Client Kontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a601f485110ddacea0fdb54cb7dcef587a25cb9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529729"
---
# <a name="adding-sids-to-a-client-context"></a><span data-ttu-id="f3ad4-103">Hinzufügen von SIDs zu einem Client Kontext</span><span class="sxs-lookup"><span data-stu-id="f3ad4-103">Adding SIDs to a Client Context</span></span>

<span data-ttu-id="f3ad4-104">Eine Anwendung kann einem vorhandenen Client Kontext [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -IDs (SIDs) hinzufügen, indem Sie die [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f3ad4-104">An application can add [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) to an existing client context by calling the [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function.</span></span> <span data-ttu-id="f3ad4-105">Die [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) -Funktion ermöglicht es einer Anwendung, sowohl eine Liste von SIDs als auch eine Liste mit einschränkenden SIDs auf den angegebenen Client Kontext anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f3ad4-105">The [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function allows an application to specify both a list of SIDs and a list of restricting SIDs to the specified client context.</span></span>

<span data-ttu-id="f3ad4-106">Das System verwendet die Liste der einschränkenden SIDs, wenn der Zugriff des Tokens auf ein Sicherungs fähiges Objekt überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="f3ad4-106">The system uses the list of restricting SIDs when it checks the token's access to a securable object.</span></span> <span data-ttu-id="f3ad4-107">Wenn ein eingeschränkter Prozess oder Thread versucht, auf ein Sicherungs fähiges Objekt zuzugreifen, führt das System zwei Zugriffs Überprüfungen durch: einen, der die aktivierten SIDs des Tokens verwendet, und einen anderen, der die Liste der einschränkenden SIDs verwendet.</span><span class="sxs-lookup"><span data-stu-id="f3ad4-107">When a restricted process or thread tries to access a securable object, the system performs two access checks: one using the token's enabled SIDs, and another using the list of restricting SIDs.</span></span> <span data-ttu-id="f3ad4-108">Der Zugriff wird nur gewährt, wenn beide Zugriffs Überprüfungen die angeforderten Zugriffsrechte zulassen.</span><span class="sxs-lookup"><span data-stu-id="f3ad4-108">Access is granted only if both access checks allow the requested access rights.</span></span>

<span data-ttu-id="f3ad4-109">Attribut Variablen müssen in Form eines Ausdrucks vorliegen, wenn Sie mit logischen Operatoren verwendet werden. Andernfalls werden Sie als UNKNOWN ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="f3ad4-109">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="example"></a><span data-ttu-id="f3ad4-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f3ad4-110">Example</span></span>

<span data-ttu-id="f3ad4-111">Im folgenden Beispiel werden eine SID und eine einschränkende sid dem Client Kontext hinzugefügt, der im Beispiel unter [Initialisieren eines Client Kontexts](initializing-a-client-context.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f3ad4-111">The following example adds a SID and a restricting SID to the client context created by the example in [Initializing a Client Context](initializing-a-client-context.md).</span></span>


```C++
BOOL AddSidsToContext(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{
    AUTHZ_CLIENT_CONTEXT_HANDLE        NewContext = NULL;
    PSID                            pEveryoneSid = NULL;
    PSID                            pLocalSid = NULL;
    SID_AND_ATTRIBUTES                Sids;
    SID_AND_ATTRIBUTES                RestrictedSids;
    DWORD                            SidCount = 0;
    DWORD                            RestrictedSidCount = 0;

    //Create a PSID from the "Everyone" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-1-0", &pEveryoneSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError());
        return FALSE;
    }

    //Create a PSID from the "Local" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-2-0", &pLocalSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError);
        return FALSE;
    }

    //Set the members of the SID_AND_ATTRIBUTES structure to be added.
    Sids.Sid = pEveryoneSid;
    Sids.Attributes = SE_GROUP_ENABLED;

    //Set the members of the SID_AND_ATTRIBUTES structure for the restricting SID.
    RestrictedSids.Sid = pLocalSid;
    RestrictedSids.Attributes = SE_GROUP_ENABLED;

    

    //Create a new context with the new "Everyone" SID and "Local" restricting SID.
    if(!AuthzAddSidsToContext(
        *phClientContext,
        &Sids,
        1,
        &RestrictedSids,
        1,
        &NewContext))
    {
        printf_s("AuthzAddSidsToContext failed with %d\n", GetLastError());
        if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        return FALSE;
    }

    if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        
        AuthzFreeContext(*phClientContext);
        *phClientContext = NewContext;

    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="f3ad4-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f3ad4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3ad4-113">Caching-Zugriffs Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="f3ad4-113">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="f3ad4-114">Überprüfen des Zugriffs mit der Authz-API</span><span class="sxs-lookup"><span data-stu-id="f3ad4-114">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="f3ad4-115">Initialisieren eines Client Kontexts</span><span class="sxs-lookup"><span data-stu-id="f3ad4-115">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="f3ad4-116">Abfragen eines Client Kontexts</span><span class="sxs-lookup"><span data-stu-id="f3ad4-116">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
