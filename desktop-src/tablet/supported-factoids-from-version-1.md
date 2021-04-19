---
description: Die Tablet PC-Plattform unterstützt eine Reihe von Faktoiden, die verwendet werden, um die Erkennungsgenauigkeit zu erhöhen.
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: Unterstützte Faktoide aus Version 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad6d08b91a457d38a3eb8543200eb1919eb2bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357079"
---
# <a name="supported-factoids-from-version-1"></a><span data-ttu-id="4ce90-103">Unterstützte Faktoide aus Version 1</span><span class="sxs-lookup"><span data-stu-id="4ce90-103">Supported Factoids from Version 1</span></span>

<span data-ttu-id="4ce90-104">\[Beachten Sie, dass die folgende Beschreibung der in Version 1 des Microsoft Windows XP Tablet PC Edition-SDK (Software Development Kit) unterstützten Faktoids weiterhin von Erkennungs Programmen unterstützt wird. es wird jedoch empfohlen, dass für alle neuen Entwicklungen (für erkenungen von lateinischen Skripts) die in der [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) -Enumeration definierten Werte verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="4ce90-104">\[Note the following description of the factoids supported in version 1 of the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) are still supported by recognizers, but it is recommended that all new development (for recognizers of Latin script) use the values defined in the [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration.\]</span></span>

<span data-ttu-id="4ce90-105">Die Tablet PC-Plattform unterstützt eine Reihe von Faktoiden, die verwendet werden, um die Erkennungsgenauigkeit zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="4ce90-105">The Tablet PC Platform supports a number of factoids that are used to increase recognition accuracy.</span></span> <span data-ttu-id="4ce90-106">Bei der Verwendung von Faktoiden ist es wichtig, dass die erwartete Eingabe genau mit der Definition von "Faktoid" übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="4ce90-106">When using factoids, it is important that the expected input exactly match the definition of the factoid.</span></span> <span data-ttu-id="4ce90-107">Wenn die Eingabe nicht mit der Definition des Faktoid identisch ist, leidet die Erkennungsgenauigkeit.</span><span class="sxs-lookup"><span data-stu-id="4ce90-107">If the input does not match the definition of the factoid, recognition accuracy suffers.</span></span> <span data-ttu-id="4ce90-108">Wenn beispielsweise die **Zahl** "Faktoid" festgelegt ist und der Benutzer Buchstaben eingibt, ist die Erkennungsgenauigkeit für Buchstaben unzureichend.</span><span class="sxs-lookup"><span data-stu-id="4ce90-108">For example, if the **Number** factoid is set and the user enters letters, the recognition accuracy for letters is poor.</span></span>

<span data-ttu-id="4ce90-109">Bestimmte Faktoide, z. b. **e-Mail** und **Ziffern**, sind fast identisch in den Sprachen.</span><span class="sxs-lookup"><span data-stu-id="4ce90-109">Certain factoids, such as **Email** and **Digit**, are almost identical across languages.</span></span> <span data-ttu-id="4ce90-110">Andere Faktoide, z. b. **Telefon** -und **PostalCode**, variieren je nach Sprache.</span><span class="sxs-lookup"><span data-stu-id="4ce90-110">Other factoids, such as **Telephone** and **PostalCode**, vary by language.</span></span> <span data-ttu-id="4ce90-111">Überprüfen Sie das Format der einzelnen Faktoid für die verwendete Sprache.</span><span class="sxs-lookup"><span data-stu-id="4ce90-111">Examine the format of each factoid for the language that you are using.</span></span> <span data-ttu-id="4ce90-112">Eine Liste der Formate für jedes Faktoid in jeder Sprache finden Sie in den Tabellen in den Themen in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="4ce90-112">A list of formats for each factoid in each language can be found in the tables in the topics following this topic.</span></span>

> [!Note]  
> <span data-ttu-id="4ce90-113">Es gibt einen geringfügigen, aber wichtigen Unterschied zwischen den Faktoiden für westliche Sprachen und den Faktoiden für ostasiatische Sprachen.</span><span class="sxs-lookup"><span data-stu-id="4ce90-113">There is a subtle but important distinction between factoids for western languages and factoids for East Asian languages.</span></span> <span data-ttu-id="4ce90-114">Faktoide für westliche Sprachen werden mithilfe von Ausdrücken implementiert, die das gewünschte Ergebnis beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4ce90-114">Factoids for western languages are implemented by using expressions that describe the desired result.</span></span> <span data-ttu-id="4ce90-115">Die Erkennung wird dann so verzerrt, dass Ergebnisse erzeugt werden, die diesem Ausdruck entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4ce90-115">The recognizer is then biased to produce results that match this expression.</span></span> <span data-ttu-id="4ce90-116">Faktoide für ostasiatische Sprachen werden implementiert, indem ein akzeptabler Bereich von Unicode-Zeichen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4ce90-116">Factoids for East Asian languages are implemented by specifying an acceptable range of Unicode characters.</span></span> <span data-ttu-id="4ce90-117">Beispielsweise akzeptiert das **Date** -Faktoid für ostasiatische Sprachen nur Unicode-Zeichen innerhalb eines bestimmten Bereichs.</span><span class="sxs-lookup"><span data-stu-id="4ce90-117">For example, the **Date** factoid for East Asian languages accepts only Unicode characters within a certain range.</span></span>

 

<span data-ttu-id="4ce90-118">Zu den Faktoiden für westliche Sprachen zählen u. a. Faktoide für Englisch (Vereinigtes Königreich), Englisch (USA), Französisch, Deutsch und Spanisch.</span><span class="sxs-lookup"><span data-stu-id="4ce90-118">Factoids for western languages include factoids for English (United Kingdom), English (United States), French, German, and Spanish.</span></span> <span data-ttu-id="4ce90-119">Zu den Faktoiden für ostasiatische Sprachen zählen Faktoide für Chinesisch (vereinfacht), Chinesisch (traditionell), Japanisch und Koreanisch.</span><span class="sxs-lookup"><span data-stu-id="4ce90-119">Factoids for East Asian languages include factoids for Chinese (Simplified), Chinese (Traditional), Japanese, and Korean.</span></span>

<span data-ttu-id="4ce90-120">In den folgenden Abschnitten sind die Formate aufgeführt, die für jedes Faktoid in jeder Sprache unterstützt werden:</span><span class="sxs-lookup"><span data-stu-id="4ce90-120">The following sections show the formats supported for each factoid in each language:</span></span>

-   [<span data-ttu-id="4ce90-121">Sprachen übergreifende Facetten übergreifende Faktoide</span><span class="sxs-lookup"><span data-stu-id="4ce90-121">Factoids Common Across Languages</span></span>](factoids-common-across-languages.md)
-   [<span data-ttu-id="4ce90-122">Faktoide für westliche Sprachen</span><span class="sxs-lookup"><span data-stu-id="4ce90-122">Factoids for Western Languages</span></span>](factoids-for-western-languages.md)
-   [<span data-ttu-id="4ce90-123">Faktoide für ostasiatische Sprachen</span><span class="sxs-lookup"><span data-stu-id="4ce90-123">Factoids for East Asian Languages</span></span>](factoids-for-east-asian-languages.md)

<span data-ttu-id="4ce90-124">Wenn Sie davon ausgehen, dass es sich um Eingaben handelt, die sich von den in den Tabellen in diesen Abschnitten aufgeführten Formaten unterscheiden, verwenden Sie kein Faktoid.</span><span class="sxs-lookup"><span data-stu-id="4ce90-124">If you expect input that is different from the formats listed in the tables in these sections, do not use a factoid.</span></span> <span data-ttu-id="4ce90-125">Außerdem sind die Faktoide in die Erkennung der einzelnen Sprachen integriert.</span><span class="sxs-lookup"><span data-stu-id="4ce90-125">In addition, factoids are built into the recognizer for each language.</span></span> <span data-ttu-id="4ce90-126">Sie können keine Faktoide in einer Sprache verwenden, die eine Erkennung einer anderen Sprache hat.</span><span class="sxs-lookup"><span data-stu-id="4ce90-126">You cannot use factoids from one language with a recognizer from another language.</span></span> <span data-ttu-id="4ce90-127">Beispielsweise können Sie das französische **Telefon** -Faktoid nicht mit einer japanischen Erkennungsfunktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ce90-127">For example, you cannot use the French **Telephone** factoid with a Japanese recognizer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ce90-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4ce90-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ce90-129">**Faktoid-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="4ce90-129">**Factoid Constants**</span></span>](factoid-constants.md)
</dt> <dt>

<span data-ttu-id="4ce90-130">[Microsoft. Ink. Factoid-Klasse](/previous-versions/ms583657(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="4ce90-130">[Microsoft.Ink.Factoid Class](/previous-versions/ms583657(v=vs.100))</span></span>
</dt> </dl>

 

 
