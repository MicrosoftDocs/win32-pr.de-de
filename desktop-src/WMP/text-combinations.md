---
title: Text Kombinationen
description: Text Kombinationen
ms.assetid: 0220b77e-5f1e-4569-a8fe-5085e0c16338
keywords:
- Windows Media Player Mobile Skins, marquees
- Skins, marquees
- Referenz für Skins, marquees
- marquees in Skins, Text Kombinationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5668a9e18555b871c82bae7ed1826766ec9429e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515842"
---
# <a name="text-combinations"></a><span data-ttu-id="39eeb-107">Text Kombinationen</span><span class="sxs-lookup"><span data-stu-id="39eeb-107">Text Combinations</span></span>

<span data-ttu-id="39eeb-108">Bei diesem Wert handelt es sich um eine durch Kommas getrennte Liste von Text-Anzeige Feld Kombinationen.</span><span class="sxs-lookup"><span data-stu-id="39eeb-108">This value is a list of text display box combinations, separated by commas.</span></span> <span data-ttu-id="39eeb-109">Textanzeige Felder können mit einem Pluszeichen verknüpft werden, um einen neuen Marquee-Anzeige Wert zu erstellen, und jeder Texttyp, der im Abschnitt "Texttyp" definiert ist, kann im Marquee verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39eeb-109">Text display boxes can be joined together by a plus character to create a new marquee display value and any text type defined in the Text Type section can be used in your marquee.</span></span>

<span data-ttu-id="39eeb-110">Wenn Sie bestimmen, was angezeigt werden soll, wertet Windows Media Player Mobile jedes Element in der Liste aus, um festzustellen, ob alle Teile verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="39eeb-110">When determining what to display, Windows Media Player Mobile evaluates each item in the list to see if all parts are available.</span></span> <span data-ttu-id="39eeb-111">Wenn dies nicht der Fall ist, wird das nächste Element ausgewertet usw., bis alle verfügbaren Teile gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="39eeb-111">If not, the next item is evaluated, and so on, until all the available parts have been found.</span></span> <span data-ttu-id="39eeb-112">Wenn Sie z. b. Author und Title anzeigen möchten, aber nicht sicher sind, ob beides verfügbar ist, verwenden Sie den folgenden Wert:</span><span class="sxs-lookup"><span data-stu-id="39eeb-112">For example, if you want to display Author and Title, but you're not sure whether both are available, use the following value:</span></span>


```C++
Title+Author, Title, Author

```



<span data-ttu-id="39eeb-113">Im vorherigen Beispiel wird der Titel + Author angezeigt, wenn der Titel und der Autor für das Medien Element definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="39eeb-113">In the preceding example, the Title+Author will be displayed if the title and author have been defined for the media item.</span></span> <span data-ttu-id="39eeb-114">Wenn beides nicht definiert ist, wird der Titel ausgewertet und bei der Definition angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39eeb-114">If both are not defined, the Title is evaluated and displayed if defined.</span></span> <span data-ttu-id="39eeb-115">Wenn der Titel nicht definiert ist, wird der Autor angezeigt, wenn er definiert ist.</span><span class="sxs-lookup"><span data-stu-id="39eeb-115">If the Title is not defined, the Author is displayed if defined.</span></span> <span data-ttu-id="39eeb-116">Wenn keines von beiden definiert ist, wird nichts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39eeb-116">If neither is defined, then nothing is displayed.</span></span>

<span data-ttu-id="39eeb-117">Wenn Sie das Pluszeichen für die Verkettung verwenden, stellen Sie sicher, dass keine Leerzeichen auf beiden Seiten des Plus Zeichens vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="39eeb-117">When using the plus sign for concatenation, be sure you have no spaces on either side of the plus sign.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39eeb-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39eeb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39eeb-119">**Marquee**</span><span class="sxs-lookup"><span data-stu-id="39eeb-119">**Marquee**</span></span>](marquee.md)
</dt> <dt>

[<span data-ttu-id="39eeb-120">**Texttyp**</span><span class="sxs-lookup"><span data-stu-id="39eeb-120">**Text Type**</span></span>](text-type.md)
</dt> </dl>

 

 




