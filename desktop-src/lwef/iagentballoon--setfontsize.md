---
title: Iagentballoon SetFontSize
description: Iagentballoon SetFontSize
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4984382408739e2d093226d04b1c99582a1a25d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311214"
---
# <a name="iagentballoonsetfontsize"></a><span data-ttu-id="53e92-103">Iagentballoon:: SetFontSize</span><span class="sxs-lookup"><span data-stu-id="53e92-103">IAgentBalloon::SetFontSize</span></span>

<span data-ttu-id="53e92-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="53e92-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in word balloon
); 
```

<span data-ttu-id="53e92-105">Legt die Größe der Schriftart fest, die in der Word-Sprechblase angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="53e92-105">Sets the size of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="53e92-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="53e92-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="53e92-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lfontsize*</span><span class="sxs-lookup"><span data-stu-id="53e92-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="53e92-108">Der Schriftgrad.</span><span class="sxs-lookup"><span data-stu-id="53e92-108">The size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="53e92-109">Der Standardschrift Grad, der in der Wort Sprechblase eines Zeichens verwendet wird, wird im Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="53e92-109">The default font size used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="53e92-110">Sie können es mit **iagentballoon:: SetFontSize** ändern.</span><span class="sxs-lookup"><span data-stu-id="53e92-110">You can change it with **IAgentBalloon::SetFontSize**.</span></span> <span data-ttu-id="53e92-111">Der Benutzer kann jedoch die Einstellung für die Schriftgröße für alle Zeichen überschreiben, indem er das Eigenschaften Blatt "Microsoft-Agent" verwendet.</span><span class="sxs-lookup"><span data-stu-id="53e92-111">However, the user can override the font size setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="53e92-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="53e92-112">See Also</span></span>

[<span data-ttu-id="53e92-113">**Iagentballoon:: GetFontSize**</span><span class="sxs-lookup"><span data-stu-id="53e92-113">**IAgentBalloon::GetFontSize**</span></span>](iagentballoon--getfontsize.md)


 

 




