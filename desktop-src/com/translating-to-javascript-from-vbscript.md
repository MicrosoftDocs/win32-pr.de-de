---
title: Übersetzen in JavaScript aus VBScript
description: Übersetzen in JavaScript aus VBScript
ms.assetid: 39a712c5-f8d7-4441-a602-93cda43c24d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff950c58c87e926c8593e5c009db4efbce0a371
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309367"
---
# <a name="translating-to-javascript-from-vbscript"></a><span data-ttu-id="7dca6-103">Übersetzen in JavaScript aus VBScript</span><span class="sxs-lookup"><span data-stu-id="7dca6-103">Translating to JavaScript from VBScript</span></span>

<span data-ttu-id="7dca6-104">In JavaScript gibt es mehrere Datentypen, wie z. b. Zahlen, Zeichen folgen, boolesche Werte, Objekte und das NULL-Attribut.</span><span class="sxs-lookup"><span data-stu-id="7dca6-104">In JavaScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="7dca6-105">VBScript verwendet nur einen Datentyp ( **Variant**), der zum Darstellen von Zeichen folgen, Zahlen, booleschen Werten und so weiter subtypisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7dca6-105">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="7dca6-106">In JavaScript können Arrays dynamisch erweitert werden, indem ein neuer Wert für die length-Eigenschaft des Arrays festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7dca6-106">In JavaScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="7dca6-107">In VBScript können Arrays nicht vergrößert werden. Sie müssen mit der **ReDim** -Anweisung erneut dimensioniert werden.</span><span class="sxs-lookup"><span data-stu-id="7dca6-107">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="7dca6-108">VBScript-und JavaScript-Unterstützungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="7dca6-108">Both VBScript and JavaScript support functions.</span></span> <span data-ttu-id="7dca6-109">VBScript unterstützt jedoch auch Unterroutinen.</span><span class="sxs-lookup"><span data-stu-id="7dca6-109">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="7dca6-110">Unterroutinen ähneln Funktionen, geben jedoch keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7dca6-110">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="7dca6-111">In JavaScript muss die Groß-/Kleinschreibung beachtet werden.</span><span class="sxs-lookup"><span data-stu-id="7dca6-111">JavaScript is case-sensitive.</span></span> <span data-ttu-id="7dca6-112">VBScript ist nicht.</span><span class="sxs-lookup"><span data-stu-id="7dca6-112">VBScript is not.</span></span>

<span data-ttu-id="7dca6-113">JavaScript wird von einer Vielzahl von Webbrowsern unterstützt, einschließlich Internet Explorer und Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="7dca6-113">JavaScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="7dca6-114">VBScript wird nur von Internet Explorer unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7dca6-114">VBScript is only supported by Internet Explorer.</span></span>

<span data-ttu-id="7dca6-115">VBScript bietet Unterstützung für die Fehlerbehandlung durch das Err-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7dca6-115">VBScript provides error handling support through its Err object.</span></span> <span data-ttu-id="7dca6-116">JavaScript bietet derzeit keine Möglichkeit zum Abfangen und behandeln von Fehlern.</span><span class="sxs-lookup"><span data-stu-id="7dca6-116">JavaScript does not currently provide a means of trapping and handling errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7dca6-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7dca6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dca6-118">Übersetzen in JavaScript</span><span class="sxs-lookup"><span data-stu-id="7dca6-118">Translating to JavaScript</span></span>](translating-to-javascript.md)
</dt> </dl>

 

 




