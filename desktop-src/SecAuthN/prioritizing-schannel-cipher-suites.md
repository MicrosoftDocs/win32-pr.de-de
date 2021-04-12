---
description: 'Cryptography API: Next Generation (CNG) stellt Funktionen bereit, mit denen die Verschlüsselungs Sammlungen, die von einem Anbieter unterstützt werden, abgefragt, hinzugefügt, entfernt und priorisiert werden. Mit diesen Funktionen vorgenommene Änderungen werden sofort wirksam, und es ist nicht erforderlich, einen aktiven Server neu zu starten.'
ms.assetid: e919be5c-ac2c-446c-a422-971805b1f672
title: Priorisieren von SChannel-Verschlüsselungs Sammlungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f885c4d51006233be252a02c7cc3bebd26a4e6c3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219071"
---
# <a name="prioritizing-schannel-cipher-suites"></a>Priorisieren von SChannel-Verschlüsselungs Sammlungen

[Cryptography API: Next Generation](../seccng/cng-portal.md) (CNG) stellt Funktionen bereit, mit denen die Verschlüsselungs Sammlungen, die von einem Anbieter unterstützt werden, abgefragt, hinzugefügt, entfernt und priorisiert werden. Mit diesen Funktionen vorgenommene Änderungen werden sofort wirksam, und es ist nicht erforderlich, einen aktiven Server neu zu starten.

> [!Note]
> Sie können auch die Liste der Verschlüsselungs Sammlungen ändern, indem Sie die Gruppenrichtlinien Einstellungen für die Verschlüsselung der SSL-Verschlüsselungs **Sammlung** mithilfe des Snap-Ins "Gruppenrichtlinie-Objekt" in der Microsoft Management Console konfigurieren.
> 
> **So konfigurieren Sie die Gruppenrichtlinien Einstellung "SSL-Verschlüsselungs **Sammlung** "**
> 
> 1.  Geben Sie an einer Eingabeaufforderung **gpeer dit. msc** ein. Der **Gruppenrichtlinienobjekt-Editor** wird angezeigt.
> 2.  Erweitern Sie **Computer Konfiguration**, **Administrative Vorlagen** und **Netzwerk**, und klicken Sie dann auf **SSL-Konfigurationseinstellungen**.
> 3.  Klicken Sie unter **SSL-Konfigurationseinstellungen** auf die Einstellung für die **Reihenfolge der SSL** -Verschlüsselungs Sammlungen.
> 4.  Scrollen Sie im Bereich für die **Reihenfolge der SSL** -Verschlüsselungs Sammlungen zum unteren Rand des Bereichs.
> 5.  Befolgen Sie die Anweisungen **zum Ändern dieser Einstellung**.
> 
> Sie müssen den Computer neu starten, nachdem Sie diese Einstellung geändert haben, damit die Änderungen wirksam werden.

 

Die Liste der Verschlüsselungs Sammlungen ist auf 1023 Zeichen beschränkt.

Informationen zum Priorisieren von SChannel-Verschlüsselungs Sammlungen finden Sie in den folgenden Beispielen.

-   [Auflisten unterstützter Verschlüsselungs Sammlungen](#listing-supported-cipher-suites)
-   [Hinzufügen, entfernen und Priorisieren von Verschlüsselungs Sammlungen](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a>Auflisten unterstützter Verschlüsselungs Sammlungen

Aufrufen der Funktion " [**bcryptenumschlag**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) " zum Auflisten der Verschlüsselungs Sammlungen, die von einem Anbieter in der Reihenfolge ihrer Priorität unterstützt werden.

Im folgenden Beispiel wird veranschaulicht, wie mit der Funktion " [**bcryptenumschlag**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) " unterstützte Verschlüsselungs Sammlungen aufgelistet werden.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{

   HRESULT Status = ERROR_SUCCESS;
   DWORD   cbBuffer = 0;
   PCRYPT_CONTEXT_FUNCTIONS pBuffer = NULL;

    Status = BCryptEnumContextFunctions(
        CRYPT_LOCAL,
        L"SSL",
        NCRYPT_SCHANNEL_INTERFACE,
        &cbBuffer,
        &pBuffer);
    if(FAILED(Status))
    {
        printf_s("\n**** Error 0x%x returned by BCryptEnumContextFunctions\n", Status);
        goto Cleanup;
    }
                
    if(pBuffer == NULL)
    {
        printf_s("\n**** Error pBuffer returned from BCryptEnumContextFunctions is null");
        goto Cleanup;
    }

    printf_s("\n\n Listing Cipher Suites ");
    for(UINT index = 0; index < pBuffer->cFunctions; ++index)
    {
        printf_s("\n%S", pBuffer->rgpszFunctions[index]);
    }

Cleanup:
    if (pBuffer != NULL)
    {
        BCryptFreeBuffer(pBuffer);
    }
}


```



## <a name="adding-removing-and-prioritizing-cipher-suites"></a>Hinzufügen, entfernen und Priorisieren von Verschlüsselungs Sammlungen

Aufrufen der Funktionen [**bcryptaddcontextfunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) und [**bcryptremuvecontextfunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) zum Hinzufügen und Entfernen von Verschlüsselungs Sammlungen aus der Liste der unterstützten Verschlüsselungs Sammlungen.

Legen Sie beim Hinzufügen einer Verschlüsselungs Sammlung den Wert des *dwposition* -Parameters der Funktion " [**bcryptaddcontextfunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) " auf " **crypt \_ Priorität \_ oben** " fest, um ihn am Anfang der priorisierten Liste hinzuzufügen, oder auf die nach-oben- **\_ \_ Seite** , um ihn am Ende der Liste hinzuzufügen.

Um die Liste der Verschlüsselungs Sammlungen zu priorisieren, entfernen Sie alle Verschlüsselungs Sammlungen aus der Liste, und fügen Sie der Liste anschließend Verschlüsselungs Sammlungen in der gewünschten Reihenfolge hinzu.

Im folgenden Beispiel wird gezeigt, wie eine Verschlüsselungs Sammlung am Anfang der priorisierten Liste für den standardmäßigen Microsoft SChannel-Anbieter hinzugefügt wird.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{
    
    SECURITY_STATUS Status = ERROR_SUCCESS;
    LPWSTR wszCipher = (L"RSA_EXPORT1024_DES_CBC_SHA");
       
    Status = BCryptAddContextFunction(
                CRYPT_LOCAL,
                L"SSL",
                NCRYPT_SCHANNEL_INTERFACE,
                wszCipher,
                CRYPT_PRIORITY_TOP);
}


```



Im folgenden Beispiel wird gezeigt, wie eine Verschlüsselungs Sammlung aus der priorisierten Liste für den standardmäßigen Microsoft SChannel-Anbieter entfernt wird.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{
    
    SECURITY_STATUS Status = ERROR_SUCCESS;
      LPWSTR wszCipher = (L"TLS_RSA_WITH_RC4_128_SHA");
       
    Status = BCryptRemoveContextFunction(
                CRYPT_LOCAL,
                L"SSL",
                NCRYPT_SCHANNEL_INTERFACE,
                wszCipher);
}


```



 

 
