---
title: Iagentballoonex-setnumlines
description: Iagentballoonex-setnumlines
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45c012d0193a0bd21ba203418920b87b2fac81b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471580"
---
# <a name="iagentballoonexsetnumlines"></a><span data-ttu-id="8623b-103">Iagentballoonex:: setnumlines</span><span class="sxs-lookup"><span data-stu-id="8623b-103">IAgentBalloonEx::SetNumLines</span></span>

<span data-ttu-id="8623b-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="8623b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

<span data-ttu-id="8623b-105">Legt die Anzahl von Textausgabe Zeilen fest, die in der Wort Sprechblase des Zeichens angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="8623b-105">Sets the number of lines of text output that can be displayed in the character's word balloon.</span></span>

-   <span data-ttu-id="8623b-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="8623b-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="8623b-107">Gibt E \_ invalidArg zurück, wenn der-Parameter NULL ist.</span><span class="sxs-lookup"><span data-stu-id="8623b-107">Returns E\_INVALIDARG if the parameter is zero.</span></span>

<dl> <dt>

<span data-ttu-id="8623b-108"><span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*llines*</span><span class="sxs-lookup"><span data-stu-id="8623b-108"><span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*</span></span>
</dt> <dd>

<span data-ttu-id="8623b-109">Anzahl der Zeilen, die in der Wort Sprechblase angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8623b-109">Number of lines to display in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="8623b-110">Die minimale Einstellung ist 1 und der Höchstwert 128.</span><span class="sxs-lookup"><span data-stu-id="8623b-110">The minimum setting is 1 and maximum is 128.</span></span> <span data-ttu-id="8623b-111">Wenn der in der Sprech [**Methode oder**](think-method.md) der Methode "Sprache" angegebene Text die Größe der aktuellen Sprechblase überschreitet, führt der-Agent automatisch einen Bildlauf im Text der [**Sprech**](speak-method.md) Blase</span><span class="sxs-lookup"><span data-stu-id="8623b-111">If the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method exceeds the size of the current balloon, Agent automatically scrolls the text in the balloon.</span></span>

<span data-ttu-id="8623b-112">Bei dieser Methode tritt ein Fehler auf, wenn das **QuickInfo** -Sprechblasen-Stilbit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8623b-112">This method will fail if the **SizeToText** balloon style bit is set.</span></span>

<span data-ttu-id="8623b-113">Die Standardeinstellung basiert auf den Einstellungen, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="8623b-113">The default setting is based on settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="8623b-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8623b-114">See Also</span></span>

<span data-ttu-id="8623b-115">[**Iagentballoon:: getnumlines**](iagentballoon--getnumlines.md), [**iagentballoonex:: GetStyle**](iagentballoonex--getstyle.md), [**iagentballoonex:: SetStyle**](iagentballoonex--setstyle.md)</span><span class="sxs-lookup"><span data-stu-id="8623b-115">[**IAgentBalloon::GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx::GetStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md)</span></span>


 

 




