---
description: Wenn eine Anwendung eine Zugriffsüberprüfung durch Aufrufen der Funktion "AuhzAccessCheck" ausführt, können die Ergebnisse dieser Zugriffsüberprüfung zwischengespeichert werden.
ms.assetid: d79a5683-6c67-487f-b9a6-4e80da38b827
title: Zwischenspeichern von Zugriffsüberprüfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83659c35fb9334e55bd7dfcd2368275dc16eb0d4836b8d6fa69a6ed8d713d953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783555"
---
# <a name="caching-access-checks"></a>Zwischenspeichern von Zugriffsüberprüfungen

Wenn eine Anwendung eine Zugriffsüberprüfung durch Aufrufen der [**Funktion "PerformhzAccessCheck"**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) durchführt, können die Ergebnisse dieser Zugriffsüberprüfung zwischengespeichert werden. Wenn der *pAuthzHandle-Parameter* der [**Funktion "AuthhzAccessCheck"**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) nicht **NULL** ist, führt die Funktion eine separate Zugriffsüberprüfung mit der angeforderten [**ACCESS \_ MASK**](access-mask.md) von **MAXIMUM \_ ALLOWED** aus und speichert die Ergebnisse dieser Überprüfung zwischen. Ein Handle für die Ergebnisse dieser Überprüfung kann dann als *Parameter Vom Typ "KindhzHandle"* an die [**Funktion "SollhzCachedAccessCheck" übergeben**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) werden. Dies ermöglicht eine schnellere Zugriffsüberprüfung für einen bestimmten Client und [*Sicherheitsdeskriptoren.*](/windows/desktop/SecGloss/s-gly)

Nur der statische Teil einer Zugriffsüberprüfung kann zwischengespeichert werden. Alle [*Rückruf-Zugriffssteuerungseinträge*](/windows/desktop/SecGloss/a-gly) (ACEs) oder ACEs, die die **\_ PRINCIPAL-SELF-SID** enthalten, müssen für jede Zugriffsüberprüfung ausgewertet werden.

Attributvariablen müssen in Form eines Ausdrucks sein, wenn sie mit logischen Operatoren verwendet werden. andernfalls werden sie als unbekannt ausgewertet.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird der Zugriff auf ein zwischengespeichertes Ergebnis einer vorherigen Zugriffsüberprüfung überprüft. Die vorherige Zugriffsüberprüfung wurde im Beispiel unter [Überprüfen des Zugriffs mit Authz API.](checking-access-with-authz-api.md)


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hinzufügen von SIDs zu einem Clientkontext](adding-sids-to-a-client-context.md)
</dt> <dt>

[Überprüfen des Zugriffs mit Authz API](checking-access-with-authz-api.md)
</dt> <dt>

[Initialisieren eines Clientkontexts](initializing-a-client-context.md)
</dt> <dt>

[Abfragen eines Clientkontexts](querying-a-client-context.md)
</dt> </dl>

 

 
