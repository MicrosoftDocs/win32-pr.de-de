---
title: Iagentballoon getfontitalic
description: Iagentballoon getfontitalic
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c1a0e1e649e325e84d4a78eee087e102e8d1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340835"
---
# <a name="iagentballoongetfontitalic"></a><span data-ttu-id="4cff0-103">Iagentballoon:: getfontitalic</span><span class="sxs-lookup"><span data-stu-id="4cff0-103">IAgentBalloon::GetFontItalic</span></span>

<span data-ttu-id="4cff0-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="4cff0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontItalic(
   long * pbFontItalic  // address of variable for italic setting for 
);                      // font displayed in word balloon 
```

<span data-ttu-id="4cff0-105">Gibt an, ob die in einer Word-Sprechblase verwendete Schriftart kursiv formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="4cff0-105">Indicates whether the font used in a word balloon is italic.</span></span>

-   <span data-ttu-id="4cff0-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="4cff0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4cff0-107"><span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbfontitalic*</span><span class="sxs-lookup"><span data-stu-id="4cff0-107"><span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*</span></span>
</dt> <dd>

<span data-ttu-id="4cff0-108">Die Adresse eines Werts, der **true** erhält, wenn die Schriftart kursiv ist, und **false** , wenn Sie nicht kursiv formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="4cff0-108">The address of a value that receives **True** if the font is italic and **False** if not italic.</span></span>

</dd> </dl>

<span data-ttu-id="4cff0-109">Der Schriftart Stil, der in der Wort Sprechblase eines Zeichens verwendet wird, wird im Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="4cff0-109">The font style used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="4cff0-110">Sie kann nicht von einer Anwendung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4cff0-110">It cannot be changed by an application.</span></span> <span data-ttu-id="4cff0-111">Der Benutzer kann jedoch die Schriftart Einstellungen für alle Zeichen über die Eigenschaften Seite des Microsoft-Agents überschreiben.</span><span class="sxs-lookup"><span data-stu-id="4cff0-111">However, the user can override the font settings for all characters through the Microsoft Agent property sheet.</span></span>

 

 




