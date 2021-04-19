---
description: Der Dienst für die Spracherkennung von Els heißt Microsoft Sprachenerkennung. Dieser Dienst verwendet von Microsoft patentierte Technologie, um Anwendungen zu ermöglichen, die Sprache zu erkennen, in der bestimmter Text geschrieben wurde.
ms.assetid: 11438e0b-d841-44d0-b68f-77868be4c92f
title: Microsoft-Sprachenerkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b395f6a1a320b66f00d996510b7cafc28b8e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349069"
---
# <a name="microsoft-language-detection"></a><span data-ttu-id="152a4-104">Microsoft-Sprachenerkennung</span><span class="sxs-lookup"><span data-stu-id="152a4-104">Microsoft Language Detection</span></span>

<span data-ttu-id="152a4-105">Der Dienst für die Spracherkennung von Els heißt Microsoft Sprachenerkennung.</span><span class="sxs-lookup"><span data-stu-id="152a4-105">The ELS language detection service is called Microsoft Language Detection.</span></span> <span data-ttu-id="152a4-106">Dieser Dienst verwendet von Microsoft patentierte Technologie, um Anwendungen zu ermöglichen, die Sprache zu erkennen, in der bestimmter Text geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="152a4-106">This service uses Microsoft-patented technology to allow applications to detect the language in which specific text is written.</span></span>

## <a name="input-to-microsoft-language-detection"></a><span data-ttu-id="152a4-107">Eingabe an Microsoft Sprachenerkennung</span><span class="sxs-lookup"><span data-stu-id="152a4-107">Input to Microsoft Language Detection</span></span>

<span data-ttu-id="152a4-108">Die Eingabe für den Microsoft Sprachenerkennung-Dienst ist UTF-16-Text (Normalized Form C).</span><span class="sxs-lookup"><span data-stu-id="152a4-108">The input to the Microsoft Language Detection service is UTF-16 (normalized form C) text.</span></span> <span data-ttu-id="152a4-109">Der Dienst muss die Sprache für diesen Text ermitteln.</span><span class="sxs-lookup"><span data-stu-id="152a4-109">The service has to determine the language for this text.</span></span>

## <a name="output-of-microsoft-language-detection"></a><span data-ttu-id="152a4-110">Ausgabe von Microsoft Sprachenerkennung</span><span class="sxs-lookup"><span data-stu-id="152a4-110">Output of Microsoft Language Detection</span></span>

<span data-ttu-id="152a4-111">Der Microsoft Sprachenerkennung-Dienst ruft eine mit zwei NULL endenden, Registrierungs formatierte UTF-16-Zeichen folgen Auflistungs Sprachen ab, die durch ihre Namen dargestellt werden, getrennt durch Null-Zeichen Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="152a4-111">The Microsoft Language Detection service retrieves a double-null-terminated, registry-formatted UTF-16 string listing languages, represented by their names, separated by null character delimiters.</span></span> <span data-ttu-id="152a4-112">Die Liste ist nach Relevanz sortiert.</span><span class="sxs-lookup"><span data-stu-id="152a4-112">The list is sorted by relevance.</span></span> <span data-ttu-id="152a4-113">In den meisten Sprachen werden neutrale Namen verwendet.</span><span class="sxs-lookup"><span data-stu-id="152a4-113">For most languages, neutral names are used.</span></span> <span data-ttu-id="152a4-114">Für einige, z. b. SR-Cyrl, SR-LATN, zh-Hant und zh-Hans, werden jedoch vollständige Namen verwendet.</span><span class="sxs-lookup"><span data-stu-id="152a4-114">However, for some, for example, sr-Cyrl, sr-Latn, zh-Hant, and zh-Hans, full names are used.</span></span>

## <a name="microsoft-language-detection-operation"></a><span data-ttu-id="152a4-115">Microsoft Sprachenerkennung-Vorgang</span><span class="sxs-lookup"><span data-stu-id="152a4-115">Microsoft Language Detection Operation</span></span>

<span data-ttu-id="152a4-116">Der Microsoft Sprachenerkennung Service überprüft das Unicode-Skript des von der Anwendung bereitgestellten Texts.</span><span class="sxs-lookup"><span data-stu-id="152a4-116">The Microsoft Language Detection service checks the Unicode script of the text provided by the application.</span></span> <span data-ttu-id="152a4-117">Er segmentiert den Text basierend auf den erkannten Skripts und bestimmt dann die Sprache, in der die einzelnen Segmente geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="152a4-117">It segments the text based on the scripts that it detects, and then determines the language in which each segment is written.</span></span> <span data-ttu-id="152a4-118">Wenn ein Skript eine einzelne Sprache anzeigt, ist die Sprache in der Ausgabeliste der Sprachen garantiert vorhanden.</span><span class="sxs-lookup"><span data-stu-id="152a4-118">If a script indicates a single language, the language is guaranteed to be present in the output list of languages.</span></span> <span data-ttu-id="152a4-119">Der Dienst verwendet einen patentierten Algorithmus, um die Relevanz der einzelnen unterstützten Sprachen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="152a4-119">The service uses a patented algorithm to determine the relevance of each supported language.</span></span>

## <a name="microsoft-language-detection-guid"></a><span data-ttu-id="152a4-120">Microsoft Sprachenerkennung-GUID</span><span class="sxs-lookup"><span data-stu-id="152a4-120">Microsoft Language Detection GUID</span></span>

<span data-ttu-id="152a4-121">Die GUID für den Microsoft Sprachenerkennung-Dienst wird in elssrvc. h deklariert, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="152a4-121">The GUID for the Microsoft Language Detection service is declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {CF7E00B1-909B-4d95-A8F4-611F7C377702}
static const GUID ELS_GUID_LANGUAGE_DETECTION =
    { 0xCF7E00B1, 0x909B, 0x4D95, { 0xA8, 0xF4, 0x61, 0x1F, 0x7C, 0x37, 0x77, 0x02 } };
```



## <a name="related-topics"></a><span data-ttu-id="152a4-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="152a4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="152a4-123">Informationen zu erweiterten linguistischen Diensten</span><span class="sxs-lookup"><span data-stu-id="152a4-123">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



