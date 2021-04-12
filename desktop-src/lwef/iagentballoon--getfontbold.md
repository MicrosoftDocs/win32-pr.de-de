---
title: Iagentballoon getfontbold
description: Iagentballoon getfontbold
ms.assetid: 5a55f771-d68e-4f66-8001-47c141661b06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858f6f42964db1bdd7ae548d308c6f6668b05631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206931"
---
# <a name="iagentballoongetfontbold"></a><span data-ttu-id="842d6-103">Iagentballoon:: getfontbold</span><span class="sxs-lookup"><span data-stu-id="842d6-103">IAgentBalloon::GetFontBold</span></span>

<span data-ttu-id="842d6-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="842d6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontBold(
   long * pbFontBold  // address of variable for bold setting for
);                    // font displayed in word balloon 
```

<span data-ttu-id="842d6-105">Gibt an, ob die in einer Word-Sprechblase verwendete Schriftart fett formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="842d6-105">Indicates whether the font used in a word balloon is bold.</span></span>

-   <span data-ttu-id="842d6-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="842d6-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="842d6-107"><span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbfontbold*</span><span class="sxs-lookup"><span data-stu-id="842d6-107"><span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbFontBold*</span></span>
</dt> <dd>

<span data-ttu-id="842d6-108">Die Adresse eines Werts, der **true** erhält, wenn die Schriftart fett formatiert ist, und **false** , wenn Sie ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="842d6-108">The address of a value that receives **True** if the font is bold and **False** if not bold.</span></span>

</dd> </dl>

<span data-ttu-id="842d6-109">Der Schriftart Stil, der in einer Wort Sprechblase verwendet wird, wird im Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="842d6-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="842d6-110">Sie kann nicht von einer Anwendung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="842d6-110">It cannot be changed by an application.</span></span> <span data-ttu-id="842d6-111">Der Benutzer kann jedoch die Schriftart Einstellungen für alle Zeichen über die Eigenschaften Seite des Microsoft-Agents überschreiben.</span><span class="sxs-lookup"><span data-stu-id="842d6-111">However, the user can override the font settings for all characters through the Microsoft Agent property sheet.</span></span>

 

 




