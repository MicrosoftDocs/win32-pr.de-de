---
title: Altersfreigabe
description: Altersfreigabe
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Windows Media Player Mobile Skins, BEWERTUNGEN
- Skins, BEWERTUNGEN
- Referenz für Skins, BEWERTUNGEN
- Bewertungen in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb90908c725fcb525e0be1547c27c588a4220c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337384"
---
# <a name="ratings"></a><span data-ttu-id="5459b-107">Altersfreigabe</span><span class="sxs-lookup"><span data-stu-id="5459b-107">Ratings</span></span>

<span data-ttu-id="5459b-108">Wenn Sie ein Skin für Windows Media Player 10,1 Mobile erstellen, können Sie die Bewertung anzeigen, die Windows Media Audio-basierten, derzeit wiedergegebenen Inhalt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5459b-108">When you create a skin for Windows Media Player 10.1 Mobile, you can display the rating associated with Windows Media Audio-based content that is currently playing.</span></span> <span data-ttu-id="5459b-109">Die Bewertung wird als Stern mit einer Zahl angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5459b-109">The rating is displayed as a star with a number on it.</span></span> <span data-ttu-id="5459b-110">Der Stern wird um eins bis fünf nummeriert, was die aktuelle Bewertung für diesen Inhalt anzeigt.</span><span class="sxs-lookup"><span data-stu-id="5459b-110">The star will be numbered one through five, denoting the current rating for that content.</span></span> <span data-ttu-id="5459b-111">Wenn der Inhalt nicht bewertet wird, wird der Stern mit 0 nummeriert.</span><span class="sxs-lookup"><span data-stu-id="5459b-111">If the content is not rated, the star will be numbered zero.</span></span>

<span data-ttu-id="5459b-112">Der bewertungsabschnitt der Skin-Definitionsdatei beginnt mit der folgenden Zeile:</span><span class="sxs-lookup"><span data-stu-id="5459b-112">The Ratings section of the skin definition file begins with this line:</span></span>


```C++
[ Ratings ]

```



<span data-ttu-id="5459b-113">Anschließend müssen Sie eine Zeile hinzufügen, die Informationen über die Größe und den Speicherort Ihres Bewertungs Symbols in der Skin enthält.</span><span class="sxs-lookup"><span data-stu-id="5459b-113">You then must add a line that contains information about the size and location of your ratings icon in your skin.</span></span>


```C++
147, 3, 22, 21       ratings96S.gif

```



<span data-ttu-id="5459b-114">Sie können die folgende Vorlage für den bewertungsabschnitt ihrer Skin-Definitionsdatei verwenden:</span><span class="sxs-lookup"><span data-stu-id="5459b-114">You can use the following template for the Ratings section of your skin definition file:</span></span>


```C++
// <Location>           <Image>
// ---------------      --------------------
```



<span data-ttu-id="5459b-115">Sie können einem Medien Element auch über die Benutzeroberfläche in Windows Media Player 10,1 Mobile einen Bewertungs Wert zuweisen. wenn das Gerät das nächste Mal mit einem Computer synchronisiert wird, wird der neue Bewertungs Wert an das Medien Element weitergegeben, wenn es sich in der Windows Media Player 10-Bibliothek befindet.</span><span class="sxs-lookup"><span data-stu-id="5459b-115">You can also assign a ratings value to a media item through the user interface in Windows Media Player 10.1 Mobile, and the next time the device synchronizes with the a computer, the new ratings value will be propagated to that media item if it resides in the Windows Media Player 10 library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5459b-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5459b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5459b-117">**Skin-Referenz**</span><span class="sxs-lookup"><span data-stu-id="5459b-117">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




