---
description: Aufzählen und Freilassen von Diensten
ms.assetid: 526e51c7-9ff2-4590-b092-172f4942ce8e
title: Aufzählen und Freilassen von Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6472851fbf5f7f84a499d2e9e04804279d397f31452d9617a8868e05cb8ebb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086610"
---
# <a name="enumerating-and-freeing-services"></a>Aufzählen und Freilassen von Diensten

Die ELS-Anwendung ruft die [**MappingGetServices-Funktion**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) auf, um die im Betriebssystem verfügbaren Dienste zu bestimmen. Die -Funktion kann entweder verwendet werden, um alle verfügbaren ELS-Dienste aufzählen oder die Dienste basierend auf von der Anwendung bereitgestellten Suchkriterien zu filtern. Wenn Dienste nicht mehr benötigt werden, ruft die Anwendung [**MappingFreeServices auf.**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)

## <a name="get-all-supported-services"></a>Alle unterstützten Dienste

Dieses Codebeispiel veranschaulicht die Verwendung von [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) und [**MappingFreeServices,**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) um alle verfügbaren Dienste im Betriebssystem zu aufzählen und dann frei zu geben. Hierzu übergibt die Anwendung **NULL für** den *pOptions-Parameter* von **MappingGetServices.**


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



## <a name="get-specific-services"></a>Bestimmte Dienste erhalten

Das nächste Beispiel veranschaulicht die Verwendung von [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) und [**MappingFreeServices,**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) um alle Dienste der Kategorie "Sprachenerkennung" zu aufzählen und dann frei zu geben. Weitere Informationen zu dieser Dienstkategorie finden Sie unter [**Microsoft Sprachenerkennung**](microsoft-language-detection.md).


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

[**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



