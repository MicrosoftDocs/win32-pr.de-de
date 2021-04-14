---
title: Iagentcharacter GetSize
description: Iagentcharacter GetSize
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e40c219cd0a1dc1d11738149ca7cfd9869fe682e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311597"
---
# <a name="iagentcharactergetsize"></a><span data-ttu-id="e27e7-103">Iagentcharacter:: GetSize</span><span class="sxs-lookup"><span data-stu-id="e27e7-103">IAgentCharacter::GetSize</span></span>

<span data-ttu-id="e27e7-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e27e7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

<span data-ttu-id="e27e7-105">Ruft die Größe des Animations Rahmens des Zeichens ab.</span><span class="sxs-lookup"><span data-stu-id="e27e7-105">Retrieves the size of the character's animation frame.</span></span>

-   <span data-ttu-id="e27e7-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="e27e7-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e27e7-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plwidth*</span><span class="sxs-lookup"><span data-stu-id="e27e7-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="e27e7-108">Die Adresse einer Variablen, die die Breite des Zeichen Animations Rahmens in Pixel relativ zum Bildschirm Ursprung (oben links) empfängt.</span><span class="sxs-lookup"><span data-stu-id="e27e7-108">Address of a variable that receives the width of the character animation frame in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="e27e7-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plheight*</span><span class="sxs-lookup"><span data-stu-id="e27e7-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="e27e7-110">Die Adresse einer Variablen, die die Höhe des Zeichen Animations Rahmens in Pixel relativ zum Bildschirm Ursprung (oben links) empfängt.</span><span class="sxs-lookup"><span data-stu-id="e27e7-110">Address of a variable that receives the height of the character animation frame in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="e27e7-111">Obwohl das Zeichen in einem unregelmäßig formatierte Regions Fenster angezeigt wird, basiert der Speicherort des Zeichens auf seinem rechteckigen Animations Rahmen.</span><span class="sxs-lookup"><span data-stu-id="e27e7-111">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="e27e7-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e27e7-112">See Also</span></span>

[<span data-ttu-id="e27e7-113">**Iagentcharacter:: SetSize**</span><span class="sxs-lookup"><span data-stu-id="e27e7-113">**IAgentCharacter::SetSize**</span></span>](iagentcharacter--setsize.md)


 

 




