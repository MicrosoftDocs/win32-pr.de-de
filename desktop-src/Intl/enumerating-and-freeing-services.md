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
# <a name="enumerating-and-freeing-services"></a>Auflisten und Freigeben von Diensten

Die Els-Anwendung ruft die [**mappinggetservices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) -Funktion auf, um die Dienste zu bestimmen, die im Betriebssystem verfügbar sind. Die-Funktion kann entweder zum Auflisten aller verfügbaren Els-Dienste oder zum Filtern der Dienste basierend auf den von der Anwendung bereitgestellten Suchkriterien verwendet werden. Wenn Dienste nicht mehr benötigt werden, ruft die Anwendung [**mappingfreeservices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)auf.

## <a name="get-all-supported-services"></a>Alle unterstützten Dienste erhalten

Dieses Codebeispiel veranschaulicht die Verwendung von [**mappinggetservices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) und [**mappingfreeservices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) zum Auflisten und anschließenden freigeben aller verfügbaren Dienste auf dem Betriebssystem. Zu diesem Zweck übergibt die Anwendung für den *poptions* -Parameter von **mappinggetservices** den Wert **null** .


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



## <a name="get-specific-services"></a>Bestimmte Dienste beziehen

Das nächste Beispiel veranschaulicht die Verwendung von [**mappinggetservices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) und [**mappingfreeservices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) zum Auflisten und anschließenden freigeben aller Dienste der Kategorie "Sprachenerkennung". Weitere Informationen zu dieser Dienst Kategorie finden Sie unter [**Microsoft Sprachenerkennung**](microsoft-language-detection.md).


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden erweiterter linguistischer Dienste](using-extended-linguistic-services.md)
</dt> <dt>

[**Mappingfreeservices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[**Mappinggetservices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



