---
title: Iagentballoon getFont-Unterstreichung
description: Iagentballoon getFont-Unterstreichung
ms.assetid: 19886e94-8095-4650-bd88-34ea9d96ddaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5acf35453209679dc96c85b3017fbe76b19d53b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037549"
---
# <a name="iagentballoongetfontunderline"></a><span data-ttu-id="d4a83-103">Iagentballoon:: getFont-Unterstreichung</span><span class="sxs-lookup"><span data-stu-id="d4a83-103">IAgentBalloon::GetFontUnderline</span></span>

<span data-ttu-id="d4a83-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="d4a83-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontUnderline(
   long * pbFontUnderline  // address of variable for underline setting
);                         // for font displayed in word balloon 
```

<span data-ttu-id="d4a83-105">Gibt an, ob die in einer Word-Sprechblase verwendete Schriftart den Stil für die Unterstreichung hat.</span><span class="sxs-lookup"><span data-stu-id="d4a83-105">Indicates whether the font used in a word balloon has the underline style set.</span></span>

-   <span data-ttu-id="d4a83-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="d4a83-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d4a83-107"><span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbfont-Unterstreichung*</span><span class="sxs-lookup"><span data-stu-id="d4a83-107"><span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbFontUnderline*</span></span>
</dt> <dd>

<span data-ttu-id="d4a83-108">Die Adresse eines Werts, der **true** empfängt, wenn der Stil der Schrift Unterstreichung festgelegt ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="d4a83-108">The address of a value that receives **True** if the font underline style is set and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="d4a83-109">Der Schriftart Stil, der in einer Wort Sprechblase verwendet wird, wird im Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="d4a83-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="d4a83-110">Sie kann nicht von einer Anwendung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d4a83-110">It cannot be changed by an application.</span></span> <span data-ttu-id="d4a83-111">Der Benutzer kann jedoch die Schriftart Einstellungen für alle Zeichen überschreiben, indem er das Eigenschaften Blatt Microsoft-Agent verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4a83-111">However, the user can override the font settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




