---
description: Die Els-Transliterations Dienste ordnen UTF-16-Text von einem Schreibsystem einem anderen Schreibsystem zu.
ms.assetid: 32e46c52-5c3c-4e22-8f4e-05286ee213ba
title: Transliterations Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc00b96d56e6b05e70b352c81da0280e9ef35043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131736"
---
# <a name="transliteration-services"></a><span data-ttu-id="c4742-103">Transliterations Dienste</span><span class="sxs-lookup"><span data-stu-id="c4742-103">Transliteration Services</span></span>

<span data-ttu-id="c4742-104">Die Els-Transliterations Dienste ordnen UTF-16-Text von einem Schreibsystem einem anderen Schreibsystem zu.</span><span class="sxs-lookup"><span data-stu-id="c4742-104">The ELS transliteration services map UTF-16 text from one writing system to another writing system.</span></span> <span data-ttu-id="c4742-105">Bei jedem Dienst handelt es sich um Daten, die auf einen bestimmten Satz von Eingabe-und Ausgabe-Unicode-Skripts angewendet werden, und die tatsächliche Transliterierung ist intern für die Els-Plattform</span><span class="sxs-lookup"><span data-stu-id="c4742-105">Each service is really data applying to a specific set of input and output Unicode scripts, and the actual transliteration is internal to the ELS platform.</span></span> <span data-ttu-id="c4742-106">Die Anwendung kann optional die verfügbaren Dienste für bestimmte Eingabe-und Ausgabe Skripts auflisten und den erforderlichen Dienst auswählen.</span><span class="sxs-lookup"><span data-stu-id="c4742-106">The application can optionally enumerate the available services for specific input and output scripts and select the service that it requires.</span></span>

<span data-ttu-id="c4742-107">Die Plattform verwaltet die Metadaten für die Els-Transliterations Dienste.</span><span class="sxs-lookup"><span data-stu-id="c4742-107">The platform maintains metadata for the ELS transliteration services.</span></span> <span data-ttu-id="c4742-108">Die Metadaten für jeden Dienststellen eine Beschreibung des Dienes bereit und listet die Eingabe-und Ausgabe Skripts auf, die der Dienst unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c4742-108">Metadata for each service provides a description of the service and lists the input and output scripts that the service supports.</span></span> <span data-ttu-id="c4742-109">Die Metadaten werden durch eine [**Mapping \_ Service \_ Info**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) -Struktur dargestellt, die von der [**mappinggetservices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) -Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c4742-109">The metadata is represented by a [**MAPPING\_SERVICE\_INFO**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) structure retrieved by the [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) function.</span></span>

## <a name="input-to-a-transliteration-service"></a><span data-ttu-id="c4742-110">Eingabe in einen Transliterations Dienst</span><span class="sxs-lookup"><span data-stu-id="c4742-110">Input to a Transliteration Service</span></span>

<span data-ttu-id="c4742-111">Die Eingabe für einen Transliterations Dienst ist UTF-16-Text in einem Schreibsystem.</span><span class="sxs-lookup"><span data-stu-id="c4742-111">The input to a transliteration service is UTF-16 text in one writing system.</span></span>

## <a name="output-of-a-transliteration-service"></a><span data-ttu-id="c4742-112">Ausgabe eines-Transaktions Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c4742-112">Output of a Transliteration Service</span></span>

<span data-ttu-id="c4742-113">Die Ausgabe eines-Transaktions Dienstanbieter ist UTF-16-Text, der einem zweiten Schreibsystem zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c4742-113">The output of a transliteration service is UTF-16 text mapped to a second writing system.</span></span> <span data-ttu-id="c4742-114">Wenn keine passende Transaktions Zuordnung für einen bestimmten Teil des Eingabe Texts verfügbar ist, bleibt der Block unverändert.</span><span class="sxs-lookup"><span data-stu-id="c4742-114">If no appropriate transliteration mapping is available for any given chunk of the input text, the chunk remains unchanged.</span></span>

## <a name="transliteration-service-operation"></a><span data-ttu-id="c4742-115">Vorgang für den Transaktions Dienst</span><span class="sxs-lookup"><span data-stu-id="c4742-115">Transliteration Service Operation</span></span>

