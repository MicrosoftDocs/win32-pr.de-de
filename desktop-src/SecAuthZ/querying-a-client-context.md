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
# <a name="querying-a-client-context"></a>Abfragen eines Client Kontexts

Anwendungen können die [**AuthZGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) -Funktion aufrufen, um Informationen über einen vorhandenen Client Kontext abzufragen.

Der *infoclass* -Parameter der [**AuthZGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) -Funktion nimmt einen Wert aus der [**Authz- \_ Kontext \_ Informations \_ Klassen**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) -Enumeration an, der angibt, welche Art von Informationen die Funktion abfragt.

Sicherheits Attribut Variablen müssen im Client Kontext vorhanden sein, wenn in einem bedingten Ausdruck darauf verwiesen wird. Andernfalls wird der Ausdruck für den bedingten Ausdruck, der auf ihn verweist, als unbekannt ausgewertet. Weitere Informationen zu bedingten Ausdrücken finden Sie im Thema [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) .

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird der Client Kontext, der im Beispiel erstellt wurde, von der [Initialisierung eines Client Kontexts](initializing-a-client-context.md) abgefragt, um die Liste der [**SIDs**](/windows/desktop/api/Winnt/ns-winnt-sid) der diesem Client Kontext zugeordneten Gruppen abzurufen.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hinzufügen von SIDs zu einem Client Kontext](adding-sids-to-a-client-context.md)
</dt> <dt>

[Caching-Zugriffs Überprüfungen](caching-access-checks.md)
</dt> <dt>

[Überprüfen des Zugriffs mit der Authz-API](checking-access-with-authz-api.md)
</dt> <dt>

[Funktionsweise von Access Check](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[Initialisieren eines Client Kontexts](initializing-a-client-context.md)
</dt> <dt>

[Sicherheits Deskriptor-Definitions Sprache für bedingte ACEs](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 



