---
title: Animations Design
description: Animations Design
ms.assetid: 8812e4cc-9062-4c65-81ef-229bd29534cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7d6cf86cfe115ec209fb305f0ae017951bd7f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947597"
---
# <a name="animation-design"></a><span data-ttu-id="c115b-103">Animations Design</span><span class="sxs-lookup"><span data-stu-id="c115b-103">Animation Design</span></span>

<span data-ttu-id="c115b-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="c115b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

### <a name="image-design"></a><span data-ttu-id="c115b-105">Bild Entwurf</span><span class="sxs-lookup"><span data-stu-id="c115b-105">Image Design</span></span>

<span data-ttu-id="c115b-106">Verwenden Sie die Microsoft Office Palette beim Entwerfen der Zeichen, um potenzielle Probleme bei der palettenrealisierung zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="c115b-106">Use the Microsoft Office Palette when designing your characters to minimize any potential palette realization issues.</span></span> <span data-ttu-id="c115b-107">Wählen Sie eine Transparenz Farbe aus, die den Farben ähnelt, die Sie in Ihrem Dokument verwenden.</span><span class="sxs-lookup"><span data-stu-id="c115b-107">Avoid selecting a transparency color that is similar to the colors that you use in your document.</span></span>

### <a name="sounds"></a><span data-ttu-id="c115b-108">Sounds</span><span class="sxs-lookup"><span data-stu-id="c115b-108">Sounds</span></span>

<span data-ttu-id="c115b-109">Mit dem Microsoft-Agent können Sie Sounds in ihren Animationen abspielen.</span><span class="sxs-lookup"><span data-stu-id="c115b-109">Microsoft Agent enables you to play sounds in your animations.</span></span> <span data-ttu-id="c115b-110">Es wird empfohlen, keine Sounds für Ihre nicht im **Leerlauf** befindlichen Animationen einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c115b-110">We recommend you do not include sounds for your **Idle** animations.</span></span> <span data-ttu-id="c115b-111">Dies ist also keine Verzögerung in der Mitte der Animation, wenn der Agent die System-Multimedia-DLL laden muss.</span><span class="sxs-lookup"><span data-stu-id="c115b-111">This is so there won't be a delay in the middle of the animation, if Agent has to load the system multimedia DLL.</span></span>

### <a name="frame-size"></a><span data-ttu-id="c115b-112">Frame Größe</span><span class="sxs-lookup"><span data-stu-id="c115b-112">Frame Size</span></span>

<span data-ttu-id="c115b-113">Typische Office-Assistenten sind 123 x 93 Pixel.</span><span class="sxs-lookup"><span data-stu-id="c115b-113">Typical Office Assistants are 123 x 93 pixels.</span></span> <span data-ttu-id="c115b-114">Obwohl Sie Zeichen anderer Größen erstellen können, werden Sie im Assistant Gallery auf 123 x 93 skaliert.</span><span class="sxs-lookup"><span data-stu-id="c115b-114">While you can create characters of other sizes, they will be scaled to 123 x 93 in the Assistant Gallery.</span></span>

### <a name="frame-transition"></a><span data-ttu-id="c115b-115">Frame Übergang</span><span class="sxs-lookup"><span data-stu-id="c115b-115">Frame Transition</span></span>

<span data-ttu-id="c115b-116">Alle Animationen außer " **Goodbye**", " **Gruß**", " **anzeigen** " und " **Ausblenden** " sollten mit der restpose-Animation beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="c115b-116">All animations except for **Goodbye**, **Greeting**, **Show** and **Hide** should begin and end with the RestPose animation.</span></span> <span data-ttu-id="c115b-117">Microsoft Office keine expliziten **Rückgabe Animationen wieder** gibt, sollten Sie Sie nicht definieren.</span><span class="sxs-lookup"><span data-stu-id="c115b-117">Microsoft Office does not play explicit **Return** animations, so you should not define them.</span></span> <span data-ttu-id="c115b-118">Alle Animationen sollten auch Exit-Verzweigungen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c115b-118">All animations should also have Exit Branching.</span></span> <span data-ttu-id="c115b-119">Durch das Beenden der Verzweigung können wir die aktuelle Animation vor der nächsten Animation "beeilen und Fertigstellen".</span><span class="sxs-lookup"><span data-stu-id="c115b-119">Exit branching enables us to 'hurry up and finish' the current animation before we call the next animation.</span></span> <span data-ttu-id="c115b-120">Wenn Sie keine Beendigungs Verzweigung angeben, ist der Übergang zwischen Animationen möglicherweise ruckartig.</span><span class="sxs-lookup"><span data-stu-id="c115b-120">If you don't supply Exit Branching, the transition between animations may be jerky.</span></span>

