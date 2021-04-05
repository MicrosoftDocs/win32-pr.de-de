---
title: Iagentballoon getnumcharsperline
description: Iagentballoon getnumcharsperline
ms.assetid: ae0c7fff-8c58-465e-9b4f-3260f7574b57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887167584c46f075bc0696c46b2dde52eb27f8d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037548"
---
# <a name="iagentballoongetnumcharsperline"></a><span data-ttu-id="217c4-103">Iagentballoon:: getnumcharsperline</span><span class="sxs-lookup"><span data-stu-id="217c4-103">IAgentBalloon::GetNumCharsPerLine</span></span>

<span data-ttu-id="217c4-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="217c4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetNumCharsPerLine(
   long * plCharsPerLine  // address of variable for characters per line
);                        // displayed in word balloon
```

<span data-ttu-id="217c4-105">Ruft den Wert für die durchschnittliche Anzahl von Zeichen pro Zeile ab, die in einer Wort Sprechblase angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="217c4-105">Retrieves the value for the average number of characters per line displayed in a word balloon.</span></span>

-   <span data-ttu-id="217c4-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="217c4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="217c4-107"><span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbcharsperline*</span><span class="sxs-lookup"><span data-stu-id="217c4-107"><span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*</span></span>
</dt> <dd>

<span data-ttu-id="217c4-108">Die Adresse einer Variablen, die die Anzahl der Zeichen pro Zeile empfängt.</span><span class="sxs-lookup"><span data-stu-id="217c4-108">The address of a variable that receives the number of characters per line.</span></span>

</dd> </dl>

<span data-ttu-id="217c4-109">Der Microsoft-Agent-Server führt automatisch einen Bildlauf der Zeilen aus, die für die gesprochene Ausgabe in der Wort Blase</span><span class="sxs-lookup"><span data-stu-id="217c4-109">The Microsoft Agent server automatically scrolls the lines displayed for spoken output in the word balloon.</span></span> <span data-ttu-id="217c4-110">Die durchschnittliche Anzahl von Zeichen pro Zeile für die Word-Sprechblase eines Zeichens wird im Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="217c4-110">The average number of characters per line for a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="217c4-111">Sie kann nicht von einer Anwendung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="217c4-111">It cannot be changed by an application.</span></span>

## <a name="see-also"></a><span data-ttu-id="217c4-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="217c4-112">See Also</span></span>

[<span data-ttu-id="217c4-113">**Iagentballoon:: getnumlines**</span><span class="sxs-lookup"><span data-stu-id="217c4-113">**IAgentBalloon::GetNumLines**</span></span>](iagentballoon--getnumlines.md)


 

 




