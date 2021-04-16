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
# <a name="adding-sids-to-a-client-context"></a>Hinzufügen von SIDs zu einem Client Kontext

Eine Anwendung kann einem vorhandenen Client Kontext [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -IDs (SIDs) hinzufügen, indem Sie die [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) -Funktion aufrufen. Die [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) -Funktion ermöglicht es einer Anwendung, sowohl eine Liste von SIDs als auch eine Liste mit einschränkenden SIDs auf den angegebenen Client Kontext anzugeben.

Das System verwendet die Liste der einschränkenden SIDs, wenn der Zugriff des Tokens auf ein Sicherungs fähiges Objekt überprüft wird. Wenn ein eingeschränkter Prozess oder Thread versucht, auf ein Sicherungs fähiges Objekt zuzugreifen, führt das System zwei Zugriffs Überprüfungen durch: einen, der die aktivierten SIDs des Tokens verwendet, und einen anderen, der die Liste der einschränkenden SIDs verwendet. Der Zugriff wird nur gewährt, wenn beide Zugriffs Überprüfungen die angeforderten Zugriffsrechte zulassen.

Attribut Variablen müssen in Form eines Ausdrucks vorliegen, wenn Sie mit logischen Operatoren verwendet werden. Andernfalls werden Sie als UNKNOWN ausgewertet.

## <a name="example"></a>Beispiel

Im folgenden Beispiel werden eine SID und eine einschränkende sid dem Client Kontext hinzugefügt, der im Beispiel unter [Initialisieren eines Client Kontexts](initializing-a-client-context.md)erstellt wurde.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Caching-Zugriffs Überprüfungen](caching-access-checks.md)
</dt> <dt>

[Überprüfen des Zugriffs mit der Authz-API](checking-access-with-authz-api.md)
</dt> <dt>

[Initialisieren eines Client Kontexts](initializing-a-client-context.md)
</dt> <dt>

[Abfragen eines Client Kontexts](querying-a-client-context.md)
</dt> </dl>

 

 
