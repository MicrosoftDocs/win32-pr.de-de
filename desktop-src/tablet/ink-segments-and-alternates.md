---
description: Eine Erkennung kann verschiedene Möglichkeiten finden, ein Ink-Beispiel in Erkennungs Segmente zu unterteilen. Daher kann die Anzahl der Erkennungs Alternativen auch für ein kleines frei Hand Beispiel sehr erstaunlich sein.
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: Frei Hand Segmente und-Alternativen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91183f6c9628ea798b66d703a59e44b26049e692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041705"
---
# <a name="ink-segments-and-alternates"></a><span data-ttu-id="55187-104">Frei Hand Segmente und-Alternativen</span><span class="sxs-lookup"><span data-stu-id="55187-104">Ink Segments and Alternates</span></span>

<span data-ttu-id="55187-105">Eine Erkennung kann verschiedene Möglichkeiten finden, ein Ink-Beispiel in Erkennungs Segmente zu unterteilen.</span><span class="sxs-lookup"><span data-stu-id="55187-105">A recognizer may find several ways to break an ink sample into recognition segments.</span></span> <span data-ttu-id="55187-106">Daher kann die Anzahl der Erkennungs Alternativen auch für ein kleines frei Hand Beispiel sehr erstaunlich sein.</span><span class="sxs-lookup"><span data-stu-id="55187-106">Because of this, the number of recognition alternates may be staggering, even for a small ink sample.</span></span>

<span data-ttu-id="55187-107">Beispielsweise kann "t o g e t h e r" die folgenden Ergebnisse liefern:</span><span class="sxs-lookup"><span data-stu-id="55187-107">For example, "t o g e t h e r" can yield the following results:</span></span>

-   <span data-ttu-id="55187-108">"um Sie zu erhalten" (plus Alternativen für jedes Wort)</span><span class="sxs-lookup"><span data-stu-id="55187-108">"to get her" (plus alternates for each word)</span></span>
-   <span data-ttu-id="55187-109">"to Gather" (plus-Alternativen für jedes Wort)</span><span class="sxs-lookup"><span data-stu-id="55187-109">"to gather" (plus alternates for each word)</span></span>
-   <span data-ttu-id="55187-110">"ein-oder-Äther" (Pluszeichen für jedes Wort)</span><span class="sxs-lookup"><span data-stu-id="55187-110">"tog ether" (plus alternates for each word)</span></span>
-   <span data-ttu-id="55187-111">"ein/aus" (plus Schalter für jedes Wort)</span><span class="sxs-lookup"><span data-stu-id="55187-111">"tog at her" (plus alternates for each word)</span></span>
-   <span data-ttu-id="55187-112">"zusammen" (plus Alternativen für das Wort)</span><span class="sxs-lookup"><span data-stu-id="55187-112">"together" (plus alternates for the word)</span></span>

<span data-ttu-id="55187-113">Das [**erkentionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) -Objekt unterstützt die effiziente Speicherung vollständiger Erkennungsergebnisse innerhalb des [**Ink**](inkdisp-class.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="55187-113">The [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object supports efficient storage of full recognition results within the [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="55187-114">Das **Ink** -Objekt ordnet die Erkennungs Alternativen den Strichen im **Ink** -Objekt zu und kann auch andere Informationen enthalten, wie z. b. baselineposition, Linien Indizes und Sprachbereiche.</span><span class="sxs-lookup"><span data-stu-id="55187-114">The **Ink** object maps the recognition alternates to the strokes in the **Ink** object and may also contain other information such as baseline position, line indices, and language ranges.</span></span>

 

 



