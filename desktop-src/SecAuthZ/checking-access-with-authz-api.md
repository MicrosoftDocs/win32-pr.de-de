---
description: Anwendungen bestimmen, ob Zugriff auf sicherungsfähige Objekte gewährt werden soll, indem sie die Funktion "SollhzAccessCheck" aufrufen.
ms.assetid: dad0a102-08ed-4cd2-bef5-87bc48fc7fc2
title: Überprüfen des Zugriffs mit Authz API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876c3b5305e33969f63932fdc9e1e4f6767c95a64b11272283420a377b39f795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783096"
---
# <a name="checking-access-with-authz-api"></a>Überprüfen des Zugriffs mit Authz API

Anwendungen bestimmen, ob Zugriff auf sicherungsfähige Objekte gewährt werden soll, indem sie die [**Funktion "BishzAccessCheck"**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) aufrufen.

Die [**FunktionSkripthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) verwendet [**sowohl DIE ACCESS \_ \_ REQUEST-**](/windows/desktop/api/Authz/ns-authz-authz_access_request) als auch die [**SECURITY \_ DESCRIPTOR-Struktur als**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) Parameter. Die **ACCESS \_ \_ REQUEST-Struktur von AUHZ** gibt eine angeforderte Zugriffsebene an. Die **FunktionSkripthzAccessCheck** wertet den angeforderten Zugriff für den angegebenen **SECURITY \_ DESCRIPTOR** für einen angegebenen Clientkontext aus. Informationen dazu, wie ein Sicherheitsdeskriptor den Zugriff auf ein Objekt steuert, finden Sie unter Steuern des Zugriffs auf [ein Objekt durch DACLs.](how-dacls-control-access-to-an-object.md)

Attributvariablen müssen in Form eines Ausdrucks sein, wenn sie mit logischen Operatoren verwendet werden. andernfalls werden sie als unbekannt ausgewertet.

## <a name="callback-function"></a>Rückruffunktion

Wenn die DACL [*(Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) des [**SECURITY \_ DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) des zu überprüfenden Objekts Rückrufeinträge [*für*](/windows/desktop/SecGloss/a-gly) die Zugriffssteuerung (ACEs) enthält, [**ruftCheckhzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) für jeden Rückruf-ACE, der in der DACL enthalten ist, die [**Funktion "CheckhzAccessCheckCallback"**](authzaccesscheckcallback.md) auf. Ein Rückruf-ACE ist eine beliebige ACE-Struktur, deren ACE-Typ das Wort "Rückruf" enthält. Die **Funktion "IntendhzAccessCheckCallback"** ist eine anwendungsdefinierte Funktion, die registriert werden muss, wenn der Ressourcen-Manager initialisiert wird, indem die [**Funktion "QshzInitializeResourceManager" aufgerufen**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) wird.

Mit einer Rückruffunktion kann eine Anwendung geschäftslogik definieren, die zur Laufzeit ausgewertet werden soll. Beim Aufruf [**der Funktion "ProgrammhzAccessCheckCallback"**](authzaccesscheckcallback.md) wird der Rückruf-ACE, der den Aufruf verursacht hat, zur Auswertung an die Rückruffunktion übergeben. Wenn die anwendungsdefinierte Logik als **TRUE ausgewertet** wird, wird der Rückruf-ACE in die Zugriffsüberprüfung einbezogen. Andernfalls wird sie ignoriert.

## <a name="caching-access-results"></a>Zwischenspeichern von Zugriffsergebnissen

Die Ergebnisse einer Zugriffsüberprüfung können zwischengespeichert und in zukünftigen Aufrufen der [**Funktion "AuhzCachedAccessCheck" verwendet**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) werden. Weitere Informationen zum Zwischenspeichern von Zugriffsüberprüfungen, einschließlich eines Beispiels, finden Sie unter [Zwischenspeichern von Zugriffsüberprüfungen.](caching-access-checks.md)

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird ein [**SECURITY \_ DESCRIPTOR erstellt,**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) der **den READ \_ CONTROL-Zugriff** für integrierte Administratoren zulässt. Er verwendet diesen Sicherheitsdeskriptor, um den Zugriff auf den Client zu überprüfen, der durch den Clientkontext angegeben wird, der im Beispiel unter [Initialisieren eines Clientkontexts erstellt wurde.](initializing-a-client-context.md)


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

[Hinzufügen von SIDs zu einem Clientkontext](adding-sids-to-a-client-context.md)
</dt> <dt>

[Zwischenspeichern von Zugriffsüberprüfungen](caching-access-checks.md)
</dt> <dt>

[Initialisieren eines Clientkontexts](initializing-a-client-context.md)
</dt> <dt>

[Abfragen eines Clientkontexts](querying-a-client-context.md)
</dt> </dl>

 

 
