---
title: Syntaxunterschiede
description: Die offensichtlichste Änderung bei der Umstellung zwischen Programmiersprachen ist die Syntax Änderung.
ms.assetid: 179efb69-3794-4a06-b770-2b3dc8409172
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3a9c2123d8b94f9fc6fe79d4ab48188830c7a1
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474349"
---
# <a name="syntax-differences"></a><span data-ttu-id="55d7f-103">Syntaxunterschiede</span><span class="sxs-lookup"><span data-stu-id="55d7f-103">Syntax Differences</span></span>

<span data-ttu-id="55d7f-104">Die offensichtlichste Änderung bei der Umstellung zwischen Programmiersprachen ist die Syntax Änderung.</span><span class="sxs-lookup"><span data-stu-id="55d7f-104">The most apparent change as you move between programming languages is the change in syntax.</span></span>

<span data-ttu-id="55d7f-105">Sehen Sie sich die Add-Methode des enhevents-Objekts an, die wie in drei verschiedenen Sprachen deklariert ist.</span><span class="sxs-lookup"><span data-stu-id="55d7f-105">Consider the EnhEvents object's Add method, shown as it is declared in three different languages.</span></span>

``` syntax
object.Add(Time As Double, Name As String) As Variant

HRESULT Add(
  double Time, 
  BSTR Name, 
  VARIANT* pVal
);
 
public com.ms.com.Variant Add( 
  double Time, 
  java.lang.String Name
);
 
```

<span data-ttu-id="55d7f-106">Obwohl die Syntax der einzelnen Sprachen die Methode anders ausdrückt, ist die Funktionalität identisch.</span><span class="sxs-lookup"><span data-stu-id="55d7f-106">Although the syntax of each language expresses the method differently, the functionality is the same.</span></span> <span data-ttu-id="55d7f-107">In jeder Sprache übernimmt die Add-Methode die Parameter *time* und *Name* und gibt ein enhevent-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="55d7f-107">In each language, the Add method takes the parameters *Time* and *Name* and returns an EnhEvent object.</span></span> <span data-ttu-id="55d7f-108">Im C++-Beispiel gibt die-Methode das-Objekt mithilfe eines dritten Output-Parameters ( *PVal*) zurück.</span><span class="sxs-lookup"><span data-stu-id="55d7f-108">In the C++ example, the method returns the object by using a third, output parameter, *pVal*.</span></span>

<span data-ttu-id="55d7f-109">In der Regel ist die Funktionalität eines COM-Objekts in den Programmiersprachen identisch.</span><span class="sxs-lookup"><span data-stu-id="55d7f-109">Typically, the functionality of a COM object is the same across programming languages.</span></span> <span data-ttu-id="55d7f-110">Aus diesem Grund ist die Dokumentation für ein COM-Objekt auch dann nützlich, wenn das Objekt in einer anderen Programmiersprache dokumentiert ist als das, das Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="55d7f-110">Because of this, documentation for a COM object is useful even if the object is documented in another programming language than the one you are using.</span></span> <span data-ttu-id="55d7f-111">Die Beschreibungen der Funktionen, Parameter und Rückgabewerte des Objekts sind mit wenigen Ausnahmen, die für alle Sprachen gültig sind.</span><span class="sxs-lookup"><span data-stu-id="55d7f-111">The descriptions of the object's functionality, parameters, and return values are, with few exceptions, valid for all languages.</span></span>

<span data-ttu-id="55d7f-112">Informationen dazu, wie Sie die Syntax eines COM-Objekts in eine andere Programmiersprache konvertieren, finden Sie unter über [setzen der COM-Objekt Syntax für Programmiersprachen](translating-com-object-syntax-for-programming-languages.md).</span><span class="sxs-lookup"><span data-stu-id="55d7f-112">For information about how to convert the syntax of a COM object to another programming language, see [Translating COM Object Syntax for Programming Languages](translating-com-object-syntax-for-programming-languages.md).</span></span>

<span data-ttu-id="55d7f-113">Die Syntax Unterschiede zwischen den Skriptsprachen Javascript, JScript und VBScript sind weniger ausgeprägt als die Syntax Unterschiede zwischen den oben gezeigten Programmiersprachen.</span><span class="sxs-lookup"><span data-stu-id="55d7f-113">The syntax differences among the scripting languages JavaScript, JScript, and VBScript are less pronounced than the syntax differences among the programming languages shown preceding.</span></span> <span data-ttu-id="55d7f-114">Sehen Sie sich beispielsweise die quadratische Funktion an, wie Sie in jeder dieser drei Skriptsprachen implementiert wird:</span><span class="sxs-lookup"><span data-stu-id="55d7f-114">For example, consider the square function as it is implemented in each of these three scripting languages:</span></span>

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

