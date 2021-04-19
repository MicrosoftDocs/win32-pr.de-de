---
title: Iagentballoon getForeColor
description: Iagentballoon getForeColor
ms.assetid: b06ad924-66b6-42a6-8c97-5bc4c46f6e2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7a251471b0281661b087dbfb9b141c54ff9dc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341677"
---
# <a name="iagentballoongetforecolor"></a><span data-ttu-id="718f3-103">Iagentballoon:: getForeColor</span><span class="sxs-lookup"><span data-stu-id="718f3-103">IAgentBalloon::GetForeColor</span></span>

<span data-ttu-id="718f3-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="718f3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetForeColor(
   long * plFGColor // address of variable for foreground color displayed
);                  // in word balloon
```

<span data-ttu-id="718f3-105">Ruft den Wert für die Vordergrundfarbe ab, die in einer Wort Sprechblase angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="718f3-105">Retrieves the value for the foreground color displayed in a word balloon.</span></span>

-   <span data-ttu-id="718f3-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="718f3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="718f3-107"><span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*PLF-Farbe*</span><span class="sxs-lookup"><span data-stu-id="718f3-107"><span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*</span></span>
</dt> <dd>

<span data-ttu-id="718f3-108">Die Adresse einer Variablen, die die Farbeinstellung für den Sprechblasen-Vordergrund empfängt.</span><span class="sxs-lookup"><span data-stu-id="718f3-108">The address of a variable that receives the color setting for the balloon foreground.</span></span>

</dd> </dl>

<span data-ttu-id="718f3-109">Die in einer Wort Sprechblase verwendete Vordergrundfarbe wird im Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="718f3-109">The foreground color used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="718f3-110">Sie kann nicht von einer Anwendung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="718f3-110">It cannot be changed by an application.</span></span> <span data-ttu-id="718f3-111">Der Benutzer kann jedoch die Vordergrundfarbe der Wort Ballons für alle Zeichen über die Eigenschaften Seite des Microsoft-Agents überschreiben.</span><span class="sxs-lookup"><span data-stu-id="718f3-111">However, the user can override the foreground color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="718f3-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="718f3-112">See Also</span></span>

[<span data-ttu-id="718f3-113">**Iagentballoon:: GetBackColor**</span><span class="sxs-lookup"><span data-stu-id="718f3-113">**IAgentBalloon::GetBackColor**</span></span>](iagentballoon--getbackcolor.md)


 

 




