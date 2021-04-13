---
title: Ittsnotifysinkw
description: Ittsnotifysinkw
ms.assetid: 6305dad6-c162-458a-899e-628f6486680e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5820f262779f86deeeca9982d0551b16d3a3406
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389944"
---
# <a name="ittsnotifysinkw"></a><span data-ttu-id="c00ca-103">Ittsnotifysinkw</span><span class="sxs-lookup"><span data-stu-id="c00ca-103">ITTSNotifySinkW</span></span>

<span data-ttu-id="c00ca-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="c00ca-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c00ca-105">Die Engine muss über [**audiostop**](https://www.bing.com/search?q=**AudioStop**), [**audiostart**](https://www.bing.com/search?q=**AudioStart**)und [**Visual**](https://www.bing.com/search?q=**Visual**)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c00ca-105">The engine must call out through [**AudioStop**](https://www.bing.com/search?q=**AudioStop**), [**AudioStart**](https://www.bing.com/search?q=**AudioStart**), and [**Visual**](https://www.bing.com/search?q=**Visual**).</span></span> <span data-ttu-id="c00ca-106">Der **visuelle** Rückruf muss IPA-Phonemes bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c00ca-106">The **Visual** callback must provide IPA phonemes.</span></span> <span data-ttu-id="c00ca-107">(Das internationale phonetische Alphabet \[ IPA \] ist eine universelle Notation zum Beschreiben des phonetischen Inhalts der gesprochenen Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="c00ca-107">(The International Phonetic Alphabet \[IPA\] is a universal notation for describing the phonetic content of spoken communication.</span></span> <span data-ttu-id="c00ca-108">Alle speakbaren Phoneme verfügen über Darstellungen in IPA.</span><span class="sxs-lookup"><span data-stu-id="c00ca-108">All speakable phonemes have representations in IPA.</span></span> <span data-ttu-id="c00ca-109">Details zur IPA-Datei finden Sie in der Microsoft Speech-API-Spezifikation \[ Teil des Sprach-SDK 4,0-Downloads \] unter [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx) .)</span><span class="sxs-lookup"><span data-stu-id="c00ca-109">Details of IPA are in the Microsoft Speech API specification \[part of the Speech SDK 4.0 download\] at [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx).)</span></span>

<span data-ttu-id="c00ca-110">Obwohl die [**visuelle**](https://www.bing.com/search?q=**Visual**) Benachrichtigung recht umfangreich ist, verwendet der Microsoft-Agent nur den **cipaphoneme** -Wert, um den Mund zu animieren, wenn das Zeichen spricht.</span><span class="sxs-lookup"><span data-stu-id="c00ca-110">Although the [**Visual**](https://www.bing.com/search?q=**Visual**) notification is fairly rich, Microsoft Agent uses only the **cIPAPhoneme** value to animate the mouth as the character speaks.</span></span> <span data-ttu-id="c00ca-111">Alle Microsoft-Agent-kompatiblen Module müssen einen eng synchronisierten Stream von **visuellen** Benachrichtigungen bereitstellen, die den phonetischen Inhalt der erzeugten Äußerung widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="c00ca-111">Any Microsoft Agent-compatible engine must provide a closely synchronized stream of **Visual** notifications reflecting the phonetic content of the produced utterance.</span></span> <span data-ttu-id="c00ca-112">In diesem Fall ist die "relativ rechtzeitige Benachrichtigung" nicht ausreichend, da Sprecher der Sprech Anwendung recht sensibel auf Abweichungen zwischen mundposition und Akustik Inhalt sind.</span><span class="sxs-lookup"><span data-stu-id="c00ca-112">In this case, "relatively timely notification" is not adequate, because speaker-hearers are fairly sensitive to discrepancies between mouth position and acoustic content.</span></span> <span data-ttu-id="c00ca-113">**Visuelle** Benachrichtigungen müssen umgehend zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c00ca-113">**Visual** notifications need to be returned promptly.</span></span>

 

 




