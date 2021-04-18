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
# <a name="using-the-cryptography-configuration-features-of-cng"></a><span data-ttu-id="e12b9-103">Verwenden der kryptografiekonfigurationsfeatures von CNG</span><span class="sxs-lookup"><span data-stu-id="e12b9-103">Using the Cryptography Configuration Features of CNG</span></span>

<span data-ttu-id="e12b9-104">Die CNG-API bietet Funktionen zum Auflisten und Abrufen von Informationen zu registrierten Anbietern.</span><span class="sxs-lookup"><span data-stu-id="e12b9-104">The CNG API provides functions to enumerate and obtain information about registered providers.</span></span>

-   [<span data-ttu-id="e12b9-105">Auflisten von Anbietern</span><span class="sxs-lookup"><span data-stu-id="e12b9-105">Enumerating Providers</span></span>](#enumerating-providers)
-   [<span data-ttu-id="e12b9-106">Anbieter Registrierungsinformationen werden erhalten.</span><span class="sxs-lookup"><span data-stu-id="e12b9-106">Getting Provider Registration Information</span></span>](#getting-provider-registration-information)

## <a name="enumerating-providers"></a><span data-ttu-id="e12b9-107">Auflisten von Anbietern</span><span class="sxs-lookup"><span data-stu-id="e12b9-107">Enumerating Providers</span></span>

<span data-ttu-id="e12b9-108">Sie verwenden die Funktion " [**bcryptenumregisteredproviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) ", um die registrierten Anbieter aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="e12b9-108">You use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to enumerate the registered providers.</span></span> <span data-ttu-id="e12b9-109">Die Funktion " **bcryptenreregisteredproviders** " kann auf zwei Arten aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="e12b9-109">The **BCryptEnumRegisteredProviders** function can be called in one of two ways:</span></span>

1.  <span data-ttu-id="e12b9-110">Der erste besteht darin, dass die Funktion " [**bcryptenumschlag registeredproviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) " den Arbeitsspeicher zuweist.</span><span class="sxs-lookup"><span data-stu-id="e12b9-110">The first is to have the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function allocate the memory.</span></span> <span data-ttu-id="e12b9-111">Dies wird erreicht, indem die Adresse eines **null** -Zeigers für den *ppbuffer* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e12b9-111">This is accomplished by passing the address of a **NULL** pointer for the *ppBuffer* parameter.</span></span> <span data-ttu-id="e12b9-112">Mit diesem Code wird der erforderliche Arbeitsspeicher für die Struktur der [**crypt- \_ Anbieter**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) und die zugehörigen Zeichen folgen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e12b9-112">This code will allocate the memory required for the [**CRYPT\_PROVIDERS**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) structure and the associated strings.</span></span> <span data-ttu-id="e12b9-113">Wenn die Funktion " **bcryptenreregisteredproviders** " auf diese Weise verwendet wird, müssen Sie den Arbeitsspeicher freigeben, wenn er nicht mehr benötigt wird, indem Sie *ppbuffer* an die Funktion " [**bcryptfreebuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) " übergeben.</span><span class="sxs-lookup"><span data-stu-id="e12b9-113">When the **BCryptEnumRegisteredProviders** function is used in this manner, you must free the memory when it is no longer needed by passing *ppBuffer* to the [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) function.</span></span>

    <span data-ttu-id="e12b9-114">Im folgenden Beispiel wird gezeigt, wie Sie die Funktion " [**bcryptenumschlag registeredproviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) " verwenden, um den Puffer für Sie zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="e12b9-114">The following example shows how to use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to allocate the buffer for you.</span></span>

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

    

2.  <span data-ttu-id="e12b9-115">Die zweite Methode besteht darin, den erforderlichen Speicher selbst zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="e12b9-115">The second method is to allocate the required memory yourself.</span></span> <span data-ttu-id="e12b9-116">Dies wird erreicht, indem die Funktion " [**bcryptenumschlag registeredproviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) " mit **null** für den Parameter " *ppbuffer* " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e12b9-116">This is accomplished by calling the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function with **NULL** for the *ppBuffer* parameter.</span></span> <span data-ttu-id="e12b9-117">Die Funktion " **bcryptenreregisteredproviders** " wird in den Wert eingefügt, auf den der Parameter " *pcbBuffer* " zeigt, die erforderliche Größe (in Bytes) der [**crypt- \_ Anbieter**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) Struktur und aller Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="e12b9-117">The **BCryptEnumRegisteredProviders** function will place in the value pointed to by the *pcbBuffer* parameter, the required size, in bytes, of the [**CRYPT\_PROVIDERS**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) structure and all strings.</span></span> <span data-ttu-id="e12b9-118">Anschließend weisen Sie den erforderlichen Arbeitsspeicher zu und übergeben die Adresse dieses Puffer Zeigers für den *ppbuffer* -Parameter in einem zweiten Aufrufen der Funktion " **bcryptenumregisteredproviders** ".</span><span class="sxs-lookup"><span data-stu-id="e12b9-118">You then allocate the required memory and pass the address of this buffer pointer for the *ppBuffer* parameter in a second call to the **BCryptEnumRegisteredProviders** function.</span></span>

    <span data-ttu-id="e12b9-119">Im folgenden Beispiel wird gezeigt, wie Sie die Funktion " [**bcryptenumschlag registeredproviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) " verwenden, um Ihren eigenen Puffer zuzuordnen und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e12b9-119">The following example shows how to use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to allocate and use your own buffer.</span></span>

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

    

## <a name="getting-provider-registration-information"></a><span data-ttu-id="e12b9-120">Anbieter Registrierungsinformationen werden erhalten.</span><span class="sxs-lookup"><span data-stu-id="e12b9-120">Getting Provider Registration Information</span></span>

<span data-ttu-id="e12b9-121">Die Funktion " [**bcryptqueryproviderregistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) " dient zum Abrufen zusätzlicher Registrierungs spezifischer Informationen über einen Anbieter.</span><span class="sxs-lookup"><span data-stu-id="e12b9-121">The [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) function is used to obtain additional, registration-specific information about a provider.</span></span> <span data-ttu-id="e12b9-122">Diese Funktion nimmt den Namen des Anbieters, für den Sie Informationen abrufen möchten, den gewünschten Anbieter Modus (Kernel Modus, Benutzermodus oder beides) und den Bezeichner der Anbieter Schnittstelle auf, für den die Registrierungsinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e12b9-122">This function takes the name of the provider that you want to obtain information for, the desired provider mode (kernel mode, user mode, or both), and the identifier of the provider interface to retrieve the registration information for.</span></span> <span data-ttu-id="e12b9-123">Wenn Sie z. b. die Registrierungsinformationen für den Benutzermodus für die Verschlüsselungs Schnittstelle für den Anbieter "Microsoft primitiver Anbieter" abrufen möchten, würden Sie einen ähnlichen Befehl wie den folgenden erstellen.</span><span class="sxs-lookup"><span data-stu-id="e12b9-123">For example, to obtain the user mode registration information for the cipher interface for the "Microsoft Primitive Provider" provider, you would make a call similar to the following.</span></span>


```C++
BCryptQueryProviderRegistration(
    MS_PRIMITIVE_PROVIDER,
    CRYPT_UM,
    BCRYPT_CIPHER_INTERFACE,
    //...
    );

```



<span data-ttu-id="e12b9-124">Wie die Funktion [**bcryptenreregisteredproviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) kann die Funktion [**bcryptqueryproviderregistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) entweder Arbeitsspeicher zuweisen, oder Sie können den Speicher selbst zuweisen.</span><span class="sxs-lookup"><span data-stu-id="e12b9-124">Like the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function, the [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) function can either allocate memory for you or you can allocate the memory yourself.</span></span> <span data-ttu-id="e12b9-125">Der Prozess ist für die beiden Funktionen identisch.</span><span class="sxs-lookup"><span data-stu-id="e12b9-125">The process is the same for the two functions.</span></span>

 

 



