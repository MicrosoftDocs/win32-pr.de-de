---
description: Um für jedes Erkennungs Ergebnis eine Vertrauens Ebene zu erhalten, können Sie entweder die Eigenschaft Vertrauen des Objekts "erkenntionalternate" oder die Eigenschaft "Vertrauen" des Gesten Objekts abrufen.
ms.assetid: b2495c5b-6db4-401c-ab7a-6556c55bbe46
title: Confidence-Eigenschaft [Informationen zur Erkennung]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f436d17d5cb83901c7d19ef4beb6dfb7ce6199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861916"
---
# <a name="confidence-property-about-recognition"></a><span data-ttu-id="22ff6-103">Vertrauens Eigenschaft \[ für die Erkennung\]</span><span class="sxs-lookup"><span data-stu-id="22ff6-103">Confidence Property \[About Recognition\]</span></span>

<span data-ttu-id="22ff6-104">Um für jedes Erkennungs Ergebnis eine Vertrauens Ebene zu erhalten, können Sie entweder die Eigenschaft [**Vertrauen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) des Objekts " [**erkenntionalternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) " oder die Eigenschaft " [**Vertrauen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) " des [**Gesten**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) Objekts abrufen.</span><span class="sxs-lookup"><span data-stu-id="22ff6-104">To obtain a level of confidence for each recognition result, you can get either the [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) property of the [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) object or the [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) property of the [**Gesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) object.</span></span> <span data-ttu-id="22ff6-105">Der Vertrauensgrad ist eine Zahl, die den Grad der Vertrauenswürdigkeit für jedes Alternative Erkennungs Ergebnis angibt, das die Erkennung für ein entsprechendes Erkennungs Segment zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="22ff6-105">The confidence level is a number that indicates the degree of confidence for each alternate recognition result that the recognizer returns for a corresponding recognition segment.</span></span>

<span data-ttu-id="22ff6-106">Das Vertrauen wird als niedrig, Mittelwert oder hoch zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="22ff6-106">Confidence is returned as low, average, or high.</span></span> <span data-ttu-id="22ff6-107">Die Anwendung verwendet folgende Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="22ff6-107">The application uses these results to:</span></span>

-   <span data-ttu-id="22ff6-108">Geben Sie dem Benutzer an, dass mehrere Möglichkeiten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="22ff6-108">Indicate to the user that multiple possibilities exist.</span></span>
-   <span data-ttu-id="22ff6-109">Ordnen Sie die Alternativen nach Vertrauensgrad zu.</span><span class="sxs-lookup"><span data-stu-id="22ff6-109">Rank the alternates by confidence level.</span></span>

## <a name="what-affects-confidence"></a><span data-ttu-id="22ff6-110">Auswirkungen auf das Vertrauen</span><span class="sxs-lookup"><span data-stu-id="22ff6-110">What Affects Confidence</span></span>

<span data-ttu-id="22ff6-111">Einige der Dinge, die die Handschrifterkennung erschweren und die Zuversicht beeinflussen, sind:</span><span class="sxs-lookup"><span data-stu-id="22ff6-111">Some of the things that make handwriting recognition difficult and affect confidence include:</span></span>

-   <span data-ttu-id="22ff6-112">Schwierigkeiten beim Bestimmen der Wort Segmentierung</span><span class="sxs-lookup"><span data-stu-id="22ff6-112">Difficulty determining word segmentation</span></span>

![Bild, das die zu schließende Schreibvorgänge anzeigt](images/5c5d1c42-cbd1-46d0-a6f8-653f204f52cd.jpg)

-   <span data-ttu-id="22ff6-114">Fall Schwierigkeiten</span><span class="sxs-lookup"><span data-stu-id="22ff6-114">Case difficulties</span></span>

![Bild, das Schwierigkeiten mit handschriftlichen Versionen des Worts "Case" anzeigt](images/1bdfb2e3-06ac-4c49-a39b-f0be51aed0e8.jpg)

-   <span data-ttu-id="22ff6-116">Ungewöhnliche Schreibstile</span><span class="sxs-lookup"><span data-stu-id="22ff6-116">Uncommon writing styles</span></span>
-   <span data-ttu-id="22ff6-117">Isoliertes Satzzeichen</span><span class="sxs-lookup"><span data-stu-id="22ff6-117">Isolated punctuation</span></span>

![Bild, das Anführungszeichen anzeigt, die zu weit von Text entfernt sind](images/743364b3-af62-4775-9d0d-f13f6e36c922.jpg)

-   <span data-ttu-id="22ff6-119">Zeichen mit Akzent in englischer Sprache</span><span class="sxs-lookup"><span data-stu-id="22ff6-119">Accented characters in English recognizers</span></span>

> [!Note]  
> <span data-ttu-id="22ff6-120">Die vertrauensbewertung ist nur für USA Englisch und alle Gesten erkenzer in dieser Version verfügbar.</span><span class="sxs-lookup"><span data-stu-id="22ff6-120">Confidence evaluation is available only for United States English and all gesture recognizers in this release.</span></span> <span data-ttu-id="22ff6-121">Methoden, die die Eigenschaft "Vertrauen" für alle anderen erkenungen bereitstellen, geben " **E \_ notimpl**" zurück.</span><span class="sxs-lookup"><span data-stu-id="22ff6-121">Methods that provide the confidence property for any other recognizer will return **E\_NOTIMPL**.</span></span>

 

 

 



