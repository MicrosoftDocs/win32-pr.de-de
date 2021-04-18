---
title: Hinzufügen von Videos
description: Hinzufügen von Videos
ms.assetid: 6f20a9ad-e92e-4774-868d-ad0e071f4935
keywords:
- Erstellen von Skins, Video
- Windows Media Player Skins, Video
- Skins, Video
- Video in Skins, hinzufügen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc952f2fa80536bc6b2bb9ef3b43c6730616af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340427"
---
# <a name="adding-video"></a><span data-ttu-id="58968-107">Hinzufügen von Videos</span><span class="sxs-lookup"><span data-stu-id="58968-107">Adding Video</span></span>

<span data-ttu-id="58968-108">Sie können der Datei ein Video hinzufügen, indem Sie einfach das **Video** -Element verwenden und definieren, wo das Videofenster platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="58968-108">You can add a video to your file by simply using the **VIDEO** element and defining where you want the video window to be placed.</span></span>

<span data-ttu-id="58968-109">Verwenden Sie denselben Code wie im Abschnitt auswählen von Dateien. Sie müssen lediglich das **Video** -Element mit den Attributen "Top", "Left", "width" und "Height" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="58968-109">Use the same code as you did in the Choosing Files section; all you need to do is add the **VIDEO** element with the top, left, width, and height attributes.</span></span>


```C++
        <VIDEO
            top = "10"
            left = "80"
            width = "180"
            height = "180"/>

```



<span data-ttu-id="58968-110">Wenn Sie ein Video abspielen, wird es im Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="58968-110">Then when you play a video, it will be displayed in the window.</span></span> <span data-ttu-id="58968-111">Die Grafik für das Video Beispiel wurde geändert, um eine etwas größere Skin zu machen.</span><span class="sxs-lookup"><span data-stu-id="58968-111">The art for the video sample was modified to make a slightly larger skin.</span></span> <span data-ttu-id="58968-112">Da Schichten in Photoshop verwendet wurden, wurden die Schaltflächen leicht verschoben, und ein neuer Satz wurde sehr schnell erstellt.</span><span class="sxs-lookup"><span data-stu-id="58968-112">Because layers were used in Photoshop, the buttons were easily moved around and a new set was created very quickly.</span></span> <span data-ttu-id="58968-113">Nur das Hintergrundbild wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="58968-113">Only the background image was changed.</span></span> <span data-ttu-id="58968-114">Eine Füllung wurde in einer leeren Ebene verwendet, und es wurde eine einschrägung und ein Prägung-Effekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="58968-114">A fill was used in a blank layer and a bevel and emboss effect was added.</span></span>

<span data-ttu-id="58968-115">Im Beispiel Abschnitt des SDK sehen Sie eine ähnliche funktionierende Grafik Skin.</span><span class="sxs-lookup"><span data-stu-id="58968-115">You can see a similar working video skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58968-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="58968-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58968-117">**Leitfaden zum Erstellen von Skin**</span><span class="sxs-lookup"><span data-stu-id="58968-117">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




