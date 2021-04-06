---
title: Natürliche Variation verwenden
description: Natürliche Variation verwenden
ms.assetid: 5d5750e4-cf30-43dc-9419-7e6bbdb9aa5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd2d35afeb168dc8839ba259f0079434b487c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100642"
---
# <a name="use-natural-variation"></a><span data-ttu-id="9faac-103">Natürliche Variation verwenden</span><span class="sxs-lookup"><span data-stu-id="9faac-103">Use Natural Variation</span></span>

<span data-ttu-id="9faac-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="9faac-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="9faac-105">Obwohl die Konsistenz der Darstellung in der herkömmlichen Schnittstelle Ihrer Anwendung, wie z. b. Menüs und Dialogfeldern, die Schnittstelle besser vorhersagbar macht, verändern Sie die Animation und die gesprochene Ausgabe in der Schnittstelle des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="9faac-105">While consistency of presentation in your application's conventional interface, such as menus and dialog boxes, makes the interface more predictable, vary the animation and spoken output in the character's interface.</span></span> <span data-ttu-id="9faac-106">Eine angemessene Variation der Zeichen Antworten bietet eine natürlichere Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="9faac-106">Appropriately varying the character's responses provides a more natural interface.</span></span> <span data-ttu-id="9faac-107">Wenn ein Zeichen den Benutzer immer genau auf die gleiche Weise adressiert, Wenn Sie z. b. immer die gleichen Wörter sagen, ist es wahrscheinlich, dass der Benutzer das Zeichen langweilig, uneigennützig oder sogar ungrob betrachtet.</span><span class="sxs-lookup"><span data-stu-id="9faac-107">If a character always addresses the user exactly the same way; for example, always saying the same words, the user is likely to consider the character boring, disinterested, or even rude.</span></span> <span data-ttu-id="9faac-108">Die menschliche Kommunikation umfasst selten eine genaue Wiederholung.</span><span class="sxs-lookup"><span data-stu-id="9faac-108">Human communication rarely involves precise repetition.</span></span> <span data-ttu-id="9faac-109">Auch wenn etwas in ähnlicher Situation wiederholt wird, können wir den Wortlaut, Gesten oder Gesichtsausdruck ändern.</span><span class="sxs-lookup"><span data-stu-id="9faac-109">Even when repeating something in a similar situation, we may change wording, gestures, or facial expression.</span></span>

<span data-ttu-id="9faac-110">Mit dem Microsoft-Agent können Sie in einer Variation für ein Zeichen erstellen.</span><span class="sxs-lookup"><span data-stu-id="9faac-110">Microsoft Agent enables you to build in some variation for a character.</span></span> <span data-ttu-id="9faac-111">Wenn Sie die Animationen eines Zeichens definieren, können Sie die Verzweigungs Wahrscheinlichkeiten in jedem Animations Frame verwenden, um eine Animation zu ändern, wenn Sie wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9faac-111">When defining a character's animations, you can use branching probabilities on any animation frame to change an animation when it plays.</span></span> <span data-ttu-id="9faac-112">Sie können jedem Zustand auch mehrere Animationen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="9faac-112">You can also assign multiple animations to each state.</span></span> <span data-ttu-id="9faac-113">Der Microsoft-Agent wählt nach dem Zufallsprinzip eine der zugewiesenen Animationen aus.</span><span class="sxs-lookup"><span data-stu-id="9faac-113">Microsoft Agent randomly chooses one of the assigned animations each time it initiates a state.</span></span> <span data-ttu-id="9faac-114">Bei der Sprachausgabe können Sie auch vertikale Balken Zeichen in den Ausgabetext einschließen, damit der gesprochene Text automatisch variiert.</span><span class="sxs-lookup"><span data-stu-id="9faac-114">For speech output, you can also include vertical bar characters in your output text to automatically vary the text spoken.</span></span> <span data-ttu-id="9faac-115">Der Microsoft-Agent wählt z. b. nach dem Zufallsprinzip eine der folgenden Anweisungen aus, wenn dieser Text als Teil der [**Sprech**](speak-method.md) Methode verarbeitet wird:</span><span class="sxs-lookup"><span data-stu-id="9faac-115">For example, Microsoft Agent will randomly select one of the following statements when processing this text as part of the [**Speak**](speak-method.md) method:</span></span>

<span data-ttu-id="9faac-116">"Ich kann dies sagen. \| Das kann ich sagen. \| Ich kann etwas anderes sagen. "</span><span class="sxs-lookup"><span data-stu-id="9faac-116">"I can say this.\|I can say that.\|I can say something else."</span></span>

 

 




