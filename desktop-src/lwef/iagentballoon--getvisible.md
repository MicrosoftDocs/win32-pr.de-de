---
title: Iagentballoon getVisible
description: Iagentballoon getVisible
ms.assetid: 328af211-4ea4-482c-8487-42c8e4cd66b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55fd8dbf6792d34b15f82ab6c402e9a0e7eb3ad3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856875"
---
# <a name="iagentballoongetvisible"></a><span data-ttu-id="6d4b8-103">Iagentballoon:: getVisible</span><span class="sxs-lookup"><span data-stu-id="6d4b8-103">IAgentBalloon::GetVisible</span></span>

<span data-ttu-id="6d4b8-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="6d4b8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for word balloon
);                   // Visible setting
```

<span data-ttu-id="6d4b8-105">Bestimmt, ob die Wort Sprechblase sichtbar oder ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="6d4b8-105">Determines whether the word balloon is visible or hidden.</span></span>

-   <span data-ttu-id="6d4b8-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="6d4b8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="6d4b8-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbvisible*</span><span class="sxs-lookup"><span data-stu-id="6d4b8-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="6d4b8-108">Adresse einer Variablen, die **true** empfängt, wenn die Wort Sprechblase sichtbar ist, und **false** , wenn Sie ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="6d4b8-108">Address of a variable that receives **True** if the word balloon is visible and **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="6d4b8-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6d4b8-109">See Also</span></span>

[<span data-ttu-id="6d4b8-110">**Iagentballoon:: setVisible**</span><span class="sxs-lookup"><span data-stu-id="6d4b8-110">**IAgentBalloon::SetVisible**</span></span>](iagentballoon--setvisible.md)


 

 




