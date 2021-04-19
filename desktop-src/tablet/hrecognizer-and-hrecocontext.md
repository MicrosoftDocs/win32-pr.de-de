---
description: Sie verweisen auf eine Handschrifterkennung mit einem herkenzer-Handle und einem Erkennungs Kontext als hrecocontext-handle. Eine Erkennungs Modul-dll (Dynamic-Link Library) kann Erkennungs Tools für mehr als eine Sprache implementieren.
ms.assetid: 23002d02-cf8f-489b-a50f-4a18ac091825
title: Herkenzer und hrecocontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12af1bb5569a22a612f0a3ed667a55aac81da2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345128"
---
# <a name="hrecognizer-and-hrecocontext"></a><span data-ttu-id="00fc1-103">Herkenzer und hrecocontext</span><span class="sxs-lookup"><span data-stu-id="00fc1-103">HRECOGNIZER and HRECOCONTEXT</span></span>

<span data-ttu-id="00fc1-104">Sie verweisen auf eine Handschrifterkennung mit einem [herkenzer](hrecognizer-handle.md) -Handle und einem Erkennungs Kontext als [hrecocontext](hrecocontext-handle.md) -handle.</span><span class="sxs-lookup"><span data-stu-id="00fc1-104">You reference an ink recognizer with an [HRECOGNIZER](hrecognizer-handle.md) handle and a recognizer context as an [HRECOCONTEXT](hrecocontext-handle.md) handle.</span></span>

