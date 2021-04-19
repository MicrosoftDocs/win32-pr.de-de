---
description: Anfordern von Text Erkennung
ms.assetid: 9db9045d-b289-4c6c-9b17-ddbc2c1d3089
title: Anfordern von Text Erkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db2442cfa1e26185c4c8d882fe71bb178911f4d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348980"
---
# <a name="requesting-text-recognition"></a><span data-ttu-id="0bb35-103">Anfordern von Text Erkennung</span><span class="sxs-lookup"><span data-stu-id="0bb35-103">Requesting Text Recognition</span></span>

<span data-ttu-id="0bb35-104">Die Anwendung ruft die [**mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) -Funktion auf, um die Texterkennung von einem bestimmten Els-Dienst anzufordern.</span><span class="sxs-lookup"><span data-stu-id="0bb35-104">The application calls the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) function to request text recognition from a specific ELS service.</span></span> <span data-ttu-id="0bb35-105">Der Dienst muss in einem vorherigen Befehl von [**mappinggetservices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)ermittelt worden sein, wie in auflisten [**und Freigeben von Diensten**](enumerating-and-freeing-services.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0bb35-105">The service must have been discovered in a previous call to [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), as described in [**Enumerating and Freeing Services**](enumerating-and-freeing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="0bb35-106">Die Plattform kann [**mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) -Aufrufe entweder synchron oder asynchron verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="0bb35-106">The platform can process [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) calls either synchronously or asynchronously.</span></span>

 

<span data-ttu-id="0bb35-107">[**Mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) behandelt die folgenden Text Typen:</span><span class="sxs-lookup"><span data-stu-id="0bb35-107">[**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) handles the following types of text:</span></span>

-   <span data-ttu-id="0bb35-108">Microsoft-Spracherkennung.</span><span class="sxs-lookup"><span data-stu-id="0bb35-108">Microsoft language detection.</span></span> <span data-ttu-id="0bb35-109">UTF-16, normalisierungs Form C, Text, für den die Sprache bestimmt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0bb35-109">UTF-16, normalization form C, text for which to determine the language.</span></span>
-   <span data-ttu-id="0bb35-110">Microsoft-Skript Erkennung.</span><span class="sxs-lookup"><span data-stu-id="0bb35-110">Microsoft script detection.</span></span> <span data-ttu-id="0bb35-111">UTF-16-Text, für den Skript Bereiche bestimmt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0bb35-111">UTF-16 text for which to determine script ranges.</span></span>
-   <span data-ttu-id="0bb35-112">Transliterations Dienste.</span><span class="sxs-lookup"><span data-stu-id="0bb35-112">Transliteration services.</span></span> <span data-ttu-id="0bb35-113">UTF-16-Text, der in Quell Skript geschrieben wurde (Schreiben von System).</span><span class="sxs-lookup"><span data-stu-id="0bb35-113">UTF-16 text written in source script (writing system).</span></span>

## <a name="use-synchronous-text-recognition"></a><span data-ttu-id="0bb35-114">Synchrone Text Erkennung verwenden</span><span class="sxs-lookup"><span data-stu-id="0bb35-114">Use Synchronous Text Recognition</span></span>

<span data-ttu-id="0bb35-115">Dieser Abschnitt enthält Anweisungen für verschiedene Möglichkeiten, eine synchrone Texterkennung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0bb35-115">This section provides instructions for several ways to perform synchronous text recognition.</span></span>

<span data-ttu-id="0bb35-116">**Synchrone Text Erkennung mit Microsoft Sprachenerkennung Service**</span><span class="sxs-lookup"><span data-stu-id="0bb35-116">**Synchronous Text Recognition with Microsoft Language Detection Service**</span></span>

<span data-ttu-id="0bb35-117">Im folgenden Beispiel wird die Verwendung von [**mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) mit dem Microsoft Sprachenerkennung Service veranschaulicht, und alle vom Dienst abgerufenen Ergebnisse werden gedruckt.</span><span class="sxs-lookup"><span data-stu-id="0bb35-117">The following example illustrates the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with the Microsoft Language Detection service, and prints all the results retrieved by the service.</span></span> <span data-ttu-id="0bb35-118">Das Ausgabeformat dieses Dienstanbieter ist eine einzelne [**Mapping- \_ Daten \_ Bereichs**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) Struktur, deren **pData** -Member auf ein Unicode-Zeichen folgen Array mit doppelter NULL-Ausführung zeigt.</span><span class="sxs-lookup"><span data-stu-id="0bb35-118">The output format of this service is a single [**MAPPING\_DATA\_RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) structure with its **pData** member pointing to a Unicode double-null-terminated, registry-formatted array of strings.</span></span> <span data-ttu-id="0bb35-119">Jede Zeichenfolge des Arrays wird auf NULL festgelegt, und eine leere Zeichenfolge wird verwendet, um das Ende des Arrays anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0bb35-119">Every string of the array is null-terminated and an empty string is used to specify the end of the array.</span></span> <span data-ttu-id="0bb35-120">Der Inhalt des Arrays ist nach Zuversicht sortierte Sprachnamen.</span><span class="sxs-lookup"><span data-stu-id="0bb35-120">The contents of the array are language names sorted by confidence.</span></span>


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
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

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
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    WCHAR * p;

    // The return format of the Language Auto-Detection is a
    // double null-terminated registry-formatted array of strings.
    // Every string of the array is null-terminated and there's an
    // empty string specifying the end of the array.
    for (p = (WCHAR *)pBag->prgResultRanges[0].pData; *p; p += wcslen(p) + 1)
    {
        printf("%ws\n", p);
    }
}
```



<span data-ttu-id="0bb35-121">**Synchrone Text Erkennung mit dem Microsoft Script-Erkennungsdienst**</span><span class="sxs-lookup"><span data-stu-id="0bb35-121">**Synchronous Text Recognition with Microsoft Script Detection Service**</span></span>

<span data-ttu-id="0bb35-122">Das nächste Beispiel veranschaulicht die Verwendung von [**mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) mit dem Microsoft Script-Erkennungsdienst und druckt alle abgerufenen Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="0bb35-122">The next example illustrates the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with the Microsoft Script Detection service, and prints all the retrieved results.</span></span> <span data-ttu-id="0bb35-123">Das Ausgabeformat dieses Dienstanbieter ist ein Array von [**Mapping- \_ Daten \_ Bereichs**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) Strukturen, die jeweils Text angeben, der im gleichen Skript geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="0bb35-123">The output format of this service is an array of [**MAPPING\_DATA\_RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) structures, each specifying text written in the same script.</span></span> <span data-ttu-id="0bb35-124">Allgemeine (zyyy) Zeichen werden dem vorherigen Bereich oder dem nächsten Bereich hinzugefügt, wenn der vorherige Bereich nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0bb35-124">Common (Zyyy) characters are added to the previous range, or to the next range if the previous range does not exist.</span></span> <span data-ttu-id="0bb35-125">Der **pData** -Member jeder Struktur verweist auf eine NULL-terminierte Unicode-Zeichenfolge, die den Unicode-Standardnamen des Skripts für den jeweiligen Bereich enthält.</span><span class="sxs-lookup"><span data-stu-id="0bb35-125">The **pData** member of each structure points to a Unicode null-terminated string containing the standard Unicode name of the script for the particular range.</span></span>

> [!Note]  
> <span data-ttu-id="0bb35-126">Ab Windows 7 entspricht der Microsoft Script-Erkennungsdienst Unicode 5,1.</span><span class="sxs-lookup"><span data-stu-id="0bb35-126">As of Windows 7, the Microsoft Script Detection service complies with Unicode 5.1.</span></span>

 


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
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Script Detection GUID to enumerate SD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_SCRIPT_DETECTION;
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
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    DWORD dwRangeIndex;

    for (dwRangeIndex = 0; dwRangeIndex < pBag->dwRangesCount; ++dwRangeIndex)
    {
        if (dwRangeIndex > 0)
        {
            printf("   ----\n");
        }
        printf("Range from %u to %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwStartIndex,
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwEndIndex);
        printf("Data size in WCHARs: %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2);
        printf("\"%ws\"\n", (WCHAR *)pBag->prgResultRanges[dwRangeIndex].pData);
    }
}
```



