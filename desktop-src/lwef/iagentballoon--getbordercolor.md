---
title: Iagentballoon getBorderColor
description: Iagentballoon getBorderColor
ms.assetid: e6c592c3-0e14-474f-a829-6028f2de5791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f78bf9425cbb12c6a87f3ad64b6c5523dc7bbd8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712047"
---
# <a name="iagentballoongetbordercolor"></a><span data-ttu-id="22a48-103">Iagentballoon:: getBorderColor</span><span class="sxs-lookup"><span data-stu-id="22a48-103">IAgentBalloon::GetBorderColor</span></span>

<span data-ttu-id="22a48-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="22a48-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetBorderColor (
  long * plBorderColor// address of variable for border color displayed
);                    // for word balloon
```

<span data-ttu-id="22a48-105">Ruft den Wert für die Rahmenfarbe ab, die für eine Wort Sprechblase angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="22a48-105">Retrieves the value for the border color displayed for a word balloon.</span></span>

-   <span data-ttu-id="22a48-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="22a48-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="22a48-107"><span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plbordercolor*</span><span class="sxs-lookup"><span data-stu-id="22a48-107"><span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*</span></span>
</dt> <dd>

<span data-ttu-id="22a48-108">Die Adresse einer Variablen, die die Farbeinstellung für den Sprechblasen Rahmen empfängt.</span><span class="sxs-lookup"><span data-stu-id="22a48-108">The address of a variable that receives the color setting for the balloon border.</span></span>

</dd> </dl>

<span data-ttu-id="22a48-109">Die Rahmenfarbe für eine Zeichen Wort Sprechblase wird im Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="22a48-109">The border color for a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="22a48-110">Sie kann nicht von einer Anwendung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="22a48-110">It cannot be changed by an application.</span></span> <span data-ttu-id="22a48-111">Der Benutzer kann jedoch die Rahmenfarbe der Wort Blasen für alle Zeichen über das Eigenschaften Blatt "Microsoft-Agent" ändern.</span><span class="sxs-lookup"><span data-stu-id="22a48-111">However, the user can change the border color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="22a48-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="22a48-112">See Also</span></span>

<span data-ttu-id="22a48-113">[**Iagentballoon:: GetBackColor**](iagentballoon--getbackcolor.md), [ **iagentballoon:: getForeColor**](iagentballoon--getforecolor.md)</span><span class="sxs-lookup"><span data-stu-id="22a48-113">[**IAgentBalloon::GetBackColor**](iagentballoon--getbackcolor.md), [**IAgentBalloon::GetForeColor**](iagentballoon--getforecolor.md)</span></span>


 

 




