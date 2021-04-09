---
description: Wenn die Eigenschaft "Faktoid" auf "None" festgelegt wird, erkennt die Zeichenerkennung Zeichen für Zeichen.
ms.assetid: 4dacceab-032e-4b9b-858f-67961fd587b5
title: Wort und Zeichenerkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f521b8abf1064ef87c5c79c3293e725c44190ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128989"
---
# <a name="word-vs-character-recognition"></a><span data-ttu-id="16a91-103">Wort und Zeichenerkennung</span><span class="sxs-lookup"><span data-stu-id="16a91-103">Word vs. Character Recognition</span></span>

<span data-ttu-id="16a91-104">Wenn die Eigenschaft " [Faktoid](/previous-versions/ms835848(v=msdn.10)) " auf " **None**" festgelegt wird, erkennt die Zeichenerkennung Zeichen für Zeichen.</span><span class="sxs-lookup"><span data-stu-id="16a91-104">By setting the [Factoid](/previous-versions/ms835848(v=msdn.10)) property to **None**, the character recognizer recognizes handwriting on a character-by-character basis.</span></span>

<span data-ttu-id="16a91-105">Mit der Eigenschaft [RecoTimeout](/previous-versions/ms835852(v=msdn.10)) ([**RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) in Automation) wird die Anzahl der Millisekunden für die Verzögerung zwischen dem letzten [Strich](/previous-versions/ms552692(v=vs.100)) und dem Ende der Handschrift Eingabe angegeben.</span><span class="sxs-lookup"><span data-stu-id="16a91-105">The [RecoTimeout](/previous-versions/ms835852(v=msdn.10)) ([**RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) in Automation) property specifies the number of milliseconds of delay between the last [Stroke](/previous-versions/ms552692(v=vs.100)) and the end of handwriting input.</span></span> <span data-ttu-id="16a91-106">Sie können diesen Wert erhöhen, um Text zu erkennen, bevor ganze Wörter oder Sätze geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="16a91-106">You can increase this value to recognize text before entire words or sentences are written.</span></span> <span data-ttu-id="16a91-107">Sie können auch das [erkennen](/previous-versions/ms836275(v=msdn.10)) von frei Hand Eingaben mithilfe der Erkennungsmethode erzwingen.</span><span class="sxs-lookup"><span data-stu-id="16a91-107">You can also force the recognition of ink immediately by using the [Recognize](/previous-versions/ms836275(v=msdn.10)) method.</span></span>

 

 