<span data-ttu-id="0bb35-127">**Synchrone Text Erkennung mit Microsoft Cyrillic to Latin Transliterations Service**</span><span class="sxs-lookup"><span data-stu-id="0bb35-127">**Synchronous Text Recognition with Microsoft Cyrillic to Latin Transliteration Service**</span></span>

<span data-ttu-id="0bb35-128">Das folgende Beispiel veranschaulicht die Verwendung von [**mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) mit dem Microsoft Cyrillic to Latin Transliterations Dienst und druckt die abgerufenen Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="0bb35-128">The following example illustrates the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with the Microsoft Cyrillic to Latin transliteration service, and prints the retrieved results.</span></span> <span data-ttu-id="0bb35-129">Beachten Sie die zwei verschiedenen Möglichkeiten, diesen Dienst aufzulisten, entweder durch die GUID oder durch die Kategorie und das Eingabe Skript.</span><span class="sxs-lookup"><span data-stu-id="0bb35-129">Note the two different ways to enumerate this service, either by GUID or by category and input script.</span></span>

<span data-ttu-id="0bb35-130">Das Ausgabeformat ist für alle verfügbaren Transliterations Dienste identisch.</span><span class="sxs-lookup"><span data-stu-id="0bb35-130">The output format is the same for all available transliteration services.</span></span> <span data-ttu-id="0bb35-131">Dabei handelt es sich um eine einzelne [**Mapping- \_ Daten \_ Bereichs**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) Struktur, deren **pData** -Member auf ein Array von Unicode-Zeichen verweist, das den ursprünglichen Text darstellt, der in das Ausgabe Skript übersetzt wurde, indem nur die Regeln des jeweiligen Transaktions Dienstanbieter angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="0bb35-131">It is a single [**MAPPING\_DATA\_RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) structure with its **pData** member pointing to an array of Unicode characters representing the original text transliterated into the output script by applying only the rules of the specific transliteration service.</span></span> <span data-ttu-id="0bb35-132">Dieser Dienst beendet seine Ausgabe nicht mit NULL, wenn die Eingabe kein abschließendes NULL-Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="0bb35-132">This service does not null-terminate its output if the input does not contain the terminating null character.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT (L"Skip The russian word for 'yes' is transliterated to Latin as '\x0434\x0430'.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices;
    DWORD                   dwServicesCount;
    HRESULT                 hResult;

    // 1. Enumerate by GUID:
    prgServices = NULL;
    dwServicesCount = 0;
    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Use the Cyrl->Latn Transliteration GUID to enumerate only this service:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_TRANSLITERATION_CYRILLIC_TO_LATIN;
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

    printf("--\n");

    // 2. Enumerate by input script and category:
    prgServices = NULL;
    dwServicesCount = 0;
    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    EnumOptions.pszCategory = L"Transliteration";
    EnumOptions.pszInputScript = L"Cyrl";
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
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    // We want the result to be null-terminated for display.
    // That's why we will also pass the input null terminator:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT) + 1, USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    printf("\"%ws\"\n", (WCHAR *)pBag->prgResultRanges[0].pData);
}
```



<span data-ttu-id="0bb35-133">**Synchrone Text Erkennung durch einen-aufrufbefehl für alle verfügbaren Dienste**</span><span class="sxs-lookup"><span data-stu-id="0bb35-133">**Synchronous Text Recognition with a Call to All Available Services**</span></span>

<span data-ttu-id="0bb35-134">Das folgende Beispiel zeigt die Verwendung von [**mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) mit allen verfügbaren Diensten und druckt die abgerufenen Ergebnisse für alle Dienste.</span><span class="sxs-lookup"><span data-stu-id="0bb35-134">The following example shows the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with all available services, and prints the retrieved results for all the services.</span></span> <span data-ttu-id="0bb35-135">Dieses Beispiel veranschaulicht den Betrieb der einzelnen Dienste.</span><span class="sxs-lookup"><span data-stu-id="0bb35-135">This example provides a good illustration of the operation of each service.</span></span> <span data-ttu-id="0bb35-136">Wenn Sie sich die Ausgabe der Beispielanwendung ansehen, ist es einfach herauszufinden, was intern mit den Diensten passiert.</span><span class="sxs-lookup"><span data-stu-id="0bb35-136">By looking at the output of the example application, it is easy to find out what is happening internally with the services.</span></span> <span data-ttu-id="0bb35-137">Dieses Beispiel zeigt auch, dass fast der gesamte Code, der zum aufzurufen eines der Els-Dienste verwendet wird, identisch ist.</span><span class="sxs-lookup"><span data-stu-id="0bb35-137">This example also shows that almost all code used to call any of the ELS services is the same.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    DWORD i;

    // Get all installed ELS services:
    hResult = MappingGetServices(NULL, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service:
            // ... prgServices[i] ...
            if (i > 0)
            {
                printf("--\n");
            }
            hResult = CallMappingRecognizeText(&prgServices[i]);
            if (SUCCEEDED(hResult))
            {
                printf("Calling the service %ws has succeeded!\n",
                    prgServices[i].pszDescription);
            }
            else
            {
                printf("Calling the service %ws has failed, failure = 0x%x!\n",
                    prgServices[i].pszDescription, hResult);
            }
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    DWORD dwRangeIndex;
    DWORD dwDataIndex;
    WCHAR c;

    for (dwRangeIndex = 0; dwRangeIndex < pBag->dwRangesCount; ++dwRangeIndex)
    {
        if (dwRangeIndex > 0)
        {
            printf("   ----\n");
        }
        printf("Range from %u to %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwStartIndex,
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwEndIndex);
        // Currently, we can treat all results as arrays of unicode WCHAR
        // characters, but there can be services in the future
        // that use different formatting, i.e. XML, HTML, etc.
        printf("Data size in WCHARs: %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2);
        printf("\"");
        for (dwDataIndex = 0; dwDataIndex < pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2; ++dwDataIndex)
        {
            c = ((WCHAR *)pBag->prgResultRanges[dwRangeIndex].pData)[dwDataIndex];
            if (c >= 32 && c < 128 && c != '"') printf("%wc", c);
            else printf("#%x", (unsigned)c);
        }
        printf("\"\n");
    }
}

void CallRecognizeText(LPCWSTR Category, LPCWSTR Text)
{
    HRESULT               Result;
    PMAPPING_SERVICE_INFO rgServices;
    DWORD                 ServicesCount;
    MAPPING_ENUM_OPTIONS  options = {sizeof(MAPPING_ENUM_OPTIONS), (LPWSTR) Category, 0};

    Result = MappingGetServices(&options, &rgServices, &ServicesCount);
    if (Result == S_OK && ServicesCount > 0)
    {
        MAPPING_PROPERTY_BAG bag = { sizeof(MAPPING_PROPERTY_BAG), 0};
        Result = MappingRecognizeText(&rgServices[0], Text, wcslen(Text), 0, NULL, &bag);
        if (Result == S_OK)
        {
            MappingFreePropertyBag(&bag);
        }

        MappingFreeServices(rgServices);
    }
}
int _tmain(int argc, _TCHAR* argv[])
{
    CallRecognizeText(L"Language Detection", L"Text to be recognized");
  
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    return 0;
}
```