### <a name="character-properties"></a><span data-ttu-id="c115b-121">Zeichen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c115b-121">Character Properties</span></span>

<span data-ttu-id="c115b-122">Mit dem Microsoft-Agent können Sie den [**Namen**](name-property.md), die [**Beschreibung**](description-property.md) und die [**ExtraData**](extradata-property.md) -Eigenschaften für den Zeichensatz festlegen.</span><span class="sxs-lookup"><span data-stu-id="c115b-122">Microsoft Agent enables you to set the character's [**Name**](name-property.md), [**Description**](description-property.md) and [**ExtraData**](extradata-property.md) properties.</span></span> <span data-ttu-id="c115b-123">Microsoft Office verwendet das **ExtraData** -Feld, um einen oder mehrere Einführungs Ausdrücke und Erinnerungs Ausdrücke zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c115b-123">Microsoft Office uses the **ExtraData** field to hold to one or more Introduction Phrases and Reminder Phrases.</span></span> <span data-ttu-id="c115b-124">Microsoft Office wählt die anderen Einführungs Ausdrücke aus, die in die Sprechblase im Assistant Gallery eingefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c115b-124">Microsoft Office picks from the other Introduction Phrases to put in the speech balloon in the Assistant Gallery.</span></span> <span data-ttu-id="c115b-125">Wir verwenden die Erinnerungs Ausdrücke, wenn Sie eine Erinnerung aus Outlook erhalten.</span><span class="sxs-lookup"><span data-stu-id="c115b-125">We use the Reminder Phrases when you receive a reminder from Outlook.</span></span>

<span data-ttu-id="c115b-126">Das Feld " [**ExtraData**](extradata-property.md) " ist wie folgt formatiert:</span><span class="sxs-lookup"><span data-stu-id="c115b-126">The [**ExtraData**](extradata-property.md) field is formatted as follows:</span></span>

<span data-ttu-id="c115b-127">IntroPhrase1~~IntroPhrase2~~IntroPhrase3 ^ ^ ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3</span><span class="sxs-lookup"><span data-stu-id="c115b-127">IntroPhrase1~~IntroPhrase2~~IntroPhrase3^^ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3</span></span>

<span data-ttu-id="c115b-128">Intro-Ausdrücke werden durch ein paar aus Tildezeichen (~) getrennt, gefolgt von Erinnerungs Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="c115b-128">Intro Phrases are separated by a pair of tilde characters (~), followed by Reminder Phrases.</span></span> <span data-ttu-id="c115b-129">Diese Erinnerungs Ausdrücke sind auch durch ein paar Tilde Zeichen getrennt.</span><span class="sxs-lookup"><span data-stu-id="c115b-129">These Reminder Phrases are also separated by a pair of tilde characters.</span></span> <span data-ttu-id="c115b-130">Die zwei Sätze von Ausdrücken sind durch zwei Caretzeichen (^^) getrennt.</span><span class="sxs-lookup"><span data-stu-id="c115b-130">The two sets of phrases are separated by two caret characters (^^).</span></span> <span data-ttu-id="c115b-131">Es gibt keine Beschränkung für die Anzahl der einzelnen Ausdrücke, es sei denn, es muss mindestens eine vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c115b-131">There is no limit to the number of each kind of phrase, except that there must be at least one of each.</span></span>

 

 




