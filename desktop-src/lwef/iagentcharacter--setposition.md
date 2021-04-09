---
title: Iagentcharacter-SetPosition
description: Iagentcharacter-SetPosition
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aee48ea26c714c570f7ae11b9b2dbc0fe92ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036742"
---
# <a name="iagentcharactersetposition"></a><span data-ttu-id="13378-103">Iagentcharacter:: SetPosition</span><span class="sxs-lookup"><span data-stu-id="13378-103">IAgentCharacter::SetPosition</span></span>

<span data-ttu-id="13378-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="13378-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

<span data-ttu-id="13378-105">Legt die Position des Animations Rahmens des Zeichens fest.</span><span class="sxs-lookup"><span data-stu-id="13378-105">Sets the position of the character's animation frame.</span></span>

-   <span data-ttu-id="13378-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="13378-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="13378-107"><span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lleft*</span><span class="sxs-lookup"><span data-stu-id="13378-107"><span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*</span></span>
</dt> <dd>

<span data-ttu-id="13378-108">Die Bildschirm Koordinate der linken Kante des Zeichen Animations Rahmens in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="13378-108">Screen coordinate of the character animation frame's left edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="13378-109"><span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*LTOP*</span><span class="sxs-lookup"><span data-stu-id="13378-109"><span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*</span></span>
</dt> <dd>

<span data-ttu-id="13378-110">Die Bildschirm Koordinate der oberen Kante des Zeichen Animations Rahmens in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="13378-110">Screen coordinate of the character animation frame's top edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="13378-111">Diese Eigenschafts Einstellung gilt für alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="13378-111">This property's setting applies to all clients of the character.</span></span> <span data-ttu-id="13378-112">Obwohl das Zeichen in einem unregelmäßig formatierte Regions Fenster angezeigt wird, basiert der Speicherort des Zeichens auf seinem rechteckigen Animations Rahmen.</span><span class="sxs-lookup"><span data-stu-id="13378-112">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

> [!Note]  
> <span data-ttu-id="13378-113">Anders als bei der Methode " [**muveto**](https://www.bing.com/search?q=**MoveTo**) " wird diese Funktion nicht in die Warteschlange gestellt.</span><span class="sxs-lookup"><span data-stu-id="13378-113">Unlike the [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) method, this function is not queued.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="13378-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="13378-114">See Also</span></span>

[<span data-ttu-id="13378-115">**Iagentcharacter:: GetPosition**</span><span class="sxs-lookup"><span data-stu-id="13378-115">**IAgentCharacter::GetPosition**</span></span>](iagentcharacter--getposition.md)


 

 




