---
title: Übersetzen von VBScript in JScript
description: Übersetzen von VBScript in JScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18c2ccb11ffa4f5f000d8cfc73f7db6f857cf6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708033"
---
# <a name="translating-to-jscript-from-vbscript"></a><span data-ttu-id="04971-103">Übersetzen von VBScript in JScript</span><span class="sxs-lookup"><span data-stu-id="04971-103">Translating to JScript from VBScript</span></span>

<span data-ttu-id="04971-104">In VBScript lautet der **für**... **Jede** Schleife listet die Member einer Auflistung auf. in JScript ist das **für**... die in-Schleife listet die Member eines JScript-Objekts oder-Arrays **auf** .</span><span class="sxs-lookup"><span data-stu-id="04971-104">In VBScript, the **For**...**Each** loop enumerates the members of a collection; in JScript, the **for**...**in** loop enumerates the members of a JScript object or array.</span></span> <span data-ttu-id="04971-105">Um eine Auflistung in JScript aufzulisten, verwenden Sie ein Enumeratorobjekt.</span><span class="sxs-lookup"><span data-stu-id="04971-105">To enumerate a collection in JScript, use an Enumerator object.</span></span>

<span data-ttu-id="04971-106">In JScript gibt es mehrere Datentypen, wie z. b. Zahlen, Zeichen folgen, boolesche Werte, Objekte und das NULL-Attribut.</span><span class="sxs-lookup"><span data-stu-id="04971-106">In JScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="04971-107">VBScript verwendet nur einen Datentyp ( **Variant**), der zum Darstellen von Zeichen folgen, Zahlen, booleschen Werten und so weiter subtypisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="04971-107">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="04971-108">In JScript können Arrays dynamisch erweitert werden, indem ein neuer Wert für die length-Eigenschaft des Arrays festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="04971-108">In JScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="04971-109">In VBScript können Arrays nicht vergrößert werden. Sie müssen mit der **ReDim** -Anweisung erneut dimensioniert werden.</span><span class="sxs-lookup"><span data-stu-id="04971-109">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="04971-110">VBScript-und JScript-Unterstützungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="04971-110">Both VBScript and JScript support functions.</span></span> <span data-ttu-id="04971-111">VBScript unterstützt jedoch auch Unterroutinen.</span><span class="sxs-lookup"><span data-stu-id="04971-111">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="04971-112">Unterroutinen ähneln Funktionen, geben jedoch keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="04971-112">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="04971-113">Bei JScript wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="04971-113">JScript is case-sensitive.</span></span> <span data-ttu-id="04971-114">VBScript ist nicht.</span><span class="sxs-lookup"><span data-stu-id="04971-114">VBScript is not.</span></span>

<span data-ttu-id="04971-115">JScript wird sowohl von Internet Explorer als auch von Netscape Navigator unterstützt.</span><span class="sxs-lookup"><span data-stu-id="04971-115">JScript is supported by both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="04971-116">"Netscape Navigator" unterstützt VBScript nicht.</span><span class="sxs-lookup"><span data-stu-id="04971-116">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="04971-117">JScript stellt das Error-Objekt bereit, das verwendet werden kann, um Fehler abzufangen und zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="04971-117">JScript provides the Error object, which can be used to trap and handle errors.</span></span> <span data-ttu-id="04971-118">Das Error-Objekt ist analog zum VBScript-Err-Objekt.</span><span class="sxs-lookup"><span data-stu-id="04971-118">The Error object is analogous to the VBScript Err object.</span></span>

<span data-ttu-id="04971-119">JScript-Arrays sind keine Arrays des Variablentyp **Variant SAFEARRAY**.</span><span class="sxs-lookup"><span data-stu-id="04971-119">JScript arrays are not arrays of the variable type **VARIANT SAFEARRAY**.</span></span> <span data-ttu-id="04971-120">Wenn Ihr Skript eine Varianz **-Varianz Variable von** einem COM-Objekt oder einem VBScript-Skript empfängt, muss es ein VBArray-Objekt verwenden, um auf die Varianz Variable **SAFEARRAY** zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="04971-120">If your script receives a **VARIANT SAFEARRAY** variable from a COM object or VBScript script, it must use a VBArray object to access the **VARIANT SAFEARRAY** variable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04971-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="04971-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04971-122">Übersetzen in JScript</span><span class="sxs-lookup"><span data-stu-id="04971-122">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