<span data-ttu-id="55d7f-115">Beachten Sie, dass die Skriptsprachen im Gegensatz zu den Programmiersprachen schwach typisiert sind.</span><span class="sxs-lookup"><span data-stu-id="55d7f-115">Notice that the scripting languages, unlike the programming languages, are weakly typed.</span></span> <span data-ttu-id="55d7f-116">Anders ausgedrückt: Sie müssen den Datentyp eines Parameters oder Rückgabewerts nicht angeben, wenn Sie eine Funktion deklarieren.</span><span class="sxs-lookup"><span data-stu-id="55d7f-116">In other words, you do not have to specify the data type of a parameter or return value when you declare a function.</span></span> <span data-ttu-id="55d7f-117">Stattdessen werden die Variablen automatisch in den entsprechenden Datentyp umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="55d7f-117">Instead, the variables are automatically cast to the appropriate data type.</span></span> <span data-ttu-id="55d7f-118">Im Fall von VBScript weisen alle Variablen denselben Datentyp auf, **Variant**.</span><span class="sxs-lookup"><span data-stu-id="55d7f-118">In the case of VBScript, all variables are of the same data type, **Variant**.</span></span>

<span data-ttu-id="55d7f-119">Die JavaScript-und JScript-Syntax für Square ist identisch.</span><span class="sxs-lookup"><span data-stu-id="55d7f-119">The JavaScript and JScript syntax for square is the same.</span></span> <span data-ttu-id="55d7f-120">JScript ist größtenteils mit JavaScript kompatibel.</span><span class="sxs-lookup"><span data-stu-id="55d7f-120">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="55d7f-121">JScript enthält jedoch einige Objekte, die zurzeit nicht von JavaScript unterstützt werden, z. b. **ActiveXObject**, **Enumerator**, **Error**, **Global** und **VBArray**.</span><span class="sxs-lookup"><span data-stu-id="55d7f-121">However, JScript includes some objects not currently supported by JavaScript, such as **ActiveXObject**, **Enumerator**, **Error**, **Global**, and **VBArray**.</span></span> <span data-ttu-id="55d7f-122">Weitere Informationen zu diesen Objekten finden Sie in der [JScript-Sprachreferenz](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="55d7f-122">For more information about these objects, see the [JScript Language Reference](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).</span></span>

<span data-ttu-id="55d7f-123">Auf der Oberfläche ähnelt die JavaScript-und JScript-Syntax der Java-Syntax.</span><span class="sxs-lookup"><span data-stu-id="55d7f-123">On the surface, JavaScript and JScript syntax resembles Java syntax.</span></span> <span data-ttu-id="55d7f-124">Diese Ähnlichkeit ist nur oberflächlich.</span><span class="sxs-lookup"><span data-stu-id="55d7f-124">This similarity is only superficial.</span></span> <span data-ttu-id="55d7f-125">Die Java-Sprache wurde unabhängig von JavaScript und JScript entwickelt und steht nicht im Zusammenhang mit beiden.</span><span class="sxs-lookup"><span data-stu-id="55d7f-125">The Java language was developed independently from both JavaScript and JScript and is not related to either.</span></span>

<span data-ttu-id="55d7f-126">VBScript hingegen ist eine Teilmenge der Programmiersprache Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="55d7f-126">VBScript, on the other hand, is a subset of the Visual Basic programming language.</span></span> <span data-ttu-id="55d7f-127">Aus diesem Grund ist die VBScript-Syntax eine Teilmenge Visual Basic Syntax und häufig mit Visual Basic Syntax austauschbar.</span><span class="sxs-lookup"><span data-stu-id="55d7f-127">Because of this, VBScript syntax is a subset of Visual Basic syntax and is often interchangeable with Visual Basic syntax.</span></span>

<span data-ttu-id="55d7f-128">Informationen zur Verwendung von COM-Objekten in Skriptsprachen finden Sie unter [Skripterstellung mit COM-Objekten](scripting-with-com-objects.md).</span><span class="sxs-lookup"><span data-stu-id="55d7f-128">For information on using COM objects in scripting languages, see [Scripting with COM Objects](scripting-with-com-objects.md).</span></span>

 

 