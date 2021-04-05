---
title: Iagentcharacter setSize
description: Iagentcharacter setSize
ms.assetid: 8324ab84-2b59-4459-b375-700d72b621bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39d5b33afa7ff59516b793f194a0ba186c2e002
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713187"
---
# <a name="iagentcharactersetsize"></a><span data-ttu-id="3a374-103">Iagentcharacter:: SetSize</span><span class="sxs-lookup"><span data-stu-id="3a374-103">IAgentCharacter::SetSize</span></span>

<span data-ttu-id="3a374-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="3a374-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSize(
   long * lWidth,  // width of the character frame
   long * lHeight  // height of the character frame
);
```

<span data-ttu-id="3a374-105">Legt die Größe des Animations Rahmens des Zeichens fest.</span><span class="sxs-lookup"><span data-stu-id="3a374-105">Sets the size of the character's animation frame.</span></span>

-   <span data-ttu-id="3a374-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="3a374-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3a374-107"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lwidth*</span><span class="sxs-lookup"><span data-stu-id="3a374-107"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span></span>
</dt> <dd>

<span data-ttu-id="3a374-108">Die Breite des Animations Rahmens des Zeichens in Pixel.</span><span class="sxs-lookup"><span data-stu-id="3a374-108">The width of the character's animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="3a374-109"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lheight*</span><span class="sxs-lookup"><span data-stu-id="3a374-109"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span></span>
</dt> <dd>

<span data-ttu-id="3a374-110">Die Höhe des Animations Rahmens des Zeichens in Pixel.</span><span class="sxs-lookup"><span data-stu-id="3a374-110">The height of the character's animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="3a374-111">Wenn Sie die Frame Größe des Zeichens ändern, wird das Zeichen in die mit dieser Methode festgelegte Größe skaliert.</span><span class="sxs-lookup"><span data-stu-id="3a374-111">Changing the character's frame size scales the character to the size set with this method.</span></span> <span data-ttu-id="3a374-112">Diese Eigenschafts Einstellung gilt für alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="3a374-112">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="3a374-113">Obwohl das Zeichen in einem unregelmäßig formatierte Regions Fenster angezeigt wird, basiert der Speicherort des Zeichens auf seinem rechteckigen Animations Rahmen.</span><span class="sxs-lookup"><span data-stu-id="3a374-113">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a374-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3a374-114">See Also</span></span>

[<span data-ttu-id="3a374-115">**Iagentcharacter:: GetSize**</span><span class="sxs-lookup"><span data-stu-id="3a374-115">**IAgentCharacter::GetSize**</span></span>](iagentcharacter--getsize.md)


 

 