## <a name="use-asynchronous-text-recognition"></a><span data-ttu-id="0bb35-138">Asynchrone Text Erkennung verwenden</span><span class="sxs-lookup"><span data-stu-id="0bb35-138">Use Asynchronous Text Recognition</span></span>

<span data-ttu-id="0bb35-139">Das folgende Beispiel zeigt die Verwendung von [**mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) für die asynchrone Texterkennung.</span><span class="sxs-lookup"><span data-stu-id="0bb35-139">The following example shows the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) for asynchronous text recognition.</span></span> <span data-ttu-id="0bb35-140">Wenn der Rückruf verwendet wird, muss die Anwendung sicherstellen, dass der Eigenschaften Behälter, der Eingabetext, die Optionen und der Dienst gültig sind, bis die Ausführung des Rückrufs abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0bb35-140">When the callback is used, the application must make sure that the property bag, the input text, the options, and the service are all valid until after the callback has finished executing.</span></span>

<span data-ttu-id="0bb35-141">Die Anwendung muss [**mappingfrepropertybag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) unmittelbar nach dem verbrauchen durch die Rückruffunktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0bb35-141">The application must call [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) immediately after the bag is consumed by the callback function.</span></span> <span data-ttu-id="0bb35-142">Weitere Informationen finden Sie unter [Bereitstellen](providing-callbacks-for-els-services.md)von Rückrufen für Els-Dienste.</span><span class="sxs-lookup"><span data-stu-id="0bb35-142">For more information, see [Providing Callbacks for ELS Services](providing-callbacks-for-els-services.md).</span></span>


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
void RecognizeCallback(PMAPPING_PROPERTY_BAG pBag, LPVOID data, DWORD dwDataSize, HRESULT Result);

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



## <a name="related-topics"></a><span data-ttu-id="0bb35-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0bb35-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bb35-144">Verwenden erweiterter linguistischer Dienste</span><span class="sxs-lookup"><span data-stu-id="0bb35-144">Using Extended Linguistic Services</span></span>](using-extended-linguistic-services.md)
</dt> <dt>

[<span data-ttu-id="0bb35-145">Bereitstellen von Rückrufen für Els-Dienste</span><span class="sxs-lookup"><span data-stu-id="0bb35-145">Providing Callbacks for ELS Services</span></span>](providing-callbacks-for-els-services.md)
</dt> <dt>

[<span data-ttu-id="0bb35-146">**Mappingfrepropertybag**</span><span class="sxs-lookup"><span data-stu-id="0bb35-146">**MappingFreePropertyBag**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag)
</dt> <dt>

[<span data-ttu-id="0bb35-147">**Mappinggetservices**</span><span class="sxs-lookup"><span data-stu-id="0bb35-147">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> <dt>

[<span data-ttu-id="0bb35-148">**Mappingrecognizetext**</span><span class="sxs-lookup"><span data-stu-id="0bb35-148">**MappingRecognizeText**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)
</dt> </dl>

 

 



