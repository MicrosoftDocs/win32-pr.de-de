---
title: Iagentballoon GetFontSize
description: Iagentballoon GetFontSize
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14b1a921f1f5c9927f58ab9e561569ba3bc98fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207400"
---
# <a name="iagentballoongetfontsize"></a><span data-ttu-id="b353b-103">Iagentballoon:: GetFontSize</span><span class="sxs-lookup"><span data-stu-id="b353b-103">IAgentBalloon::GetFontSize</span></span>

<span data-ttu-id="b353b-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="b353b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in word balloon 
```

<span data-ttu-id="b353b-105">Ruft den Wert für die Größe der Schriftart ab, die in einer Word-Sprechblase angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b353b-105">Retrieves the value for the size of the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="b353b-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b353b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b353b-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plfontsize*</span><span class="sxs-lookup"><span data-stu-id="b353b-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="b353b-108">Die Adresse eines Werts, der die Größe der Schriftart erhält.</span><span class="sxs-lookup"><span data-stu-id="b353b-108">The address of a value that receives the size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="b353b-109">Der in einer Wort Sprechblase verwendete Standardschrift Grad wird im Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="b353b-109">The default font size used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="b353b-110">Sie können es mit [**iagentballoon:: SetFontSize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**)ändern.</span><span class="sxs-lookup"><span data-stu-id="b353b-110">You can change it with [**IAgentBalloon::SetFontSize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**).</span></span> <span data-ttu-id="b353b-111">Der Benutzer kann jedoch die Schriftart Größen Einstellungen für alle Zeichen überschreiben, indem er das Eigenschaften Blatt "Microsoft-Agent" verwendet.</span><span class="sxs-lookup"><span data-stu-id="b353b-111">However, the user can override the font size settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




