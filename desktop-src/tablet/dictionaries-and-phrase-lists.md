---
description: Das Lexicon oder die Liste möglicher Wörter, die vom Sprachmodell einer bestimmten Erkennungsfunktion verwendet werden, ist in mindestens einem Wörterbuch enthalten.
ms.assetid: e975a75f-ab88-4164-afc8-3b817988504d
title: Wörterbücher und Ausdrucks Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f88dc2f6b05eea322b6e88dda1f986b3c54b7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353898"
---
# <a name="dictionaries-and-phrase-lists"></a><span data-ttu-id="8e212-103">Wörterbücher und Ausdrucks Listen</span><span class="sxs-lookup"><span data-stu-id="8e212-103">Dictionaries and Phrase lists</span></span>

<span data-ttu-id="8e212-104">Das Lexicon oder die Liste möglicher Wörter, die vom Sprachmodell einer bestimmten Erkennungsfunktion verwendet werden, ist in mindestens einem Wörterbuch enthalten.</span><span class="sxs-lookup"><span data-stu-id="8e212-104">The lexicon, or list of possible words used by a particular recognizer's language model, is contained in one or more dictionaries.</span></span> <span data-ttu-id="8e212-105">Die Erkennung durchsucht alle im System verfügbaren Wörterbücher, wenn Erkennungs Übereinstimmungen kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="8e212-105">The recognizer searches all dictionaries available on the system when compiling recognition matches.</span></span> <span data-ttu-id="8e212-106">Sie können die Microsoft Speech APIs (SAPI) verwenden, um einige dieser Wörterbücher zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8e212-106">You can use the Microsoft Speech APIs (SAPI) to modify some of these dictionaries.</span></span>

<span data-ttu-id="8e212-107">Eine Ausdrucks Liste stellt eine andere Möglichkeit zum Ändern des vokabularerkennungs-Vokabulars dar.</span><span class="sxs-lookup"><span data-stu-id="8e212-107">A phrase list provides another means of modifying the recognizer's vocabulary.</span></span> <span data-ttu-id="8e212-108">Durch das Hinzufügen von Wörtern zu einer Ausdrucks Liste wird das Vokabular erweitert. durch das Hinzufügen von Wörtern und Einschränken der Erkennungsfunktion zur Verwendung nur der Ausdrucks Liste (im Gegensatz zur Ausdrucks Liste und den Wörterbüchern) wird das Vokabular eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="8e212-108">Adding words to a phrase list extends the vocabulary; adding words and then constraining the recognizer to use only the phrase list (as opposed to the phrase list and the dictionaries) restricts the vocabulary.</span></span>

<span data-ttu-id="8e212-109">Frühere Versionen der Tablet PC-Technologie-APIs stützten sich auf das Konzept der Wortlisten.</span><span class="sxs-lookup"><span data-stu-id="8e212-109">Previous releases of the Tablet PC Technology APIs relied on the concept of word lists.</span></span> <span data-ttu-id="8e212-110">Word-Listen sind fast identisch mit den Ausdrucks Listen und werden für denselben Zweck verwendet, wenn Sie direkt mit einem [**erkenzercontext**](inkrecognizercontext-class.md) -Objekt in einer Anwendung arbeiten, für die frei Hand Eingaben aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8e212-110">Word lists are almost identical to phrase lists and are used for the same purpose when working directly with a [**RecognizerContext**](inkrecognizercontext-class.md) object in an application that is ink enabled.</span></span> <span data-ttu-id="8e212-111">Weitere Informationen dazu, wo und wann Wortlisten verwendet werden sollten, finden Sie unter [Setting Context for Ink-Enabled Controls](setting-context-for-ink-enabled-controls.md).</span><span class="sxs-lookup"><span data-stu-id="8e212-111">For more details about where and when to use word lists, see [Setting Context for Ink-Enabled Controls](setting-context-for-ink-enabled-controls.md).</span></span>

<span data-ttu-id="8e212-112">Wenn die Größe der Liste, mit der Sie das Lexikon erweitern möchten, 100.000 Wörter überschreitet, empfiehlt es sich, anstelle einer Wort Liste oder einer Ausdrucks Liste ein Wörterbuch zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e212-112">When the size of the list with which you want to extend the lexicon exceeds 100,000 words, we recommend that you use a dictionary instead of a word list or phrase list.</span></span>

 

 



