---
title: Iagentballoonex setnumcharsperline
description: Iagentballoonex setnumcharsperline
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a44abe14de6bb1cef631a51b4516d083657016
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310964"
---
# <a name="iagentballoonexsetnumcharsperline"></a><span data-ttu-id="17612-103">Iagentballoonex:: setnumcharsperline</span><span class="sxs-lookup"><span data-stu-id="17612-103">IAgentBalloonEx::SetNumCharsPerLine</span></span>

<span data-ttu-id="17612-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="17612-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

<span data-ttu-id="17612-105">Legt die Anzahl von Zeichen pro Zeile fest, die in der Wort Sprechblase des Zeichens angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="17612-105">Sets the number of characters per line that can be displayed in the character's word balloon.</span></span>

-   <span data-ttu-id="17612-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="17612-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="17612-107">Gibt E \_ invalidArg zurück, wenn der-Parameter kleiner als acht ist.</span><span class="sxs-lookup"><span data-stu-id="17612-107">Returns E\_INVALIDARG if the parameter is less than eight.</span></span>

<dl> <dt>

<span data-ttu-id="17612-108"><span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lcharsperline*</span><span class="sxs-lookup"><span data-stu-id="17612-108"><span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*</span></span>
</dt> <dd>

<span data-ttu-id="17612-109">Anzahl der Zeilen, die in der Wort Sprechblase angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="17612-109">Number of lines to display in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="17612-110">Die minimale Einstellung ist 8, und der Höchstwert ist 255.</span><span class="sxs-lookup"><span data-stu-id="17612-110">The minimum setting is 8 and the maximum is 255.</span></span> <span data-ttu-id="17612-111">Wenn der in der Sprech [**Methode oder**](think-method.md) der Methode "Sprache" angegebene Text die Größe der aktuellen Sprechblase überschreitet, führt der-Agent automatisch einen Bildlauf im Text der [**Sprech**](speak-method.md) Blase</span><span class="sxs-lookup"><span data-stu-id="17612-111">If the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method exceeds the size of the current balloon, Agent automatically scrolls the text in the balloon.</span></span>

<span data-ttu-id="17612-112">Die Standardeinstellung basiert auf den Einstellungen, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="17612-112">The default setting is based on settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="17612-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="17612-113">See Also</span></span>

[<span data-ttu-id="17612-114">**Iagentballoon:: getnumcharsperline**</span><span class="sxs-lookup"><span data-stu-id="17612-114">**IAgentBalloon::GetNumCharsPerLine**</span></span>](iagentballoon--getnumcharsperline.md)


 

 




