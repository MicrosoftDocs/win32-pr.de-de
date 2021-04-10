---
title: Entwerfen der Schnittstelle
description: Entwerfen der Schnittstelle
ms.assetid: 7b87bab4-8246-461a-a9cd-2d348e7f0d48
keywords:
- Windows Media Player Mobile Skins, Benutzeroberflächen
- Skins, Benutzeroberflächen
- Erstellen von Skins, Benutzeroberflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8070ef6fd4589f762624d7a0b5ee1d380a264066
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100774"
---
# <a name="designing-the-interface"></a><span data-ttu-id="300f6-106">Entwerfen der Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="300f6-106">Designing the Interface</span></span>

<span data-ttu-id="300f6-107">Nachdem die Funktionen ausgewählt wurden, kann die Schnittstelle entworfen werden.</span><span class="sxs-lookup"><span data-stu-id="300f6-107">Once the functions have been chosen, the interface can be designed.</span></span> <span data-ttu-id="300f6-108">Eine einfache Schnittstelle wurde ausgewählt, um die Funktionalität zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="300f6-108">A simple interface was chosen to match the functionality.</span></span> <span data-ttu-id="300f6-109">Symbole für die Steuerelemente wurden aus VCR-Standard Steuerelementen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="300f6-109">Symbols for the controls were chosen from standard VCR controls.</span></span>

<span data-ttu-id="300f6-110">In der folgenden Abbildung wird gezeigt, wie die Schnittstelle aussieht.</span><span class="sxs-lookup"><span data-stu-id="300f6-110">The following image shows what the interface will look like.</span></span>

![Beispiel Schnittstelle](images/ceswmful.png)

-   <span data-ttu-id="300f6-112">**PLAYPAUSE oder playpausestopschaltfläche.**</span><span class="sxs-lookup"><span data-stu-id="300f6-112">**PlayPause or PlayPauseStop button.**</span></span> <span data-ttu-id="300f6-113">Der Benutzer greift auf die meisten zu, daher können Sie eine größere Schaltfläche in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="300f6-113">The user will be tapping this the most, so you might consider a larger button.</span></span> <span data-ttu-id="300f6-114">Die obere rechte Ecke stellt einen guten Speicherort dar, den der Benutzer schnell finden kann.</span><span class="sxs-lookup"><span data-stu-id="300f6-114">The upper-right corner makes a good location that the user can find quickly.</span></span> <span data-ttu-id="300f6-115">Ein voll Bild Pfeil wird verwendet, um die Wiedergabe anzugeben, und zwei vertikale Balken (hier nicht dargestellt) werden verwendet, um die Pause anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="300f6-115">A solid arrow is used to indicate play and two vertical bars (not shown here) will be used to indicate pause.</span></span>
    > [!Note]  
    > <span data-ttu-id="300f6-116">Die Schaltfläche playpauenbeenden kann nur beim Erstellen eines Skin für Windows Media Player 10 Mobile oder höher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="300f6-116">The PlayPauseStop button can only be used when creating a skin for Windows Media Player 10 Mobile or later.</span></span>

     

-   <span data-ttu-id="300f6-117">**Schaltfläche "Abbrechen"**</span><span class="sxs-lookup"><span data-stu-id="300f6-117">**Stop button.**</span></span> <span data-ttu-id="300f6-118">Um das Auffinden zu erleichtern, wird es in der linken oberen Ecke platziert.</span><span class="sxs-lookup"><span data-stu-id="300f6-118">To make this easy to find, it is placed at the upper-left corner.</span></span> <span data-ttu-id="300f6-119">Ein Quadrat wird verwendet, um den Vorgang zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="300f6-119">A square is used to indicate stop.</span></span> <span data-ttu-id="300f6-120">Wenn Sie ein Skin für Windows Media Player 10 Mobile oder höher erstellen, stellt die playpauenstop-Schalt Fläche diese Funktionalität bereits bereit.</span><span class="sxs-lookup"><span data-stu-id="300f6-120">If you are creating a skin for Windows Media Player 10 Mobile or later, the PlayPauseStop button already provides this functionality.</span></span>
-   <span data-ttu-id="300f6-121">**Die Schaltflächen Next und Prev.**</span><span class="sxs-lookup"><span data-stu-id="300f6-121">**Next and Prev buttons.**</span></span> <span data-ttu-id="300f6-122">Da diese nicht so häufig verwendet werden, werden Sie auf der linken Seite platziert.</span><span class="sxs-lookup"><span data-stu-id="300f6-122">Since these will not be used as often, they are placed on the left.</span></span> <span data-ttu-id="300f6-123">Das nächste befindet sich über der Schaltfläche "Prev", da Benutzer wahrscheinlich in einer Wiedergabeliste fortfahren möchten.</span><span class="sxs-lookup"><span data-stu-id="300f6-123">The Next is above the Prev button because people will more likely want to move forward in a playlist.</span></span> <span data-ttu-id="300f6-124">Die Symbole mit Doppelpfeil werden verwendet, da Sie in der-Funktion mit einem Fast-Forward-Steuerelement vergleichbar sind.</span><span class="sxs-lookup"><span data-stu-id="300f6-124">The double-arrow symbols are used because they are similar in function to a fast-forward control.</span></span>
-   <span data-ttu-id="300f6-125">**Volume TrackBar.**</span><span class="sxs-lookup"><span data-stu-id="300f6-125">**Volume trackbar.**</span></span> <span data-ttu-id="300f6-126">Diese wird unten auf dem Bildschirm platziert und ist eine einfache Zeile mit einer Zieh Punkt Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="300f6-126">This is placed at the bottom of the screen and is a simple line with a thumb button on top of it.</span></span>
-   <span data-ttu-id="300f6-127">**Marquee-Textfeld.**</span><span class="sxs-lookup"><span data-stu-id="300f6-127">**Marquee text box.**</span></span> <span data-ttu-id="300f6-128">Diese wird unter der Schaltfläche PLAYPAUSE oder playpauseend platziert, sodass Sie leicht zu erkennen ist.</span><span class="sxs-lookup"><span data-stu-id="300f6-128">This is placed under the PlayPause or PlayPauseStop button so that it is easy to see.</span></span>

<span data-ttu-id="300f6-129">Möglicherweise möchten Sie dies zuerst skizzieren und mit der Platzierung der einzelnen Benutzeroberflächen Elemente experimentieren.</span><span class="sxs-lookup"><span data-stu-id="300f6-129">You may want to sketch this first and experiment with the placement of each user interface element.</span></span> <span data-ttu-id="300f6-130">Der hier gezeigte Entwurf wurde aus Gründen der Einfachheit und Benutzerfreundlichkeit ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="300f6-130">The design shown here was chosen for simplicity and ease of use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="300f6-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="300f6-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="300f6-132">**Skin Guide**</span><span class="sxs-lookup"><span data-stu-id="300f6-132">**Skin Guide**</span></span>](skin-guide.md)
</dt> </dl>

 

 




