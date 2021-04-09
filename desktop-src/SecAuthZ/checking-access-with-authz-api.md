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
# <a name="checking-access-with-authz-api"></a>Überprüfen des Zugriffs mit der Authz-API

Anwendungen bestimmen, ob der Zugriff auf Sicherungs fähige Objekte durch Aufrufen der [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) -Funktion gewährt werden soll.

Die [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) -Funktion nimmt sowohl [**Authz- \_ zugriffsanforderungs \_**](/windows/desktop/api/Authz/ns-authz-authz_access_request) -als auch [**Sicherheits \_ deskriptorstrukturen**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) als Parameter an. Die **Authz- \_ Zugriffs \_ Anforderungs** Struktur gibt eine angeforderte Zugriffsebene an. Die **authzaccesscheck** -Funktion wertet den angeforderten Zugriff anhand der angegebenen **Sicherheits \_ Beschreibung** für einen angegebenen Client Kontext aus. Informationen dazu, wie ein Sicherheits Deskriptor den Zugriff auf ein Objekt steuert, finden Sie unter [Steuern des Zugriffs auf ein Objekt durch DACLs](how-dacls-control-access-to-an-object.md).

Attribut Variablen müssen in Form eines Ausdrucks vorliegen, wenn Sie mit logischen Operatoren verwendet werden. Andernfalls werden Sie als UNKNOWN ausgewertet.

## <a name="callback-function"></a>Rückruffunktion

Wenn die [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) der [**Sicherheits \_ Beschreibung**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) des zu überprüfenden Objekts alle Rückruf [*Zugriffs Steuerungs Einträge*](/windows/desktop/SecGloss/a-gly) (ACEs) enthält, ruft [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) die [**authzaccesscheckcallback**](authzaccesscheckcallback.md) -Funktion für jeden Rückruf-ACE auf, der in der DACL enthalten ist. Ein Rückruf-ACE ist eine beliebige ACE-Struktur, deren ACE-Typ das Wort "Callback" enthält. Die **authzaccesscheckcallback** -Funktion ist eine Anwendungs definierte Funktion, die registriert werden muss, wenn der Ressourcen-Manager durch Aufrufen der [**authzinitializeresourcemanager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) -Funktion initialisiert wird.

Eine Rückruffunktion ermöglicht es einer Anwendung, Geschäftslogik zu definieren, die zur Laufzeit ausgewertet werden soll. Wenn die [**authzaccesscheckcallback**](authzaccesscheckcallback.md) -Funktion aufgerufen wird, wird der Rückruf-ACE, der den Aufruf ausgelöst hat, zur Auswertung an die Rückruffunktion übermittelt. Wenn die von der Anwendung definierte Logik als **true** ausgewertet wird, ist der Rückruf-ACE in der Zugriffs Überprüfung enthalten. Andernfalls wird sie ignoriert.

## <a name="caching-access-results"></a>Caching-Zugriffs Ergebnisse

Die Ergebnisse einer Zugriffs Überprüfung können zwischengespeichert und in zukünftigen Aufrufen der [**authzcachedaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) -Funktion verwendet werden. Weitere Informationen zum Zwischenspeichern von Zugriffs Überprüfungen, einschließlich eines Beispiels, finden Sie unter [Caching Access Checks](caching-access-checks.md).

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird eine [**Sicherheits \_ Beschreibung**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) erstellt, die **Lese \_** Zugriff auf integrierte Administratoren ermöglicht. Diese Sicherheits Beschreibung wird verwendet, um den Zugriff für den Client zu überprüfen, der durch den Client Kontext angegeben wird, der im Beispiel unter [Initialisieren eines Client Kontexts](initializing-a-client-context.md)erstellt wurde.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hinzufügen von SIDs zu einem Client Kontext](adding-sids-to-a-client-context.md)
</dt> <dt>

[Caching-Zugriffs Überprüfungen](caching-access-checks.md)
</dt> <dt>

[Initialisieren eines Client Kontexts](initializing-a-client-context.md)
</dt> <dt>

[Abfragen eines Client Kontexts](querying-a-client-context.md)
</dt> </dl>

 

 
