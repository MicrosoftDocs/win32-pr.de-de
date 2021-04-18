---
description: Gebiets Schema- \_ sscripts
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb79f78626e7afb54229d8e0619e26d94250f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347803"
---
# <a name="locale_sscripts"></a><span data-ttu-id="ceb8c-103">Gebiets Schema- \_ sscripts</span><span class="sxs-lookup"><span data-stu-id="ceb8c-103">LOCALE\_SSCRIPTS</span></span>

<span data-ttu-id="ceb8c-104">**Windows Vista und höher:** Eine Zeichenfolge, die eine Liste von Skripts mit der in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html)verwendeten 4-Zeichen-Notation darstellt.</span><span class="sxs-lookup"><span data-stu-id="ceb8c-104">**Windows Vista and later:** A string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="ceb8c-105">Jeder Skript Name besteht aus vier lateinischen Zeichen, und die Liste wird in alphabetischer Reihenfolge mit den einzelnen Namen angeordnet, gefolgt von einem Semikolon.</span><span class="sxs-lookup"><span data-stu-id="ceb8c-105">Each script name consists of four Latin characters and the list is arranged in alphabetical order with each name, including the last, followed by a semicolon.</span></span>

<span data-ttu-id="ceb8c-106">[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) oder [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) kann mit *LCTYPE* , festgelegt auf locale \_ sscripts, als Teil einer Strategie aufgerufen werden, um Sicherheitsprobleme im Zusammenhang mit internationalisierten Domänen Namen (IDNs) zu mindern.</span><span class="sxs-lookup"><span data-stu-id="ceb8c-106">[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) can be called with *LCType* set to LOCALE\_SSCRIPTS as part of a strategy to mitigate security issues related to Internationalized Domain Names (IDNs).</span></span> <span data-ttu-id="ceb8c-107">Im folgenden finden Sie einige Beispiel Werte:</span><span class="sxs-lookup"><span data-stu-id="ceb8c-107">Here are some example values:</span></span>



| <span data-ttu-id="ceb8c-108">Gebietsschema</span><span class="sxs-lookup"><span data-stu-id="ceb8c-108">Locale</span></span>                  | <span data-ttu-id="ceb8c-109">Gebiets Schema-/Sprachname</span><span class="sxs-lookup"><span data-stu-id="ceb8c-109">Locale/language name</span></span> | <span data-ttu-id="ceb8c-110">Wert</span><span class="sxs-lookup"><span data-stu-id="ceb8c-110">Value</span></span>                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb8c-111">Englisch (USA)</span><span class="sxs-lookup"><span data-stu-id="ceb8c-111">English (United States)</span></span> | <span data-ttu-id="ceb8c-112">de-DE</span><span class="sxs-lookup"><span data-stu-id="ceb8c-112">en-US</span></span>                | <span data-ttu-id="ceb8c-113">Latn</span><span class="sxs-lookup"><span data-stu-id="ceb8c-113">Latn;</span></span>                                                                                                  |
| <span data-ttu-id="ceb8c-114">Hindi (Indien)</span><span class="sxs-lookup"><span data-stu-id="ceb8c-114">Hindi (India)</span></span>           | <span data-ttu-id="ceb8c-115">hi-IN</span><span class="sxs-lookup"><span data-stu-id="ceb8c-115">hi-IN</span></span>                | <span data-ttu-id="ceb8c-116">Vas</span><span class="sxs-lookup"><span data-stu-id="ceb8c-116">Deva;</span></span>                                                                                                  |
| <span data-ttu-id="ceb8c-117">Japanisch (Japan)</span><span class="sxs-lookup"><span data-stu-id="ceb8c-117">Japanese (Japan)</span></span>        | <span data-ttu-id="ceb8c-118">ja-JP</span><span class="sxs-lookup"><span data-stu-id="ceb8c-118">ja-JP</span></span>                | <span data-ttu-id="ceb8c-119">**Windows 7 und höher:** Han Hira; Jpan; Betrieben</span><span class="sxs-lookup"><span data-stu-id="ceb8c-119">**Windows 7 and later:** Hani;Hira;Jpan;Kana;</span></span><br/> <span data-ttu-id="ceb8c-120">**Windows Vista:** Han Hira; Betrieben</span><span class="sxs-lookup"><span data-stu-id="ceb8c-120">**Windows Vista:** Hani;Hira;Kana;</span></span><br/> |



 

<span data-ttu-id="ceb8c-121">Ein Verbund Skript Wert enthält nicht das lateinische Skript, es sei denn, er ist ein wesentlicher Bestandteil des für das jeweilige Gebiets Schema verwendeten Schreibsystems.</span><span class="sxs-lookup"><span data-stu-id="ceb8c-121">A compound script value does not include the Latin script unless it is an essential part of the writing system used for the particular locale.</span></span> <span data-ttu-id="ceb8c-122">Lateinische Zeichen werden häufig im Kontext von Gebiets Schemas verwendet, für die Sie nicht nativ sind, z. b. für einen fremden Geschäftsnamen.</span><span class="sxs-lookup"><span data-stu-id="ceb8c-122">Latin characters are often used in the context of locales for which they are not native, for example, for a foreign business name.</span></span> <span data-ttu-id="ceb8c-123">Im obigen Beispiel für Hindi in Indien ist der einzige Skript Wert "Deva" (für "Devanagari"), obwohl auch lateinische Zeichen in Hindi-Text vorkommen können.</span><span class="sxs-lookup"><span data-stu-id="ceb8c-123">In the example above for Hindi in India, the only script value is "Deva" (for "Devanagari"), although Latin characters can also appear in Hindi text.</span></span> <span data-ttu-id="ceb8c-124">Die Funktion " [verifyscripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) " weist ein spezielles Flag auf, um diesen Fall zu beheben.</span><span class="sxs-lookup"><span data-stu-id="ceb8c-124">The [VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) function has a special flag to address this case.</span></span>

 

 




