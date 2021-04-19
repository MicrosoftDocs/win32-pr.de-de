---
description: Ein Erkennungs Segment ist die grundlegende frei Hand Einheit, die eine Erkennung intern verwendet, um ein Erkennungs Ergebnis für ein bestimmtes Ink-Objekt zu erhalten.
ms.assetid: 5215a0bd-6dff-4cda-b2e5-c54f64680e02
title: Erkennungs Segmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7037849378477950b906b85efe6980c4246421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350112"
---
# <a name="recognition-segments"></a><span data-ttu-id="ea5d9-103">Erkennungs Segmente</span><span class="sxs-lookup"><span data-stu-id="ea5d9-103">Recognition Segments</span></span>

<span data-ttu-id="ea5d9-104">Ein Erkennungs Segment ist die grundlegende frei Hand Einheit, die eine Erkennung intern verwendet, um ein Erkennungs Ergebnis für ein bestimmtes Ink-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ea5d9-104">A recognition segment is the basic ink unit that a recognizer uses internally to produce a recognition result for a particular Ink object.</span></span> <span data-ttu-id="ea5d9-105">Ein Erkennungs Segment ist eine Auflistung von Hand Strichen.</span><span class="sxs-lookup"><span data-stu-id="ea5d9-105">A recognition segment is a collection of ink strokes.</span></span> <span data-ttu-id="ea5d9-106">Beispielsweise kann ein Erkennungs Modul, das eine englische, kursive Handschrift erkennen kann, ein Wort als grundlegendes Erkennungs Segment verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea5d9-106">For example, a recognizer that is capable of recognizing English cursive handwriting might use a word as the basic recognition segment.</span></span>

<span data-ttu-id="ea5d9-107">Andere Erkennungs Tools können Teile von zusammengesetzten Wörtern als einfache Segmente verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea5d9-107">Other recognizers may use parts of composite words as basic segments.</span></span> <span data-ttu-id="ea5d9-108">In Spanisch werden z. b. kurze Wörter häufig kombiniert, um längere zusammengesetzte Wörter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ea5d9-108">For example, in Spanish, short words are commonly combined to provide longer composite words.</span></span> <span data-ttu-id="ea5d9-109">"Damelo" ist ein spanisches Wort, das aus drei Wörtern besteht ("da bin Lo"), aber als einzelnes Wort geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ea5d9-109">"Damelo" is a Spanish word that is composed of three words "da me lo" (give me that), but it is written as a single word.</span></span> <span data-ttu-id="ea5d9-110">Ein spanischer Erkennungs Modul könnte jedes Teilwort als Segment erkennen.</span><span class="sxs-lookup"><span data-stu-id="ea5d9-110">A Spanish recognizer could recognize each subword as a segment.</span></span>

<span data-ttu-id="ea5d9-111">Eine Erkennung kann verschiedene Möglichkeiten finden, ein Ink-Beispiel in Erkennungs Segmente zu unterteilen.</span><span class="sxs-lookup"><span data-stu-id="ea5d9-111">A recognizer may find several ways to break an ink sample into recognition segments.</span></span> <span data-ttu-id="ea5d9-112">Da Mehrdeutigkeit an der Erkennung der beabsichtigten Eingabe des Benutzers beteiligt ist, kann die Erkennung viele alternative Übereinstimmungen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ea5d9-112">Because ambiguity is involved in recognizing the user's intended input, the recognizer can return many alternate matches.</span></span>

<span data-ttu-id="ea5d9-113">Weitere Informationen zu Alternativen finden Sie unter [Alternativen](alternates.md).</span><span class="sxs-lookup"><span data-stu-id="ea5d9-113">For more information about alternates, see [Alternates](alternates.md).</span></span>

 

 



