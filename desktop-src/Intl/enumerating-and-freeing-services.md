---
description: Auflisten und Freigeben von Diensten
ms.assetid: 526e51c7-9ff2-4590-b092-172f4942ce8e
title: Auflisten und Freigeben von Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859abe590ccaf2f71df676d5989778d5b391be57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368995"
---
# <a name="enumerating-and-freeing-services"></a><span data-ttu-id="1b5f8-103">Auflisten und Freigeben von Diensten</span><span class="sxs-lookup"><span data-stu-id="1b5f8-103">Enumerating and Freeing Services</span></span>

<span data-ttu-id="1b5f8-104">Die Els-Anwendung ruft die [**mappinggetservices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) -Funktion auf, um die Dienste zu bestimmen, die im Betriebssystem verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-104">The ELS application calls the [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) function to determine the services that are available on the operating system.</span></span> <span data-ttu-id="1b5f8-105">Die-Funktion kann entweder zum Auflisten aller verfügbaren Els-Dienste oder zum Filtern der Dienste basierend auf den von der Anwendung bereitgestellten Suchkriterien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-105">The function can be used either to enumerate all available ELS services, or to filter the services based on application-provided search criteria.</span></span> <span data-ttu-id="1b5f8-106">Wenn Dienste nicht mehr benötigt werden, ruft die Anwendung [**mappingfreeservices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)auf.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-106">When services are no longer needed, the application calls [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).</span></span>

## <a name="get-all-supported-services"></a><span data-ttu-id="1b5f8-107">Alle unterstützten Dienste erhalten</span><span class="sxs-lookup"><span data-stu-id="1b5f8-107">Get All Supported Services</span></span>

<span data-ttu-id="1b5f8-108">Dieses Codebeispiel veranschaulicht die Verwendung von [**mappinggetservices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) und [**mappingfreeservices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) zum Auflisten und anschließenden freigeben aller verfügbaren Dienste auf dem Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-108">This code example illustrates the use of [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) and [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) to enumerate and then free all available services on the operating system.</span></span> <span data-ttu-id="1b5f8-109">Zu diesem Zweck übergibt die Anwendung für den *poptions* -Parameter von **mappinggetservices** den Wert **null** .</span><span class="sxs-lookup"><span data-stu-id="1b5f8-109">To do this, the application passes **NULL** for the *pOptions* parameter of **MappingGetServices**.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

int __cdecl main()
{
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 Result;
    DWORD                   i;

    // Get all installed ELS services.
    Result = MappingGetServices(NULL, &prgServices, &dwServicesCount);

    if (SUCCEEDED(Result))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service.
            // ... prgServices[i] ...
            printf_s("Service: %ws, category: %ws\n",
                prgServices[i].pszDescription, prgServices[i].pszCategory);
        }
        MappingFreeServices(prgServices);
    }
    return 0;
}
```



## <a name="get-specific-services"></a><span data-ttu-id="1b5f8-110">Bestimmte Dienste beziehen</span><span class="sxs-lookup"><span data-stu-id="1b5f8-110">Get Specific Services</span></span>

<span data-ttu-id="1b5f8-111">Das nächste Beispiel veranschaulicht die Verwendung von [**mappinggetservices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) und [**mappingfreeservices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) zum Auflisten und anschließenden freigeben aller Dienste der Kategorie "Sprachenerkennung".</span><span class="sxs-lookup"><span data-stu-id="1b5f8-111">The next example illustrates the use of [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) and [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) to enumerate and then free all services of category "Language Detection".</span></span> <span data-ttu-id="1b5f8-112">Weitere Informationen zu dieser Dienst Kategorie finden Sie unter [**Microsoft Sprachenerkennung**](microsoft-language-detection.md).</span><span class="sxs-lookup"><span data-stu-id="1b5f8-112">For more information about this service category, see [**Microsoft Language Detection**](microsoft-language-detection.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 Result;
    DWORD                   i;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);

    // Use the Language Auto-Detection category to enumerate
    // all language detection services.
    EnumOptions.pszCategory = L"Language Detection";

    // Execute the enumeration:
    Result = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(Result))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service.
            // ... prgServices[i] ...
            printf_s("Service: %ws, category: %ws\n",
                prgServices[i].pszDescription, prgServices[i].pszCategory);
        }
        MappingFreeServices(prgServices);
    }
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="1b5f8-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1b5f8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b5f8-114">Verwenden erweiterter linguistischer Dienste</span><span class="sxs-lookup"><span data-stu-id="1b5f8-114">Using Extended Linguistic Services</span></span>](using-extended-linguistic-services.md)
</dt> <dt>

[<span data-ttu-id="1b5f8-115">**Mappingfreeservices**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-115">**MappingFreeServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[<span data-ttu-id="1b5f8-116">**Mappinggetservices**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-116">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



