---
description: 'Kryptografie-API: Next Generation (CNG) stellt Funktionen bereit, die die von einem Anbieter unterstützten Verschlüsselungssammlungen abfragen, hinzufügen, entfernen und priorisieren. Änderungen, die mit diesen Funktionen vorgenommen werden, werden sofort wirksam und erfordern keinen Neustart eines aktiven Servers.'
ms.assetid: e919be5c-ac2c-446c-a422-971805b1f672
title: Priorisieren von Schannel-Verschlüsselungssammlungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4436d2f72ebaa1f8d551d935ea9f16d2c03cd7c75fc7d40a73f1a27c7406ad6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920769"
---
# <a name="prioritizing-schannel-cipher-suites"></a>Priorisieren von Schannel-Verschlüsselungssammlungen

[Kryptografie-API: Next Generation](../seccng/cng-portal.md) (CNG) stellt Funktionen bereit, die die von einem Anbieter unterstützten Verschlüsselungssammlungen abfragen, hinzufügen, entfernen und priorisieren. Änderungen, die mit diesen Funktionen vorgenommen werden, werden sofort wirksam und erfordern keinen Neustart eines aktiven Servers.

> [!Note]
> Sie können die Liste der Verschlüsselungssammlungen auch ändern, indem Sie die Gruppenrichtlinieneinstellungen der **SSL Cipher Suite Order** mithilfe des Gruppenrichtlinie Object-Snap-Ins in Microsoft Management Console konfigurieren.
> 
> **So konfigurieren Sie die Gruppenrichtlinieneinstellung **SSL Cipher Suite Order****
> 
> 1.  Geben Sie an einer Eingabeaufforderung **gpedit.msc** ein. Die **Gruppenrichtlinienobjekt-Editor** wird angezeigt.
> 2.  Erweitern Sie **Computerkonfiguration**, **Administrative Vorlagen**, **Netzwerk**, und klicken Sie dann auf **SSL-Konfiguration Einstellungen**.
> 3.  Klicken Sie **unter SSL-Konfiguration Einstellungen** auf die Einstellung **SSL Cipher Suite Order** .
> 4.  Scrollen Sie im Bereich **SSL Cipher Suite Order (SSL Cipher Suite-Reihenfolge)** zum unteren Rand des Bereichs.
> 5.  Befolgen Sie die Anweisungen mit der Bezeichnung **Ändern dieser Einstellung.**
> 
> Es ist erforderlich, den Computer neu zu starten, nachdem Sie diese Einstellung geändert haben, damit die Änderungen wirksam werden.

 

Die Liste der Verschlüsselungssammlungen ist auf 1023 Zeichen beschränkt.

Informationen zum Priorisieren von Schannel-Verschlüsselungssammlungen finden Sie in den folgenden Beispielen.

-   [Auflisten unterstützter Verschlüsselungssammlungen](#listing-supported-cipher-suites)
-   [Hinzufügen, Entfernen und Priorisieren von Verschlüsselungssammlungen](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a>Auflisten unterstützter Verschlüsselungssammlungen

Rufen Sie die [**BCryptEnumContextFunctions-Funktion**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) auf, um die Verschlüsselungssammlungen aufzulisten, die ein Anbieter nach Priorität unterstützt.

Im folgenden Beispiel wird veranschaulicht, wie die [**BCryptEnumContextFunctions-Funktion**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) verwendet wird, um unterstützte Verschlüsselungssammlungen aufzulisten.


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



## <a name="adding-removing-and-prioritizing-cipher-suites"></a>Hinzufügen, Entfernen und Priorisieren von Verschlüsselungssammlungen

Rufen Sie die Funktionen [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) und [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) auf, um Verschlüsselungssammlungen aus der Liste der unterstützten Verschlüsselungssammlungen hinzuzufügen und zu entfernen.

Legen Sie beim Hinzufügen einer Verschlüsselungssammlung den Wert des *dwPosition-Parameters* der [**BCryptAddContextFunction-Funktion**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) auf **CRYPT \_ PRIORITY \_ TOP** fest, um ihn am Anfang der priorisierten Liste hinzuzufügen, oder auf **CRYPT \_ PRIORITY \_ BOTTOM,** um ihn am Ende der Liste hinzuzufügen.

Um die Liste der Verschlüsselungssammlungen zu priorisieren, entfernen Sie alle Verschlüsselungssammlungen aus der Liste, und fügen Sie der Liste dann Verschlüsselungssammlungen in der gewünschten Reihenfolge hinzu.

Das folgende Beispiel zeigt, wie Sie eine Verschlüsselungssammlung am Anfang der priorisierten Liste für den Microsoft Schannel-Standardanbieter hinzufügen.


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



Das folgende Beispiel zeigt, wie Sie eine Verschlüsselungssammlung aus der priorisierten Liste für den Microsoft Schannel-Standardanbieter entfernen.


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



 

 
