---
description: Bereitstellen von Rückrufen für ELS-Dienste
ms.assetid: 48609c55-9e82-4407-ae28-41b07b1e1161
title: Bereitstellen von Rückrufen für ELS-Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec6704bcf11d2619431aa1b855cd711f82e75e71fc4a762c0e8cf2cb35082341
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040490"
---
# <a name="providing-callbacks-for-els-services"></a>Bereitstellen von Rückrufen für ELS-Dienste

Wenn Ihre Anwendung asynchrone Vorgänge für die Texterkennung verwendet, muss sie eine Rückruffunktion bereitstellen, die der ELS-Dienst verwenden kann. Die Rückruffunktion basiert auf dem [**MappingCallbackProc-Prototyp.**](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)

Im Thema [Anfordern der Texterkennung](requesting-text-recognition.md) wird beschrieben, wie Ihre Anwendung asynchrone Texterkennung von einem ELS-Dienst anfordern kann. Das folgende Beispiel zeigt eine Anwendung, die [**mappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)asynchron aufruft. Die Rückruffunktion für die Texterkennung heißt **RecognizeCallback.** Beachten Sie, dass die Anwendung sicherstellen muss, dass der Eigenschaftenbehälter, der Eingabetext, die Optionen und der Dienst alle gültig sind, bis die Rückruffunktion ausgeführt wurde. Darüber hinaus muss die Anwendung sicherstellen, dass [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) sofort aufgerufen wird, nachdem der Behälter von der Rückruffunktion verbraucht wurde.

> [!Note]  
> Es kann eine gute Idee sein, dass Ihre Anwendung die Rückruffunktion verwendet, um die Ressourcen frei zu machen, nachdem sie die Verarbeitung abgeschlossen oder sie kopiert hat.

 


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void RecognizeCallback(
     PMAPPING_PROPERTY_BAG pBag, 
     LPVOID data, DWORD dwDataSize, 
     HRESULT Result); 

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Language Auto-Detection GUID to enumerate LAD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_LANGUAGE_DETECTION;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG    bag;
    MAPPING_OPTIONS         Options;
    HRESULT                 hResult;
    HANDLE                  SyncEvent;
    DWORD                   dwWaitResult;

    SyncEvent = CreateEvent(NULL, FALSE, FALSE, NULL);

    if (SyncEvent == NULL)
    {
        hResult = E_FAIL;
    }
    else
    {
        ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
        bag.Size = sizeof (MAPPING_PROPERTY_BAG);

        ZeroMemory(&Options, sizeof (MAPPING_OPTIONS));
        Options.Size = sizeof (MAPPING_OPTIONS);
        Options.pfnRecognizeCallback = (PFN_MAPPINGCALLBACKPROC)RecognizeCallback;
        Options.pRecognizeCallerData = &SyncEvent;
        Options.dwRecognizeCallerDataSize = sizeof (HANDLE);

        // MappingRecognizeText's dwIndex parameter specifies the first
        // index inside the text from where the recognition should start.
        // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
        // of the input string.
        hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, &Options, &bag);
        if (SUCCEEDED(hResult))
        {
            // We are using an event to synchronize our waiting for the call to end,
            // because some objects have to be valid till the end of the callback call:
            // - the input text
            // - the property bag
            // - the options
            // - the service
            dwWaitResult = WaitForSingleObject(SyncEvent, INFINITE);
            if (dwWaitResult != WAIT_OBJECT_0)
            {
                hResult = E_FAIL;
            }
        }
        CloseHandle(SyncEvent);
    }
    return hResult;
}

void RecognizeCallback(PMAPPING_PROPERTY_BAG pBag, LPVOID data, DWORD dwDataSize, HRESULT Result)
{
    HANDLE SyncEvent;
    WCHAR * p;

    UNREFERENCED_PARAMETER(dwDataSize);

    if (SUCCEEDED(Result))
    {
        for (p = (WCHAR *)pBag->prgResultRanges[0].pData; *p; p += wcslen(p) + 1)
        {
            printf("%ws\n", p);
        }
        MappingFreePropertyBag(pBag);
    }

    SyncEvent = *((HANDLE *)data);
    SetEvent(SyncEvent);
} 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden erweiterter linguistischer Dienste](using-extended-linguistic-services.md)
</dt> <dt>

[Anfordern der Texterkennung](requesting-text-recognition.md)
</dt> <dt>

[**MappingCallbackProc**](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)
</dt> <dt>

[**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag)
</dt> <dt>

[**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)
</dt> </dl>

 

 



