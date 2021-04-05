---
title: Ittsbusnotifysinkw
description: Ittsbusnotifysinkw
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a1ce3013ba1d8acf01f79b4f71d2d5088f4d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948018"
---
# <a name="ittsbufnotifysinkw"></a><span data-ttu-id="387c7-103">Ittsbusnotifysinkw</span><span class="sxs-lookup"><span data-stu-id="387c7-103">ITTSBufNotifySinkW</span></span>

<span data-ttu-id="387c7-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="387c7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="387c7-105">Die Engine muss **Lesezeichen** durchlesen.</span><span class="sxs-lookup"><span data-stu-id="387c7-105">The engine must call out through **BookMark**.</span></span> <span data-ttu-id="387c7-106">Während der Vorverarbeitung der Sprachausgabe fügt der Microsoft-Agent-Code Lesezeichen zwischen "Wörtern" ein und verwendet die Ankunft dieser Lesezeichen, um das Tempo des Texts in der Wort Sprechblase zu steuern.</span><span class="sxs-lookup"><span data-stu-id="387c7-106">During preprocessing of speech output, Microsoft Agent code inserts bookmarks between "words" and uses the arrival of those bookmarks to drive the pacing of text in the word balloon.</span></span> <span data-ttu-id="387c7-107">Obwohl SAPI nicht mehr als die Ankunft dieser Lesezeichen vor dem Ende der Äußerung benötigt, müssen die Lesezeichen relativ rechtzeitig zurückgegeben werden, um den Microsoft-Agent zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="387c7-107">While SAPI does not require anything more than the arrival of those bookmarks at some time before the end of the utterance, the bookmarks must be returned in a relatively timely fashion to support Microsoft Agent.</span></span>

<span data-ttu-id="387c7-108">Beachten Sie, dass es in manchen Sprachen (z. b. Japanisch) kein Strict-Konzept für "Word" gibt.</span><span class="sxs-lookup"><span data-stu-id="387c7-108">Note that there is no strict concept of "word" in some languages, such as Japanese.</span></span> <span data-ttu-id="387c7-109">Die [**sprach**](speak-method.md) Methode von Microsoft-Agent definiert ein Wort als eine verbundene Zeichenfolge von Symbolen, die eine Bedeutung und eine Aussprache isoliert hat.</span><span class="sxs-lookup"><span data-stu-id="387c7-109">Microsoft Agent's [**Speak**](speak-method.md) method defines a "word" as a connected string of symbols that has a meaning and pronunciation in isolation.</span></span> <span data-ttu-id="387c7-110">Der Microsoft-Agent verwendet relativ einfachen Code, um zu bestimmen, was ein Wort ist: Es sucht nach Symbolen, die durch Leerzeichen getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="387c7-110">Microsoft Agent uses fairly simple parsing code to determine what a "word" is: it looks for symbols separated by white space.</span></span> <span data-ttu-id="387c7-111">Folglich gibt es drei "Wörter" in der englischen Zeichenfolge "The 101 dalmatane": "The", "101" und "Dalmatier".</span><span class="sxs-lookup"><span data-stu-id="387c7-111">Thus, there are three "words" in the English string "The 101 Dalmatians": "the", "one hundred and one", and "Dalmatians".</span></span> <span data-ttu-id="387c7-112">Text, der im Microsoft Agent Map-Tag enthalten ist, wird als einzelnes "Wort" zu Anzeige Zwecken behandelt.</span><span class="sxs-lookup"><span data-stu-id="387c7-112">Text included in the Microsoft Agent Map tag is treated as a single "word" for display purposes.</span></span>

 

 




