---
title: Iagentballoon getfontname
description: Iagentballoon getfontname
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f29ad981fb4b10249b17e55c92fb286552eedc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388719"
---
# <a name="iagentballoongetfontname"></a><span data-ttu-id="15ff0-103">Iagentballoon:: getfontname</span><span class="sxs-lookup"><span data-stu-id="15ff0-103">IAgentBalloon::GetFontName</span></span>

<span data-ttu-id="15ff0-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="15ff0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in word balloon
```

<span data-ttu-id="15ff0-105">Ruft den Wert für die Schriftart ab, die in einer Word-Sprechblase angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="15ff0-105">Retrieves the value for the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="15ff0-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="15ff0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="15ff0-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszfontname*</span><span class="sxs-lookup"><span data-stu-id="15ff0-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="15ff0-108">Die Adresse eines BSTR, der den in einer Wort Sprechblase angezeigten Schriftart Namen empfängt.</span><span class="sxs-lookup"><span data-stu-id="15ff0-108">The address of a BSTR that receives the font name displayed in a word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="15ff0-109">Die in einer Wort Sprechblase verwendete Standard Schriftart wird im Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="15ff0-109">The default font used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="15ff0-110">Sie können es mit [**iagentballoon:: setfontname**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**)ändern.</span><span class="sxs-lookup"><span data-stu-id="15ff0-110">You can change it with [**IAgentBalloon::SetFontName**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**).</span></span> <span data-ttu-id="15ff0-111">Der Benutzer kann die Schriftart Einstellung für alle Zeichen mithilfe des Eigenschaften Blatts Microsoft-Agent überschreiben.</span><span class="sxs-lookup"><span data-stu-id="15ff0-111">The user can override the font setting for all characters using the Microsoft Agent property sheet.</span></span>

 

 