<span data-ttu-id="00fc1-105">Eine Erkennungs Modul-dll (Dynamic-Link Library) kann Erkennungs Tools für mehr als eine Sprache implementieren.</span><span class="sxs-lookup"><span data-stu-id="00fc1-105">A recognizer dynamic-link library (DLL) can implement recognizers for more than one language.</span></span> <span data-ttu-id="00fc1-106">Wenn dies der Fall ist, wird jede Sprache durch eine CLSID ausgewählt, die beim Erstellen des [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekts in der Anwendung übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="00fc1-106">If so, each language is selected by a CLSID that is passed in when creating the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object in the application.</span></span> <span data-ttu-id="00fc1-107">Außerdem kann eine Erkennungs-DLL mehrere Erkennungs Handles erstellen, wenn Sie geladen wird, eine oder mehrere für jede erkannte Sprache.</span><span class="sxs-lookup"><span data-stu-id="00fc1-107">In addition, a recognizer DLL can create multiple recognizer handles when it is loaded, one or more for each language recognized.</span></span>

<span data-ttu-id="00fc1-108">Ein Erkennungs Kontext wird erstellt, um das Ereignis zu repräsentieren, das ein bestimmtes frei Hand Element erkennt.</span><span class="sxs-lookup"><span data-stu-id="00fc1-108">A recognizer context is created to represent the event of recognizing a specific piece of ink.</span></span> <span data-ttu-id="00fc1-109">Wenn der Kontext erstellt wird, wird das zugehörige Erkennungs Objekt Handle an die Funktion " [**featecontext**](/windows/desktop/api/recapis/nf-recapis-createcontext) " übergeben.</span><span class="sxs-lookup"><span data-stu-id="00fc1-109">When the context is created, the associated recognizer objects handle is passed to the [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) function.</span></span> <span data-ttu-id="00fc1-110">Dadurch wird die Sprache dem Erkennungs Kontext zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="00fc1-110">This associates the language with the recognizer context.</span></span>

<span data-ttu-id="00fc1-111">Ein Erkennungs Kontext kann die Erkennung sämtlicher frei Hand Eingaben im Textkörper einer e-Mail, das frei Handzeichen eines einzelnen Felds innerhalb einer Anwendung oder eine einzelne Textzeile darstellen, die im Tablet PC-Eingabe Panel geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="00fc1-111">A recognizer context may represent the recognition of all the ink in the body of an email, the ink of a single field within an application, or a single line of text written in the Tablet PC Input Panel.</span></span> <span data-ttu-id="00fc1-112">Die Menge an frei Hand Eingaben in einem einzelnen Erkennungs Kontext kann von einem einzelnen Strich zu einer ganzen Seite oder mehr abweichen.</span><span class="sxs-lookup"><span data-stu-id="00fc1-112">The volume of ink in a single recognizer context may vary from a single stroke to a whole page or more.</span></span>

<span data-ttu-id="00fc1-113">Der Erkennungs Kontext wird durch die folgenden Einstellungen definiert:</span><span class="sxs-lookup"><span data-stu-id="00fc1-113">The recognizer context is defined by the settings of:</span></span>

-   <span data-ttu-id="00fc1-114">Das Erkennungs Handbuch.</span><span class="sxs-lookup"><span data-stu-id="00fc1-114">The recognition guide.</span></span>
-   <span data-ttu-id="00fc1-115">Alle Faktoide.</span><span class="sxs-lookup"><span data-stu-id="00fc1-115">Any factoids.</span></span>
-   <span data-ttu-id="00fc1-116">Alle Flags.</span><span class="sxs-lookup"><span data-stu-id="00fc1-116">Any flags.</span></span>
-   <span data-ttu-id="00fc1-117">Der Text Kontext.</span><span class="sxs-lookup"><span data-stu-id="00fc1-117">The text context.</span></span>
-   <span data-ttu-id="00fc1-118">Eine beliebige Wort Liste.</span><span class="sxs-lookup"><span data-stu-id="00fc1-118">Any word list.</span></span>
-   <span data-ttu-id="00fc1-119">Der AutoComplete-Zeichenmodus.</span><span class="sxs-lookup"><span data-stu-id="00fc1-119">The character Autocomplete mode.</span></span>

<span data-ttu-id="00fc1-120">Das Handle für den Erkennungs Kontext wird an alle Funktionen, die diese Einstellungen verwenden, übermittelt.</span><span class="sxs-lookup"><span data-stu-id="00fc1-120">The handle for the recognizer context is passed to all functions that use these settings.</span></span> <span data-ttu-id="00fc1-121">Durch Ändern einer Einstellung wird der Erkennungs Kontext geändert.</span><span class="sxs-lookup"><span data-stu-id="00fc1-121">Changing a setting changes the recognizer context.</span></span>

<span data-ttu-id="00fc1-122">Die Anwendung kann mehrere Kontexte verwenden, um frei Hand Eingaben aus verschiedenen Teilen des Bildschirms zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="00fc1-122">The application may use several contexts to recognize ink from different parts of the screen.</span></span> <span data-ttu-id="00fc1-123">Ein einzelner Kontext kann mehrere Textzeilen erkennen.</span><span class="sxs-lookup"><span data-stu-id="00fc1-123">An individual context can recognize multiple lines of text.</span></span> <span data-ttu-id="00fc1-124">Ein einzelner Kontext kann jedoch zwei Absätze, die nebeneinander geschrieben wurden, nicht gleichzeitig verarbeiten, z. b. mehrere Spalten in einem Zeitungsartikel.</span><span class="sxs-lookup"><span data-stu-id="00fc1-124">However, an individual context cannot process two paragraphs written side by side, such as multiple columns in a newspaper article.</span></span>

<span data-ttu-id="00fc1-125">Um neue frei Hand Eingaben zu erkennen, erstellen Sie einen neuen Kontext.</span><span class="sxs-lookup"><span data-stu-id="00fc1-125">To recognize new ink, create a new context.</span></span> <span data-ttu-id="00fc1-126">Verwenden Sie als Alternative die [**clonecontext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) -Funktion, um eine Kopie eines Kontexts zu erstellen, der keine frei Hand Eingaben und Ergebnisse enthält, oder die [**resetcontext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) -Funktion, um einen Kontext der frei Hand Eingaben und Ergebnisse zu löschen.</span><span class="sxs-lookup"><span data-stu-id="00fc1-126">As an alternative, use the [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) function to make a copy of a context that does not have the ink and results, or the [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) function to clear a context of its ink and results.</span></span> <span data-ttu-id="00fc1-127">Mit diesen Ansätzen kann eine Ink-Anwendung einen Kontext wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="00fc1-127">With these approaches, an ink application can reuse a context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00fc1-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00fc1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00fc1-129">**Setguide-Funktion**</span><span class="sxs-lookup"><span data-stu-id="00fc1-129">**SetGuide Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setguide)
</dt> <dt>

[<span data-ttu-id="00fc1-130">**Getguide-Funktion**</span><span class="sxs-lookup"><span data-stu-id="00fc1-130">**GetGuide Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getguide)
</dt> <dt>

[<span data-ttu-id="00fc1-131">**Setfaktoid-Funktion**</span><span class="sxs-lookup"><span data-stu-id="00fc1-131">**SetFactoid Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setfactoid)
</dt> <dt>

[<span data-ttu-id="00fc1-132">**SetFlags-Funktion**</span><span class="sxs-lookup"><span data-stu-id="00fc1-132">**SetFlags Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setflags)
</dt> <dt>

[<span data-ttu-id="00fc1-133">**"Stenabledunicoderanges"-Funktion**</span><span class="sxs-lookup"><span data-stu-id="00fc1-133">**SetEnabledUnicodeRanges Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)
</dt> <dt>

[<span data-ttu-id="00fc1-134">**GetEnabledUnicodeRanges-Funktion**</span><span class="sxs-lookup"><span data-stu-id="00fc1-134">**GetEnabledUnicodeRanges Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)
</dt> <dt>

[<span data-ttu-id="00fc1-135">**Setcacmode-Funktion**</span><span class="sxs-lookup"><span data-stu-id="00fc1-135">**SetCACMode Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setcacmode)
</dt> <dt>

[<span data-ttu-id="00fc1-136">**Settextcontext-Funktion**</span><span class="sxs-lookup"><span data-stu-id="00fc1-136">**SetTextContext Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-settextcontext)
</dt> <dt>

[<span data-ttu-id="00fc1-137">**Setwordlist-Funktion**</span><span class="sxs-lookup"><span data-stu-id="00fc1-137">**SetWordList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 



