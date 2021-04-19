---
description: Eine Alternative ist eine potenzielle Wort Übereinstimmung für ein Erkennungs Segment. Eine Erkennung generiert Alternativen und basiert Sie auf akzeptablen Übereinstimmungen von frei Hand Eingaben oder Audioeingaben mit einem Wörterbuch oder einer Faktoid.
ms.assetid: 69327f1d-f240-4b8a-8bee-0a96a0c425c2
title: Alternative Stile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350c9ac97f0af1451a0ded6445cf658dad4ee4c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343204"
---
# <a name="alternates"></a><span data-ttu-id="0619a-104">Alternative Stile</span><span class="sxs-lookup"><span data-stu-id="0619a-104">Alternates</span></span>

<span data-ttu-id="0619a-105">Eine Alternative ist eine potenzielle Wort Übereinstimmung für ein Erkennungs Segment.</span><span class="sxs-lookup"><span data-stu-id="0619a-105">An alternate is a potential word match for a recognition segment.</span></span> <span data-ttu-id="0619a-106">Eine Erkennung generiert Alternativen und basiert Sie auf akzeptablen Übereinstimmungen von frei Hand Eingaben oder Audioeingaben mit einem Wörterbuch oder einer Faktoid.</span><span class="sxs-lookup"><span data-stu-id="0619a-106">A recognizer generates alternates and bases them on acceptable matches of the ink or audio input against a dictionary or factoid.</span></span>

> [!Note]  
> <span data-ttu-id="0619a-107">Die vertrauensbewertung ist derzeit nur für die Microsoft English (USA)-und Gesten Erkennungs Tools verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0619a-107">Confidence evaluation is currently available only for the Microsoft English (United States) and gesture recognizers.</span></span>

 

<span data-ttu-id="0619a-108">Manchmal kann die frei Hand Eingabe mehrdeutige Unterschiede zwischen Segmenten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0619a-108">Sometimes the ink may have ambiguous distinctions between segments.</span></span> <span data-ttu-id="0619a-109">Die Erkennung vergleicht diese Segmente mit einem Erkennungs Wörterbuch, um mögliche Übereinstimmungen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="0619a-109">The recognizer compares these segments to a recognizer dictionary to determine possible matches.</span></span> <span data-ttu-id="0619a-110">Wenn die Erkennung die Segmente vergleicht, behält Sie eine Liste möglicher alternativer Übereinstimmungen bei und weist jeder jeweils einen Vertrauensgrad zu.</span><span class="sxs-lookup"><span data-stu-id="0619a-110">When the recognizer compares the segments, it maintains a list of possible alternate matches and assigns a confidence level to each one, picking a top choice.</span></span>

> [!Note]  
> <span data-ttu-id="0619a-111">Die Erkennung kann keine Alternativen für einen Teil von frei Hand Eingaben bereitstellen, der kleiner als ein Erkennungs Segment ist.</span><span class="sxs-lookup"><span data-stu-id="0619a-111">The recognizer cannot provide alternates for a portion of ink that is smaller than a recognition segment.</span></span>

 

 

 



