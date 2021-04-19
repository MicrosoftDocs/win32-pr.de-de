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
# <a name="initializing-a-client-context"></a>Initialisieren eines Client Kontexts

Eine Anwendung muss einen Client Kontext erstellen, bevor Sie mit der Authz-API Zugriffs Überprüfungen oder-Überwachungen durchführen kann.

Eine Anwendung muss die [**authzinitializeresourcemanager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) -Funktion zum Initialisieren des Ressourcen-Managers aufruft. Die Anwendung kann dann eine von mehreren Funktionen aufzurufen, um einen Client Kontext zu erstellen. Wenn Sie Zugriffs Überprüfungen oder die Überwachung Remote ausführen, müssen Sie außerdem die [**authzinitializeremoteresourcemanager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) -Funktion verwenden.

Um einen Client Kontext zu erstellen, der auf einem vorhandenen Client Kontext basiert, rufen Sie die [**authzinitializecontextfromauthzcontext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) -Funktion auf.

Die [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) -Funktion erstellt mithilfe der Informationen in einem Anmelde Token einen neuen Client Kontext. Die [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) -Funktion erstellt mithilfe der angegebenen [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid)einen neuen Client Kontext.

Wenn möglich, wird anstelle von [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)die [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) -Funktion aufgerufen. **AuthzInitializeContextFromSid** versucht, die in einem Anmelde Token verfügbaren Informationen abzurufen, wenn der Client tatsächlich angemeldet ist. Ein tatsächliches Anmelde Token bietet weitere Informationen, wie z. b. den Anmeldetyp und die Anmelde Eigenschaften, und gibt das Verhalten des Authentifizierungs Pakets an, das für die Anmeldung verwendet wird. Der von **AuthzInitializeContextFromToken** erstellte Client Kontext verwendet ein Anmelde Token, und der resultierende Client Kontext ist ausführender und präziser als ein von **AuthzInitializeContextFromSid** erstellter Client Kontext.

> [!Note]  
> Sicherheits Attribut Variablen müssen im Client Kontext vorhanden sein, wenn in einem bedingten Ausdruck darauf verwiesen wird. Andernfalls wird der Ausdruck für den bedingten Ausdruck, der auf ihn verweist, als unbekannt ausgewertet. Weitere Informationen zu bedingten Ausdrücken finden Sie im Thema [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) .

 

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird der Authz-Ressourcen-Manager initialisiert und die [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) -Funktion aufgerufen, um einen Client Kontext aus dem Anmelde Token zu erstellen, das dem aktuellen Prozess zugeordnet ist.


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

[Abfragen eines Client Kontexts](querying-a-client-context.md)
</dt> <dt>

[Sicherheits Deskriptor-Definitions Sprache für bedingte ACEs](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[**Authzinitializeremoteresourcemanager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**Authzinitializeresourcemanager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



