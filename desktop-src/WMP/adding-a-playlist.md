---
title: Hinzufügen einer Wiedergabeliste
description: Hinzufügen einer Wiedergabeliste
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- Erstellen von Skins, Wiedergabelisten
- Windows Media Player Skins, Wiedergabelisten
- Skins, Wiedergabelisten
- Wiedergabelisten, Skins
- Metadatei-Wiedergabelisten, Skins
- Windows Media Metadatei-Wiedergabelisten, Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42a4bc253d4b1a3ba9b8fe0f31ca16b0d522956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340226"
---
# <a name="adding-a-playlist"></a><span data-ttu-id="684e8-109">Hinzufügen einer Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="684e8-109">Adding a Playlist</span></span>

<span data-ttu-id="684e8-110">Mithilfe von Wiedergabelisten können Sie aus den Sammlungen ihrer Audiodaten und Videos auswählen.</span><span class="sxs-lookup"><span data-stu-id="684e8-110">You can use playlists to choose from collections of your audio and video.</span></span>

<span data-ttu-id="684e8-111">Wenn Sie die Grafik von ihrer ersten Skin verwenden, können Sie einige Änderungen an der Skin-Definitionsdatei vornehmen.</span><span class="sxs-lookup"><span data-stu-id="684e8-111">Using the artwork from your first skin, you can make a few changes to the skin definition file.</span></span>

<span data-ttu-id="684e8-112">Der erste Schritt besteht darin, die Shell zu verwenden, die für die meisten Skins verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="684e8-112">The first step is to use the shell you will use for most skins:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">

        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
    </VIEW>


</THEME>

```



<span data-ttu-id="684e8-113">Fügen Sie nun eine zweite **Ansicht** hinzu, die eine Wiedergabeliste enthält.</span><span class="sxs-lookup"><span data-stu-id="684e8-113">Now add a second **VIEW**, which contains a playlist.</span></span> <span data-ttu-id="684e8-114">Platzieren Sie den folgenden Code nach dem </VIEW> des Shellcodes.</span><span class="sxs-lookup"><span data-stu-id="684e8-114">Place the following code after the </VIEW> of the shell code.</span></span>


```C++
     <VIEW 
          id = "playview">
          <PLAYLIST/>
     </VIEW>

```



<span data-ttu-id="684e8-115">Sie müssen dieser zweiten Ansicht eine ID zuordnen, damit Sie später darauf verweisen können.</span><span class="sxs-lookup"><span data-stu-id="684e8-115">You will need to give this second view an ID so you can refer to it later.</span></span> <span data-ttu-id="684e8-116">Fügen Sie ein playelement und ein stopelement hinzu.</span><span class="sxs-lookup"><span data-stu-id="684e8-116">Add a PLAYELEMENT and a STOPELEMENT.</span></span> <span data-ttu-id="684e8-117">Diese vordefinierten Schaltflächen machen das Leben einfacher.</span><span class="sxs-lookup"><span data-stu-id="684e8-117">These predefined buttons make life easier.</span></span>


```C++
        <PLAYELEMENT
            mappingColor = "#00FF00" />
                          
        <STOPELEMENT
            mappingColor = "#FF0000" />

```



<span data-ttu-id="684e8-118">Fügen Sie schließlich dem playelement ein OnClick-Ereignis hinzu, um eine Wiedergabeliste in der zweiten Ansicht anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="684e8-118">Finally, add an onClick event to the PLAYELEMENT to display a playlist in the second view:</span></span>


```C++
            onClick = "JScript: theme.openView('playview');" />

```



<span data-ttu-id="684e8-119">Im Beispiel Abschnitt des SDK sehen Sie eine ähnliche funktionierende Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="684e8-119">You can see a similar working playlist skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="684e8-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="684e8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="684e8-121">**Leitfaden zum Erstellen von Skin**</span><span class="sxs-lookup"><span data-stu-id="684e8-121">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




