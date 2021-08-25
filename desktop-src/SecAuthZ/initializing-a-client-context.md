---
description: Eine Anwendung muss einen Clientkontext erstellen, bevor sie Authz API zum Durchführen von Zugriffsüberprüfungen oder Überwachungen verwenden kann.
ms.assetid: 82f207ff-cac4-4e9a-a9e6-ddb3f6c8b30a
title: Initialisieren eines Clientkontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da8a3c3191f323cf6ce35fda90f4bd75299dac67183986998cf21a80c0ee6995
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908040"
---
# <a name="initializing-a-client-context"></a>Initialisieren eines Clientkontexts

Eine Anwendung muss einen Clientkontext erstellen, bevor sie Authz API zum Durchführen von Zugriffsüberprüfungen oder Überwachungen verwenden kann.

Eine Anwendung muss die [**AuthzInitializeResourceManager-Funktion**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) aufrufen, um den Ressourcen-Manager zu initialisieren. Die Anwendung kann dann eine von mehreren Funktionen aufrufen, um einen Clientkontext zu erstellen. Wenn Sie Zugriffsüberprüfungen oder Remoteüberwachungen durchführen, müssen Sie außerdem die [**Funktion AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) verwenden.

Um einen Clientkontext auf Grundlage eines vorhandenen Clientkontexts zu erstellen, rufen Sie die [**Funktion AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) auf.

Die [**AutohzInitializeContextFromToken-Funktion**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) erstellt mithilfe von Informationen in einem Anmeldetoken einen neuen Clientkontext. Die [**AutohzInitializeContextFromSid-Funktion**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) erstellt mithilfe der angegebenen [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid)einen neuen Clientkontext.

Rufen Sie nach Möglichkeit die [**AutohzInitializeContextFromToken-Funktion**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) anstelle von [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)auf. **AutoritititializeContextFromSid** versucht, die in einem Anmeldetoken verfügbaren Informationen abzurufen, bei denen der Client tatsächlich angemeldet war. Ein tatsächliches Anmeldetoken stellt weitere Informationen bereit, z. B. Anmeldetyp und Anmeldeeigenschaften, und gibt das Verhalten des Authentifizierungspakets wieder, das für die Anmeldung verwendet wird. Der von **AuthzInitializeContextFromToken** erstellte Clientkontext verwendet ein Anmeldetoken, und der resultierende Clientkontext ist vollständiger und genauer als ein Clientkontext, der von **AutorhzInitializeContextFromSid** erstellt wurde.

> [!Note]  
> Sicherheitsattributvariablen müssen im Clientkontext vorhanden sein, wenn in einem bedingten Ausdruck darauf verwiesen wird. Andernfalls wird der bedingte Ausdrucksausdruck, der auf sie verweist, als unbekannt ausgewertet. Weitere Informationen zu bedingten Ausdrücken finden Sie im Thema [Sicherheitsbeschreibungsdefinitionssprache für bedingte ACEs.](security-descriptor-definition-language-for-conditional-aces-.md)

 

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird der Authz-Ressourcen-Manager initialisiert und die [**AutohzInitializeContextFromToken-Funktion aufruft,**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) um einen Clientkontext aus dem Anmeldetoken zu erstellen, das dem aktuellen Prozess zugeordnet ist.


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

[Hinzufügen von SIDs zu einem Clientkontext](adding-sids-to-a-client-context.md)
</dt> <dt>

[Zwischenspeichern von Zugriffsüberprüfungen](caching-access-checks.md)
</dt> <dt>

[Überprüfen des Zugriffs mit Authz API](checking-access-with-authz-api.md)
</dt> <dt>

[Funktionsweise von AccessCheck](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[Abfragen eines Clientkontexts](querying-a-client-context.md)
</dt> <dt>

[Sicherheitsbeschreibungsdefinitionssprache für bedingte ACEs](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



