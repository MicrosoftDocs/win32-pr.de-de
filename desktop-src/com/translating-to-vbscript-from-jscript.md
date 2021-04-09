---
title: Übersetzen in VBScript aus JScript
description: Übersetzen in VBScript aus JScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f5ac608e94f883edc3b319fd04625e9a08d18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036652"
---
# <a name="translating-to-vbscript-from-jscript"></a><span data-ttu-id="579eb-103">Übersetzen in VBScript aus JScript</span><span class="sxs-lookup"><span data-stu-id="579eb-103">Translating to VBScript from JScript</span></span>

<span data-ttu-id="579eb-104">In VBScript lautet der **für**... **Jede** Schleife listet die Member einer Auflistung auf. in JScript ist das **für**... die in-Schleife listet die Member eines JScript-Objekts oder-Arrays **auf** .</span><span class="sxs-lookup"><span data-stu-id="579eb-104">In VBScript, the **For**...**Each** loop enumerates the members of a collection; in JScript, the **for**...**in** loop enumerates the members of a JScript object or array.</span></span> <span data-ttu-id="579eb-105">Um eine Auflistung in JScript aufzulisten, verwenden Sie ein Enumeratorobjekt.</span><span class="sxs-lookup"><span data-stu-id="579eb-105">To enumerate a collection in JScript, use an Enumerator object.</span></span>

<span data-ttu-id="579eb-106">JScript stellt das Error-Objekt bereit, das verwendet werden kann, um Fehler abzufangen und zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="579eb-106">JScript provides the Error object, which can be used to trap and handle errors.</span></span> <span data-ttu-id="579eb-107">Das Error-Objekt ist analog zum VBScript-Err-Objekt.</span><span class="sxs-lookup"><span data-stu-id="579eb-107">The Error object is analogous to the VBScript Err object.</span></span>

<span data-ttu-id="579eb-108">In JScript gibt es mehrere Datentypen, wie z. b. Zahlen, Zeichen folgen, boolesche Werte, Objekte und das NULL-Attribut.</span><span class="sxs-lookup"><span data-stu-id="579eb-108">In JScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="579eb-109">VBScript verwendet nur einen Datentyp ( **Variant**), der zum Darstellen von Zeichen folgen, Zahlen, booleschen Werten und so weiter subtypisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="579eb-109">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="579eb-110">In JScript können Arrays dynamisch erweitert werden, indem ein neuer Wert für die length-Eigenschaft des Arrays festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="579eb-110">In JScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="579eb-111">In VBScript können Arrays nicht vergrößert werden. Sie müssen mit der **ReDim** -Anweisung erneut dimensioniert werden.</span><span class="sxs-lookup"><span data-stu-id="579eb-111">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="579eb-112">VBScript-und JScript-Unterstützungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="579eb-112">Both VBScript and JScript support functions.</span></span> <span data-ttu-id="579eb-113">VBScript unterstützt jedoch auch Unterroutinen.</span><span class="sxs-lookup"><span data-stu-id="579eb-113">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="579eb-114">Unterroutinen ähneln Funktionen, geben jedoch keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="579eb-114">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="579eb-115">Bei JScript wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="579eb-115">JScript is case-sensitive.</span></span> <span data-ttu-id="579eb-116">VBScript ist nicht.</span><span class="sxs-lookup"><span data-stu-id="579eb-116">VBScript is not.</span></span>

<span data-ttu-id="579eb-117">JScript wird von einer Vielzahl von Webbrowsern unterstützt, einschließlich Internet Explorer und Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="579eb-117">JScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="579eb-118">"Netscape Navigator" unterstützt VBScript nicht.</span><span class="sxs-lookup"><span data-stu-id="579eb-118">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="579eb-119">JScript-Arrays sind keine Arrays des Variablentyp **Variant SAFEARRAY**.</span><span class="sxs-lookup"><span data-stu-id="579eb-119">JScript arrays are not arrays of the variable type **VARIANT SAFEARRAY**.</span></span> <span data-ttu-id="579eb-120">Ein JScript-Skript muss ein VBArray-Objekt verwenden, um auf die Varianz Variable **SAFEARRAY** zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="579eb-120">A JScript script must use a VBArray object to access the **VARIANT SAFEARRAY** variable.</span></span> <span data-ttu-id="579eb-121">VBScript-Skripts können direkt auf **Variant-SAFEARRAY**-Variablen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="579eb-121">VBScript scripts can access **VARIANT SAFEARRAY** variables directly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="579eb-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="579eb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="579eb-123">Übersetzen in VBScript</span><span class="sxs-lookup"><span data-stu-id="579eb-123">Translating to VBScript</span></span>](translating-to-vbscript.md)
</dt> </dl>

 

 




