---
title: Iagentballoon setfontname
description: Iagentballoon setfontname
ms.assetid: 6babf5f6-2abd-46c2-ade0-899a8e4488bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f983064c5df8cde8322658bbd0c713bbf238ecf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037547"
---
# <a name="iagentballoonsetfontname"></a><span data-ttu-id="a1cf0-103">Iagentballoon:: setfontname</span><span class="sxs-lookup"><span data-stu-id="a1cf0-103">IAgentBalloon::SetFontName</span></span>

<span data-ttu-id="a1cf0-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="a1cf0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font displayed in word balloon
);
                   
```

<span data-ttu-id="a1cf0-105">Legt die in der Wort Sprechblase angezeigte Schriftart fest.</span><span class="sxs-lookup"><span data-stu-id="a1cf0-105">Sets the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="a1cf0-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a1cf0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a1cf0-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszfontname*</span><span class="sxs-lookup"><span data-stu-id="a1cf0-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="a1cf0-108">Ein BSTR, das die in der Wort Sprechblase angezeigte Schriftart festlegt.</span><span class="sxs-lookup"><span data-stu-id="a1cf0-108">A BSTR that sets the font displayed in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="a1cf0-109">Die in der Wort Sprechblase eines Zeichens verwendete Standard Schriftart wird im Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="a1cf0-109">The default font used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="a1cf0-110">Sie können es mit **iagentballoon:: setfontname** ändern.</span><span class="sxs-lookup"><span data-stu-id="a1cf0-110">You can change it with **IAgentBalloon::SetFontName**.</span></span> <span data-ttu-id="a1cf0-111">Der Benutzer kann jedoch die Schriftart Einstellung für alle Zeichen mithilfe des Eigenschaften Blatts Microsoft-Agent überschreiben.</span><span class="sxs-lookup"><span data-stu-id="a1cf0-111">However, the user can override the font setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1cf0-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a1cf0-112">See Also</span></span>

[<span data-ttu-id="a1cf0-113">**Iagentballoon:: getVisible**</span><span class="sxs-lookup"><span data-stu-id="a1cf0-113">**IAgentBalloon::GetVisible**</span></span>](iagentballoon--getvisible.md)


 

 




