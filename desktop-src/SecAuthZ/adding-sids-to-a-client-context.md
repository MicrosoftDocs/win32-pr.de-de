---
description: Eine Anwendung kann einem vorhandenen Clientkontext Sicherheits-IDs (SIDs) hinzufügen, indem sie die Funktion "HzAddSidsToContext" aufruft.
ms.assetid: d49ce47b-e91a-452b-b423-07e8d282d28a
title: Hinzufügen von SIDs zu einem Clientkontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07805031d299efc400c491c7fff1c43653e90b53f6c753c81a8676d4b0941b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784922"
---
# <a name="adding-sids-to-a-client-context"></a>Hinzufügen von SIDs zu einem Clientkontext

Eine Anwendung kann [*einem*](/windows/desktop/SecGloss/s-gly) vorhandenen Clientkontext Sicherheits-IDs (SIDs) hinzufügen, indem sie die Funktion [**"HzAddSidsToContext"**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) aufruft. Mit [**der Funktion "PerlhzAddSidsToContext"**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) kann eine Anwendung sowohl eine Liste von SIDs als auch eine Liste der SiDs auf den angegebenen Clientkontext beschränken.

Das System verwendet die Liste der einschränkenden SIDs, wenn es den Zugriff des Tokens auf ein sicherungsfähiges Objekt überprüft. Wenn ein eingeschränkter Prozess oder Thread versucht, auf ein sicherungsfähiges Objekt zu zugreifen, führt das System zwei Zugriffsüberprüfungen durch: eine mit aktivierten SIDs des Tokens und eine andere mithilfe der Liste der einschränkenden SIDs. Der Zugriff wird nur gewährt, wenn beide Zugriffsüberprüfungen die angeforderten Zugriffsrechte zulassen.

Attributvariablen müssen in Form eines Ausdrucks sein, wenn sie mit logischen Operatoren verwendet werden. Andernfalls werden sie als unbekannt ausgewertet.

## <a name="example"></a>Beispiel

Im folgenden Beispiel werden dem Clientkontext, der im Beispiel unter Initialisieren eines Clientkontexts erstellt wurde, eine SID und eine [einschränkende SID hinzufügt.](initializing-a-client-context.md)


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

[Zwischenspeichern von Zugriffsüberprüfungen](caching-access-checks.md)
</dt> <dt>

[Überprüfen des Zugriffs mit Authz API](checking-access-with-authz-api.md)
</dt> <dt>

[Initialisieren eines Clientkontexts](initializing-a-client-context.md)
</dt> <dt>

[Abfragen eines Clientkontexts](querying-a-client-context.md)
</dt> </dl>

 

 
