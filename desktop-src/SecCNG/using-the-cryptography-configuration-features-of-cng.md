---
description: Stellt Funktionen zum Aufzählen und Abrufen von Informationen zu registrierten Anbietern bereit.
ms.assetid: 5b07060e-0c66-4bf2-b697-05231cb38375
title: Verwenden der kryptografiekonfigurationsfeatures von CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd700b52810f43381722a315bec12216acd7b683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354487"
---
# <a name="using-the-cryptography-configuration-features-of-cng"></a>Verwenden der kryptografiekonfigurationsfeatures von CNG

Die CNG-API bietet Funktionen zum Auflisten und Abrufen von Informationen zu registrierten Anbietern.

-   [Auflisten von Anbietern](#enumerating-providers)
-   [Anbieter Registrierungsinformationen werden erhalten.](#getting-provider-registration-information)

## <a name="enumerating-providers"></a>Auflisten von Anbietern

Sie verwenden die Funktion " [**bcryptenumregisteredproviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) ", um die registrierten Anbieter aufzuzählen. Die Funktion " **bcryptenreregisteredproviders** " kann auf zwei Arten aufgerufen werden:

1.  Der erste besteht darin, dass die Funktion " [**bcryptenumschlag registeredproviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) " den Arbeitsspeicher zuweist. Dies wird erreicht, indem die Adresse eines **null** -Zeigers für den *ppbuffer* -Parameter übergeben wird. Mit diesem Code wird der erforderliche Arbeitsspeicher für die Struktur der [**crypt- \_ Anbieter**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) und die zugehörigen Zeichen folgen zugeordnet. Wenn die Funktion " **bcryptenreregisteredproviders** " auf diese Weise verwendet wird, müssen Sie den Arbeitsspeicher freigeben, wenn er nicht mehr benötigt wird, indem Sie *ppbuffer* an die Funktion " [**bcryptfreebuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) " übergeben.

    Im folgenden Beispiel wird gezeigt, wie Sie die Funktion " [**bcryptenumschlag registeredproviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) " verwenden, um den Puffer für Sie zuzuweisen.

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

    

2.  Die zweite Methode besteht darin, den erforderlichen Speicher selbst zuzuordnen. Dies wird erreicht, indem die Funktion " [**bcryptenumschlag registeredproviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) " mit **null** für den Parameter " *ppbuffer* " aufgerufen wird. Die Funktion " **bcryptenreregisteredproviders** " wird in den Wert eingefügt, auf den der Parameter " *pcbBuffer* " zeigt, die erforderliche Größe (in Bytes) der [**crypt- \_ Anbieter**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) Struktur und aller Zeichen folgen. Anschließend weisen Sie den erforderlichen Arbeitsspeicher zu und übergeben die Adresse dieses Puffer Zeigers für den *ppbuffer* -Parameter in einem zweiten Aufrufen der Funktion " **bcryptenumregisteredproviders** ".

    Im folgenden Beispiel wird gezeigt, wie Sie die Funktion " [**bcryptenumschlag registeredproviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) " verwenden, um Ihren eigenen Puffer zuzuordnen und zu verwenden.

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

    

## <a name="getting-provider-registration-information"></a>Anbieter Registrierungsinformationen werden erhalten.

Die Funktion " [**bcryptqueryproviderregistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) " dient zum Abrufen zusätzlicher Registrierungs spezifischer Informationen über einen Anbieter. Diese Funktion nimmt den Namen des Anbieters, für den Sie Informationen abrufen möchten, den gewünschten Anbieter Modus (Kernel Modus, Benutzermodus oder beides) und den Bezeichner der Anbieter Schnittstelle auf, für den die Registrierungsinformationen abgerufen werden sollen. Wenn Sie z. b. die Registrierungsinformationen für den Benutzermodus für die Verschlüsselungs Schnittstelle für den Anbieter "Microsoft primitiver Anbieter" abrufen möchten, würden Sie einen ähnlichen Befehl wie den folgenden erstellen.


```C++
BCryptQueryProviderRegistration(
    MS_PRIMITIVE_PROVIDER,
    CRYPT_UM,
    BCRYPT_CIPHER_INTERFACE,
    //...
    );

```



Wie die Funktion [**bcryptenreregisteredproviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) kann die Funktion [**bcryptqueryproviderregistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) entweder Arbeitsspeicher zuweisen, oder Sie können den Speicher selbst zuweisen. Der Prozess ist für die beiden Funktionen identisch.

 

 



