---
title: Iagentballoon getnumlines
description: Iagentballoon getnumlines
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d66c18d75af77a2559efc86f775710fb32e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388716"
---
# <a name="iagentballoongetnumlines"></a><span data-ttu-id="5a14a-103">Iagentballoon:: getnumlines</span><span class="sxs-lookup"><span data-stu-id="5a14a-103">IAgentBalloon::GetNumLines</span></span>

<span data-ttu-id="5a14a-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="5a14a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetNumLines(
   long * pcLines  // address of variable for number of lines 
);                  // displayed in word balloon
```

<span data-ttu-id="5a14a-105">Ruft den Wert der Anzahl der Zeilen ab, die in einer Wort Sprechblase angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5a14a-105">Retrieves the value of the number of lines displayed in a word balloon.</span></span>

-   <span data-ttu-id="5a14a-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="5a14a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5a14a-107"><span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pclines*</span><span class="sxs-lookup"><span data-stu-id="5a14a-107"><span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*</span></span>
</dt> <dd>

<span data-ttu-id="5a14a-108">Die Adresse einer Variablen, die die Anzahl der angezeigten Zeilen erhält.</span><span class="sxs-lookup"><span data-stu-id="5a14a-108">The address of a variable that receives the number of lines displayed.</span></span>

</dd> </dl>

<span data-ttu-id="5a14a-109">Der Microsoft-Agent-Server führt automatisch einen Bildlauf der Zeilen aus, die für die gesprochene Ausgabe in der Wort Blase</span><span class="sxs-lookup"><span data-stu-id="5a14a-109">The Microsoft Agent server automatically scrolls the lines displayed for spoken output in the word balloon.</span></span> <span data-ttu-id="5a14a-110">Die Anzahl der Zeilen für eine Zeichen Wort Sprechblase wird im Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="5a14a-110">The number of lines for a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="5a14a-111">Sie kann nicht von einer Anwendung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5a14a-111">It cannot be changed by an application.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a14a-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5a14a-112">See Also</span></span>

[<span data-ttu-id="5a14a-113">**Iagentballoon:: getnumcharsperline**</span><span class="sxs-lookup"><span data-stu-id="5a14a-113">**IAgentBalloon::GetNumCharsPerLine**</span></span>](iagentballoon--getnumcharsperline.md)


 

 




