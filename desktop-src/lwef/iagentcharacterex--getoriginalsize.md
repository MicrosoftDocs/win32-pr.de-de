---
title: Iagentcharakteriex getoriginalsize
description: Iagentcharakteriex getoriginalsize
ms.assetid: a27ae88f-3655-4375-b563-0cc320d012cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e1712587e70d9756e3d37ca9e0f3cbfdb82c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036778"
---
# <a name="iagentcharacterexgetoriginalsize"></a><span data-ttu-id="005f1-103">Iagentcharakteriex:: getoriginalsize</span><span class="sxs-lookup"><span data-stu-id="005f1-103">IAgentCharacterEx::GetOriginalSize</span></span>

<span data-ttu-id="005f1-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="005f1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetOriginalSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

<span data-ttu-id="005f1-105">Ruft die ursprüngliche Größe des Animations Rahmens des Zeichens ab.</span><span class="sxs-lookup"><span data-stu-id="005f1-105">Retrieves the original size of the character's animation frame.</span></span>

-   <span data-ttu-id="005f1-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="005f1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="005f1-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plwidth*</span><span class="sxs-lookup"><span data-stu-id="005f1-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="005f1-108">Adresse einer Variablen, die die ursprüngliche Breite des Zeichen Animations Rahmens in Pixel empfängt.</span><span class="sxs-lookup"><span data-stu-id="005f1-108">Address of a variable that receives the original width of the character animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="005f1-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plheight*</span><span class="sxs-lookup"><span data-stu-id="005f1-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="005f1-110">Adresse einer Variablen, die die ursprüngliche Höhe des Zeichen Animations Rahmens in Pixel empfängt.</span><span class="sxs-lookup"><span data-stu-id="005f1-110">Address of a variable that receives the original height of the character animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="005f1-111">Dieser Befehl gibt die ursprüngliche Größe des Zeichen Rahmens zurück, wie er im Microsoft-Agent-Zeichen-Editor erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="005f1-111">This call returns the original size of the character frame as built in the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="005f1-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="005f1-112">See Also</span></span>

[<span data-ttu-id="005f1-113">**Iagentcharacter:: GetSize**</span><span class="sxs-lookup"><span data-stu-id="005f1-113">**IAgentCharacter::GetSize**</span></span>](iagentcharacter--getsize.md)


 

 




