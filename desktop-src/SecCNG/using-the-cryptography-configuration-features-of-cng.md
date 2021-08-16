---
description: Stellt Funktionen zum Aufzählen und Abrufen von Informationen zu registrierten Anbietern zur Verfügung.
ms.assetid: 5b07060e-0c66-4bf2-b697-05231cb38375
title: Verwenden der Kryptografiekonfigurationsfunktionen von CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa1845d7c1df7afb95b93446b1e86b3838aed7e0ef51bb0e53b6f7a83f3515b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905399"
---
# <a name="using-the-cryptography-configuration-features-of-cng"></a>Verwenden der Kryptografiekonfigurationsfunktionen von CNG

Die CNG-API stellt Funktionen zum Aufzählen und Abrufen von Informationen zu registrierten Anbietern bereit.

-   [Auflisten von Anbietern](#enumerating-providers)
-   [Abrufen von Informationen zur Anbieterregistrierung](#getting-provider-registration-information)

## <a name="enumerating-providers"></a>Auflisten von Anbietern

Sie verwenden die [**BCryptEnumRegisteredProviders-Funktion,**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) um die registrierten Anbieter zu aufzählen. Die **BCryptEnumRegisteredProviders-Funktion** kann auf zwei Arten aufgerufen werden:

1.  Die erste besteht in der Zuweisung des Arbeitsspeichers durch die [**BCryptEnumRegisteredProviders-Funktion.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) Dies wird erreicht, indem die Adresse eines **NULL-Zeigers** für den *ppBuffer-Parameter übergeben* wird. Mit diesem Code wird der erforderliche Arbeitsspeicher für die [**CRYPT \_ PROVIDERS-Struktur**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) und die zugeordneten Zeichenfolgen zugeordnet. Wenn die **BCryptEnumRegisteredProviders-Funktion** auf diese Weise verwendet wird, müssen Sie den Arbeitsspeicher frei geben, wenn er nicht mehr benötigt wird, indem Sie *ppBuffer* an die [**BCryptFreeBuffer-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) übergeben.

    Das folgende Beispiel zeigt, wie Sie die [**BCryptEnumRegisteredProviders-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) verwenden, um den Puffer für Sie zu reservieren.

    ```C++
    #include <windows.h>

    #ifndef NT_SUCCESS
    #define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
    #endif

    void EnumProviders1()
    {
        NTSTATUS status;
        ULONG cbBuffer = 0;
        PCRYPT_PROVIDERS pBuffer = NULL;

        /*
        Get the providers, letting the BCryptEnumRegisteredProviders 
        function allocate the memory.
        */
        status = BCryptEnumRegisteredProviders(&cbBuffer, &pBuffer);

        if (NT_SUCCESS(status))
        {
            if (pBuffer != NULL)
            {
                // Enumerate the providers.
                for (ULONG i = 0; i < pBuffer->cProviders; i++)
                {
                    printf("%S\n", pBuffer->rgpszProviders[i]);
                }
            }
        }
        else
        {
            printf("BCryptEnumRegisteredProviders failed with error " 
                "code 0x%08x\n", status);
        }

        if (NULL != pBuffer)
        {
            /*
            Free the memory allocated by the 
            BCryptEnumRegisteredProviders function.
            */
            BCryptFreeBuffer(pBuffer);
        }
    }
    
    ```

    

2.  Die zweite Methode besteht im Zuweisen des erforderlichen Arbeitsspeichers selbst. Dies wird erreicht, indem die [**BCryptEnumRegisteredProviders-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) mit **NULL für** den *ppBuffer-Parameter aufgerufen* wird. Die **BCryptEnumRegisteredProviders-Funktion** wird in den Wert, auf den durch den *parameterregistrBuffer* verwiesen wird, die erforderliche Größe der [**CRYPT \_ PROVIDERS-Struktur**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) und aller Zeichenfolgen in Byte platzieren. Anschließend weisen Sie den erforderlichen Arbeitsspeicher zu und übergeben die Adresse dieses Pufferzeigers für den *ppBuffer-Parameter* in einem zweiten Aufruf der **BCryptEnumRegisteredProviders-Funktion.**

    Das folgende Beispiel zeigt, wie Sie die [**BCryptEnumRegisteredProviders-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) verwenden, um Ihren eigenen Puffer zu zuordnen und zu verwenden.

    ```C++
    #include <windows.h>
    #include <stdio.h>

    #ifndef NT_SUCCESS
    #define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
    #endif

    void EnumProviders2()
    {
        NTSTATUS status;
        ULONG cbBuffer = 0;

        // Get the required size of the buffer.
        status = BCryptEnumRegisteredProviders(&cbBuffer, NULL);

        if (STATUS_BUFFER_TOO_SMALL == status)
        {
            // Allocate the buffer.
            PCRYPT_PROVIDERS pBuffer = 
                (PCRYPT_PROVIDERS)LocalAlloc(LPTR, cbBuffer);
            if (NULL != pBuffer)
            {
                // Get the providers in the buffer that was allocated.
                status = BCryptEnumRegisteredProviders(
                    &cbBuffer, 
                    &pBuffer);
                if (NT_SUCCESS(status))
                {
                    for (ULONG i = 0; i < pBuffer->cProviders; i++)
                    {
                        // Enumerate the providers.
                        printf("%S\n", pBuffer->rgpszProviders[i]);
                    }
                }

                // Free the memory that was allocated.
                LocalFree(pBuffer);
            }
        }
    }
    
    ```

    

## <a name="getting-provider-registration-information"></a>Abrufen von Anbieterregistrierungsinformationen

Die [**BCryptQueryProviderRegistration-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) wird verwendet, um zusätzliche registrierungsspezifische Informationen zu einem Anbieter zu erhalten. Diese Funktion verwendet den Namen des Anbieters, für den Sie Informationen abrufen möchten, den gewünschten Anbietermodus (Kernelmodus, Benutzermodus oder beides) und den Bezeichner der Anbieterschnittstelle, für den die Registrierungsinformationen abgerufen werden. Um beispielsweise die Registrierungsinformationen für den Benutzermodus für die Verschlüsselungsschnittstelle für den Anbieter "Microsoft Primitive Provider" zu erhalten, würden Sie einen Aufruf ähnlich dem folgenden ausführen.


```C++
BCryptQueryProviderRegistration(
    MS_PRIMITIVE_PROVIDER,
    CRYPT_UM,
    BCRYPT_CIPHER_INTERFACE,
    //...
    );

```



Wie die [**BCryptEnumRegisteredProviders-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) kann die [**BCryptQueryProviderRegistration-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) entweder Arbeitsspeicher für Sie zuweisen, oder Sie können den Arbeitsspeicher selbst zuweisen. Der Prozess ist für die beiden Funktionen identisch.

 

 



