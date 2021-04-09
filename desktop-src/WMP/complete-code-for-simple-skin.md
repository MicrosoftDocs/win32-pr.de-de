---
title: Vervollständigen von Code für einfache Skin
description: Vervollständigen von Code für einfache Skin
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- Erstellen von Skins, Codebeispielen
- Windows Media Player Skins, Codebeispiele
- Skins, Codebeispiele
- Skin-Definitions Dateien, Codebeispiele
- Erstellen von Skins, Beispiele
- Windows Media Player Skins, Beispiele
- Skins, Beispiele
- Skin-Definitions Dateien, Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3682e6143c751d1c72cd8799f849fef7c9c27adb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856443"
---
# <a name="complete-code-for-simple-skin"></a><span data-ttu-id="d2e92-111">Vervollständigen von Code für einfache Skin</span><span class="sxs-lookup"><span data-stu-id="d2e92-111">Complete Code for Simple Skin</span></span>

<span data-ttu-id="d2e92-112">Im folgenden finden Sie den gesamten Code für die erste Beispiel Skin:</span><span class="sxs-lookup"><span data-stu-id="d2e92-112">Here is the complete code for the first sample skin:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick="JScript: player.URL='https://proseware.com/laure.wma';" />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick = "JScript: view.close(); " />
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



<span data-ttu-id="d2e92-113">Nun haben Sie alle Teile zusammengestellt.</span><span class="sxs-lookup"><span data-stu-id="d2e92-113">Now you have all the pieces put together.</span></span>

<span data-ttu-id="d2e92-114">Erstellen Sie eine komprimierte Datei mit der Dateinamenerweiterung ". zip".</span><span class="sxs-lookup"><span data-stu-id="d2e92-114">Create a compressed file with a .zip file name extension.</span></span> <span data-ttu-id="d2e92-115">Diese komprimierte Datei enthält Ihre Skin-Definitionsdatei, Bitmaps und alle Digital Media-Dateien, die Sie einschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="d2e92-115">This compressed file contains your skin definition file, bitmaps, and any digital media files you want to include.</span></span> <span data-ttu-id="d2e92-116">Benennen Sie die Datei so um, dass Sie die Dateinamenerweiterung. WMZ enthält.</span><span class="sxs-lookup"><span data-stu-id="d2e92-116">Rename the file so that it has a .wmz file name extension.</span></span> <span data-ttu-id="d2e92-117">Wenn Sie dann auf die komprimierte Skin doppelklicken, wird Sie gestartet.</span><span class="sxs-lookup"><span data-stu-id="d2e92-117">Then double-clicking your compressed skin will start it playing.</span></span>

<span data-ttu-id="d2e92-118">Im Abschnitt mit den Beispielen des SDK sehen Sie eine ähnliche Arbeits einfache Skin.</span><span class="sxs-lookup"><span data-stu-id="d2e92-118">You can see a similar working simple skin in the samples section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2e92-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d2e92-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2e92-120">**Erstellen der Skin-Definitionsdatei**</span><span class="sxs-lookup"><span data-stu-id="d2e92-120">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




