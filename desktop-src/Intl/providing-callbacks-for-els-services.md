---
description: Bereitstellen von Rückrufen für Els-Dienste
ms.assetid: 48609c55-9e82-4407-ae28-41b07b1e1161
title: Bereitstellen von Rückrufen für Els-Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d22091f666649aab43c66f3d532f8e8f971d49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215365"
---
# <a name="providing-callbacks-for-els-services"></a><span data-ttu-id="c6494-103">Bereitstellen von Rückrufen für Els-Dienste</span><span class="sxs-lookup"><span data-stu-id="c6494-103">Providing Callbacks for ELS Services</span></span>

<span data-ttu-id="c6494-104">Wenn Ihre Anwendung asynchrone Vorgänge für die Texterkennung verwendet, muss Sie eine Rückruffunktion für den zu verwendenden Els-Dienst bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c6494-104">If your application is using asynchronous operations for text recognition, it must provide a callback function for the ELS service to use.</span></span> <span data-ttu-id="c6494-105">Die Rückruffunktion basiert auf dem Prototyp [**mappingcallbackproc**](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc) .</span><span class="sxs-lookup"><span data-stu-id="c6494-105">The callback function is based on the [**MappingCallbackProc**](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc) prototype.</span></span>

<span data-ttu-id="c6494-106">Im Thema [anfordern von Texterkennung](requesting-text-recognition.md) wird beschrieben, wie Ihre Anwendung die asynchrone Texterkennung von einem Els-Dienst anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="c6494-106">The [Requesting Text Recognition](requesting-text-recognition.md) topic describes how your application can request asynchronous text recognition from an ELS service.</span></span> <span data-ttu-id="c6494-107">Das folgende Beispiel zeigt eine Anwendung, die einen asynchronen Rückruf von [**mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)ausführt.</span><span class="sxs-lookup"><span data-stu-id="c6494-107">The following example shows an application that makes an asynchronous call to [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext).</span></span> <span data-ttu-id="c6494-108">Die Rückruffunktion für die Texterkennung heißt " **erkennzecallback**".</span><span class="sxs-lookup"><span data-stu-id="c6494-108">The callback function for text recognition is called **RecognizeCallback**.</span></span> <span data-ttu-id="c6494-109">Beachten Sie, dass die Anwendung sicherstellen muss, dass der Eigenschaften Behälter, der Eingabetext, die Optionen und der Dienst gültig sind, bis die Ausführung der Rückruffunktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c6494-109">Note that the application must make sure that the property bag, the input text, the options, and the service are all valid until after the callback function has finished executing.</span></span> <span data-ttu-id="c6494-110">Darüber hinaus muss die Anwendung sicherstellen, dass [**mappingfrepropertybag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) unmittelbar nach dem verbrauchen durch die Rückruffunktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c6494-110">Additionally, the application must ensure that [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) is called immediately after the bag is consumed by the callback function.</span></span>

> [!Note]  
> <span data-ttu-id="c6494-111">Es könnte ratsam sein, dass Ihre Anwendung die Rückruffunktion verwendet, um die Ressourcen freizugeben, nachdem Sie sie verarbeitet oder kopiert haben.</span><span class="sxs-lookup"><span data-stu-id="c6494-111">It might be a good idea for your application to use the callback function to free the resources after it has finished processing or copying them.</span></span>

 


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



## <a name="related-topics"></a><span data-ttu-id="c6494-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c6494-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6494-113">Verwenden erweiterter linguistischer Dienste</span><span class="sxs-lookup"><span data-stu-id="c6494-113">Using Extended Linguistic Services</span></span>](using-extended-linguistic-services.md)
</dt> <dt>

[<span data-ttu-id="c6494-114">Anfordern von Text Erkennung</span><span class="sxs-lookup"><span data-stu-id="c6494-114">Requesting Text Recognition</span></span>](requesting-text-recognition.md)
</dt> <dt>

[<span data-ttu-id="c6494-115">**Mappingcallbackproc**</span><span class="sxs-lookup"><span data-stu-id="c6494-115">**MappingCallbackProc**</span></span>](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)
</dt> <dt>

[<span data-ttu-id="c6494-116">**Mappingfrepropertybag**</span><span class="sxs-lookup"><span data-stu-id="c6494-116">**MappingFreePropertyBag**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag)
</dt> <dt>

[<span data-ttu-id="c6494-117">**Mappingrecognizetext**</span><span class="sxs-lookup"><span data-stu-id="c6494-117">**MappingRecognizeText**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)
</dt> </dl>

 

 