<span data-ttu-id="c4742-116">Ein-Transaktions Dienst ordnet Unicode-Text von einem Eingabe Skript nach Bedarf einem Ausgabe Skript zu.</span><span class="sxs-lookup"><span data-stu-id="c4742-116">A transliteration service maps Unicode text from an input script to an output script, character by character or term by term, as appropriate.</span></span> <span data-ttu-id="c4742-117">Die Anwendung kann den spezifischen zu berücksichtigenden Transaktions Dienst abrufen, indem Sie beim Aufrufen von [**mappinggetservices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)Eingabe-und Ausgabe Skripts angibt oder die Dienst-GUID bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c4742-117">The application can choose to obtain the specific transliteration service of interest by specifying input and output scripts when calling [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), or by providing the service GUID.</span></span> <span data-ttu-id="c4742-118">Eine weitere Option für die Anwendung besteht darin, alle verfügbaren Transaktionsdienste aufzulisten, indem die Dienst Kategorie "Transliterierung" angegeben wird, wenn **mappinggetservices** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c4742-118">Another option for the application is to enumerate all available transliteration services by specifying the service category "Transliteration" when calling **MappingGetServices**.</span></span> <span data-ttu-id="c4742-119">In diesem Fall ruft die Anwendung jeden Dienst auf und vergleicht die Ergebnisse mit dem ursprünglichen Text, um festzustellen, ob die Ergebnisse durch den Vorgang eines bestimmten dienstanens geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="c4742-119">In this case, the application calls each service and compares the results with the original text to see if the results have been changed by the operation of a particular service.</span></span>

<span data-ttu-id="c4742-120">Die Anwendung kann die Texterkennung für einen Els-Transaktions Dienst mit einem Rückruf von [**mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)anfordern.</span><span class="sxs-lookup"><span data-stu-id="c4742-120">The application can request text recognition for an ELS transliteration service with a call to [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext).</span></span> <span data-ttu-id="c4742-121">Beim Empfang der Anforderung ordnet der-Transaktions Dienst einen Puffer zu, der die Transaktionsdaten enthält, und führt dann eine Texterkennung für jeden Codepunkt in der von der Anwendung bereitgestellten Eingabe Zeichenfolge aus.</span><span class="sxs-lookup"><span data-stu-id="c4742-121">When it receives the request, the transliteration service allocates a buffer to contain the transliterated data, and then performs text recognition for each code point in the input string supplied by the application.</span></span>

> [!Note]  
> <span data-ttu-id="c4742-122">Der ursprüngliche Text und der transliterierte Text können eine unterschiedliche Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c4742-122">The original text and the transliterated text might have different lengths.</span></span>

 

## <a name="transliteration-service-guids"></a><span data-ttu-id="c4742-123">Dienst-GUIDs für Transliterationen</span><span class="sxs-lookup"><span data-stu-id="c4742-123">Transliteration Service GUIDs</span></span>

<span data-ttu-id="c4742-124">Die GUIDs für die-Transliterations Dienste werden in elssrvc. h deklariert, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c4742-124">The GUIDs for the transliteration services are declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {A3A8333B-F4FC-42f6-A0C4-0462FE7317CB}
static const GUID ELS_GUID_TRANSLITERATION_HANT_TO_HANS =
    { 0xA3A8333B, 0xF4FC, 0x42f6, { 0xA0, 0xC4, 0x04, 0x62, 0xFE, 0x73, 0x17, 0xCB } };

// {3CACCDC8-5590-42dc-9A7B-B5A6B5B3B63B}
static const GUID ELS_GUID_TRANSLITERATION_HANS_TO_HANT =
    { 0x3CACCDC8, 0x5590, 0x42dc, { 0x9A, 0x7B, 0xB5, 0xA6, 0xB5, 0xB3, 0xB6, 0x3B } };

// {D8B983B1-F8BF-4a2b-BCD5-5B5EA20613E1}
static const GUID ELS_GUID_TRANSLITERATION_MALAYALAM_TO_LATIN =
    { 0xD8B983B1, 0xF8BF, 0x4a2b, { 0xBC, 0xD5, 0x5B, 0x5E, 0xA2, 0x06, 0x13, 0xE1 } };

// {C4A4DCFE-2661-4d02-9835-F48187109803}
static const GUID ELS_GUID_TRANSLITERATION_DEVANAGARI_TO_LATIN =
    { 0xC4A4DCFE, 0x2661, 0x4d02, { 0x98, 0x35, 0xF4, 0x81, 0x87, 0x10, 0x98, 0x03 } };

// {3DD12A98-5AFD-4903-A13F-E17E6C0BFE01}
static const GUID ELS_GUID_TRANSLITERATION_CYRILLIC_TO_LATIN =
    { 0x3DD12A98, 0x5AFD, 0x4903, { 0xA1, 0x3F, 0xE1, 0x7E, 0x6C, 0x0B, 0xFE, 0x01 } };

// {F4DFD825-91A4-489f-855E-9AD9BEE55727}
static const GUID ELS_GUID_TRANSLITERATION_BENGALI_TO_LATIN =
    { 0xF4DFD825, 0x91A4, 0x489f, { 0x85, 0x5E, 0x9A, 0xD9, 0xBE, 0xE5, 0x57, 0x27 } };
```



## <a name="related-topics"></a><span data-ttu-id="c4742-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4742-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4742-126">Informationen zu erweiterten linguistischen Diensten</span><span class="sxs-lookup"><span data-stu-id="c4742-126">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



