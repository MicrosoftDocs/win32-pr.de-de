---
title: Iagentballoon GetBackColor
description: Iagentballoon GetBackColor
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce886c9929892c89b56f162f784dc27a472209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037160"
---
# <a name="iagentballoongetbackcolor"></a><span data-ttu-id="85294-103">Iagentballoon:: GetBackColor</span><span class="sxs-lookup"><span data-stu-id="85294-103">IAgentBalloon::GetBackColor</span></span>

<span data-ttu-id="85294-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="85294-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

<span data-ttu-id="85294-105">Ruft den Wert für die in einer Wort Sprechblase angezeigte Hintergrundfarbe ab.</span><span class="sxs-lookup"><span data-stu-id="85294-105">Retrieves the value for the background color displayed in a word balloon.</span></span>

-   <span data-ttu-id="85294-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="85294-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="85294-107"><span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plbgcolor*</span><span class="sxs-lookup"><span data-stu-id="85294-107"><span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*</span></span>
</dt> <dd>

<span data-ttu-id="85294-108">Die Adresse einer Variablen, die die Farbeinstellung für den Hintergrund der Sprechblase empfängt.</span><span class="sxs-lookup"><span data-stu-id="85294-108">The address of a variable that receives the color setting for the balloon background.</span></span>

</dd> </dl>

<span data-ttu-id="85294-109">Die in einer Wort Sprechblase verwendete Hintergrundfarbe wird im Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="85294-109">The background color used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="85294-110">Sie kann nicht von einer Anwendung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="85294-110">It cannot be changed by an application.</span></span> <span data-ttu-id="85294-111">Der Benutzer kann jedoch die Hintergrundfarbe der Wort Blasen für alle Zeichen über die Eigenschaften Seite des Microsoft-Agents ändern.</span><span class="sxs-lookup"><span data-stu-id="85294-111">However, the user can change the background color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="85294-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="85294-112">See Also</span></span>

[<span data-ttu-id="85294-113">**Iagentballoon:: getForeColor**</span><span class="sxs-lookup"><span data-stu-id="85294-113">**IAgentBalloon::GetForeColor**</span></span>](iagentballoon--getforecolor.md)


 

 




