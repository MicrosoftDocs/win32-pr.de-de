---
title: Video (Windows Media Player SDK)
description: Video
ms.assetid: 3c654494-19b5-401e-bed8-02f7cc7d7f4e
keywords:
- Windows Media Player Mobile Skins, Video
- Skins, Video
- Referenz für Skins, Video
- Video in Skins, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d505acec3f6917c7ed3d182c656ff5e9f29f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106340553"
---
# <a name="video-windows-media-player-sdk"></a><span data-ttu-id="ca5dd-107">Video (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="ca5dd-107">Video (Windows Media Player SDK)</span></span>

<span data-ttu-id="ca5dd-108">Eine Videoanzeige ermöglicht dem Benutzer die Anzeige digitaler Videodateien.</span><span class="sxs-lookup"><span data-stu-id="ca5dd-108">A video display allows the user to view digital video files.</span></span> <span data-ttu-id="ca5dd-109">Der Anzeigebereich des Videos ist nur sichtbar, wenn das Video abgespielt oder angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="ca5dd-109">The video display area is only visible when video is playing or paused.</span></span> <span data-ttu-id="ca5dd-110">Wenn Sie Ihre Skin entwerfen, sollten Sie Platz im Hintergrundbild reservieren, um die Videoanzeige zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="ca5dd-110">When you design your skin, you will want to reserve space in the Background image to contain the video display.</span></span> <span data-ttu-id="ca5dd-111">Wenn Sie dies nicht tun, kann sich die Videoanzeige selbst über alle sichtbaren Grafiken, wie z. b. die Hintergrund Datei, Schaltflächen und trackbars, übernehmen, sodass der Benutzer die Steuerelemente auf der Skin nicht mehr bedienen kann.</span><span class="sxs-lookup"><span data-stu-id="ca5dd-111">If you don't, the video display may superimpose itself over any visible art, such as the Background file, buttons, and trackbars, which will keep the user from operating the controls on your skin.</span></span>

<span data-ttu-id="ca5dd-112">Der Video Abschnitt der Skin-Definitionsdatei muss mit der folgenden Zeile beginnen:</span><span class="sxs-lookup"><span data-stu-id="ca5dd-112">The Video section of the skin definition file must begin with this line:</span></span>


```C++
[ Video ]

```



<span data-ttu-id="ca5dd-113">Anschließend müssen Sie eine Zeile hinzufügen, die den Speicherort und die Größe des Videoanzeige Bereichs in der Skin angibt.</span><span class="sxs-lookup"><span data-stu-id="ca5dd-113">You then must add a line that specifies the location and size of the video display area in your skin.</span></span>


```C++
0,38,240,172

```



<span data-ttu-id="ca5dd-114">Sie können die folgende Vorlage für den Video Abschnitt Ihrer Skin-Definitionsdatei verwenden:</span><span class="sxs-lookup"><span data-stu-id="ca5dd-114">You can use the following template for the Video section of your skin definition file:</span></span>


```C++
//  <Location>
//  ----------

```



<span data-ttu-id="ca5dd-115">In den folgenden Abschnitten finden Sie weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="ca5dd-115">The following sections provide further details.</span></span>

-   [<span data-ttu-id="ca5dd-116">Video Speicherort</span><span class="sxs-lookup"><span data-stu-id="ca5dd-116">Video Location</span></span>](video-location.md)
-   [<span data-ttu-id="ca5dd-117">Video Bildquelle</span><span class="sxs-lookup"><span data-stu-id="ca5dd-117">Video Image Source</span></span>](video-image-source.md)
-   [<span data-ttu-id="ca5dd-118">Video Größe</span><span class="sxs-lookup"><span data-stu-id="ca5dd-118">Video Size</span></span>](video-size.md)
-   [<span data-ttu-id="ca5dd-119">Beispiel für einen Video Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ca5dd-119">Sample Video Section</span></span>](sample-video-section.md)

## <a name="related-topics"></a><span data-ttu-id="ca5dd-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ca5dd-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca5dd-121">**Skin-Referenz**</span><span class="sxs-lookup"><span data-stu-id="ca5dd-121">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




