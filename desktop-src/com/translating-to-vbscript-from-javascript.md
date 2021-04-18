---
title: Übersetzen in VBScript aus JavaScript
description: Übersetzen in VBScript aus JavaScript
ms.assetid: f302e032-4e94-42f1-839b-022dab538760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eda8169a665dc93133f7ac933de12ecc612f3e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338169"
---
# <a name="translating-to-vbscript-from-javascript"></a><span data-ttu-id="7e2e5-103">Übersetzen in VBScript aus JavaScript</span><span class="sxs-lookup"><span data-stu-id="7e2e5-103">Translating to VBScript from JavaScript</span></span>

<span data-ttu-id="7e2e5-104">In JavaScript gibt es mehrere Datentypen, z. b. Zahlen, Zeichen folgen, boolesche Werte, Objekte und das NULL-Attribut.</span><span class="sxs-lookup"><span data-stu-id="7e2e5-104">In JavaScript, there are several data types, such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="7e2e5-105">VBScript verwendet nur einen Datentyp ( **Variant**), der zum Darstellen von Zeichen folgen, Zahlen, booleschen Werten und so weiter subtypisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e2e5-105">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="7e2e5-106">In JavaScript können Arrays dynamisch erweitert werden, indem ein neuer Wert für die length-Eigenschaft des Arrays festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7e2e5-106">In JavaScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="7e2e5-107">In VBScript können Arrays nicht vergrößert werden. Sie müssen mit der **ReDim** -Anweisung erneut dimensioniert werden.</span><span class="sxs-lookup"><span data-stu-id="7e2e5-107">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="7e2e5-108">VBScript-und JavaScript-Unterstützungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="7e2e5-108">Both VBScript and JavaScript support functions.</span></span> <span data-ttu-id="7e2e5-109">VBScript unterstützt jedoch auch Unterroutinen.</span><span class="sxs-lookup"><span data-stu-id="7e2e5-109">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="7e2e5-110">Unterroutinen ähneln Funktionen, mit dem Unterschied, dass Sie keinen Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7e2e5-110">Subroutines are similar to functions, except they do not return a value.</span></span>

<span data-ttu-id="7e2e5-111">In JavaScript muss die Groß-/Kleinschreibung beachtet werden.</span><span class="sxs-lookup"><span data-stu-id="7e2e5-111">JavaScript is case-sensitive.</span></span> <span data-ttu-id="7e2e5-112">VBScript ist nicht.</span><span class="sxs-lookup"><span data-stu-id="7e2e5-112">VBScript is not.</span></span>

<span data-ttu-id="7e2e5-113">JavaScript wird von einer Vielzahl von Webbrowsern unterstützt, einschließlich Internet Explorer und Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="7e2e5-113">JavaScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="7e2e5-114">"Netscape Navigator" unterstützt VBScript nicht.</span><span class="sxs-lookup"><span data-stu-id="7e2e5-114">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="7e2e5-115">VBScript unterstützt die Fehlerbehandlung durch das Err-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7e2e5-115">VBScript supports error handling through its Err object.</span></span> <span data-ttu-id="7e2e5-116">JavaScript bietet derzeit keine Möglichkeit zum Abfangen und behandeln von Fehlern.</span><span class="sxs-lookup"><span data-stu-id="7e2e5-116">JavaScript does not currently provide a means of trapping and handling errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e2e5-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7e2e5-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e2e5-118">Übersetzen in VBScript</span><span class="sxs-lookup"><span data-stu-id="7e2e5-118">Translating to VBScript</span></span>](translating-to-vbscript.md)
</dt> </dl>

 

 




