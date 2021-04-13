---
title: Iagentcharacter GetPosition
description: Iagentcharacter GetPosition
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cdff0d6876fc7257e05014f3d9ba695db5d168
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311598"
---
# <a name="iagentcharactergetposition"></a><span data-ttu-id="47096-103">Iagentcharacter:: GetPosition</span><span class="sxs-lookup"><span data-stu-id="47096-103">IAgentCharacter::GetPosition</span></span>

<span data-ttu-id="47096-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="47096-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

<span data-ttu-id="47096-105">Ruft die Animations Frame Position des Zeichens ab.</span><span class="sxs-lookup"><span data-stu-id="47096-105">Retrieves the character's animation frame position.</span></span>

-   <span data-ttu-id="47096-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="47096-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="47096-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plleft*</span><span class="sxs-lookup"><span data-stu-id="47096-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="47096-108">Adresse einer Variablen, die die Bildschirm Koordinate der linken Kante des Zeichen Animations Rahmens in Pixel relativ zum Bildschirm Ursprung empfängt (oben links).</span><span class="sxs-lookup"><span data-stu-id="47096-108">Address of a variable that receives the screen coordinate of the character animation frame's left edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="47096-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*pltop*</span><span class="sxs-lookup"><span data-stu-id="47096-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="47096-110">Adresse einer Variablen, die die Bildschirm Koordinate des oberen Rands des Zeichen Animations Rahmens in Pixel relativ zum Bildschirm Ursprung empfängt (oben links).</span><span class="sxs-lookup"><span data-stu-id="47096-110">Address of a variable that receives the screen coordinate of the character animation frame's top edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="47096-111">Obwohl das Zeichen in einem unregelmäßig formatierte Regions Fenster angezeigt wird, basiert der Speicherort des Zeichens auf seinem rechteckigen Animations Rahmen.</span><span class="sxs-lookup"><span data-stu-id="47096-111">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="47096-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="47096-112">See Also</span></span>

<span data-ttu-id="47096-113">[**Iagentcharacter:: SetPosition**](iagentcharacter--setposition.md), [ **iagentcharacter:: GetSize**](iagentcharacter--getsize.md)</span><span class="sxs-lookup"><span data-stu-id="47096-113">[**IAgentCharacter::SetPosition**](iagentcharacter--setposition.md), [**IAgentCharacter::GetSize**](iagentcharacter--getsize.md)</span></span>


 

 




