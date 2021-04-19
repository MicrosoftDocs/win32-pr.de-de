---
title: Iagentpropertysheet GetPosition
description: Iagentpropertysheet GetPosition
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff4dcac994901824d7dc37868d7fcfc3f39cefd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342277"
---
# <a name="iagentpropertysheetgetposition"></a><span data-ttu-id="fd217-103">Iagentpropertysheet:: GetPosition</span><span class="sxs-lookup"><span data-stu-id="fd217-103">IAgentPropertySheet::GetPosition</span></span>

<span data-ttu-id="fd217-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="fd217-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of property sheet
   long * plTop    // address of variable for top edge of property sheet
);
```

<span data-ttu-id="fd217-105">Ruft die Position des Eigenschaften Blatt Fensters des Microsoft-Agents ab.</span><span class="sxs-lookup"><span data-stu-id="fd217-105">Retrieves the Microsoft Agent's property sheet window position.</span></span>

-   <span data-ttu-id="fd217-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="fd217-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="fd217-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plleft*</span><span class="sxs-lookup"><span data-stu-id="fd217-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="fd217-108">Adresse einer Variablen, die die Bildschirm Koordinate des linken Rands des Eigenschaften Blatts in Pixel relativ zum Bildschirm Ursprung empfängt (oben links).</span><span class="sxs-lookup"><span data-stu-id="fd217-108">Address of a variable that receives the screen coordinate of the left edge of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="fd217-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*pltop*</span><span class="sxs-lookup"><span data-stu-id="fd217-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="fd217-110">Adresse einer Variablen, die die Bildschirm Koordinate des oberen Rands des Eigenschaften Blatts in Pixel relativ zum Bildschirm Ursprung empfängt (oben links).</span><span class="sxs-lookup"><span data-stu-id="fd217-110">Address of a variable that receives the screen coordinate of the top edge of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="fd217-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fd217-111">See Also</span></span>

[<span data-ttu-id="fd217-112">**Iagentpropertysheet:: GetSize**</span><span class="sxs-lookup"><span data-stu-id="fd217-112">**IAgentPropertySheet::GetSize**</span></span>](iagentpropertysheet--getsize.md)


 

 




