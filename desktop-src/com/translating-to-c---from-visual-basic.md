---
title: Übersetzen in C++ von Visual Basic
description: Visual Basic behandelt Zeiger implizit. In C++ ist Ihre Anwendung für die Ausführung erforderlicher Zeigerarithmetik verantwortlich.
ms.assetid: bbbcaba1-cf5a-4768-ad1d-22a040bfe384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53de112f19b51be92657fb3293bb35e1d41ff9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206717"
---
# <a name="translating-to-c-from-visual-basic"></a><span data-ttu-id="24fdf-104">Übersetzen in C++ von Visual Basic</span><span class="sxs-lookup"><span data-stu-id="24fdf-104">Translating to C++ from Visual Basic</span></span>

<span data-ttu-id="24fdf-105">Visual Basic behandelt Zeiger implizit.</span><span class="sxs-lookup"><span data-stu-id="24fdf-105">Visual Basic handles pointers implicitly.</span></span> <span data-ttu-id="24fdf-106">In C++ ist Ihre Anwendung für die Ausführung erforderlicher Zeigerarithmetik verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="24fdf-106">In C++, your application is responsible for performing any necessary pointer arithmetic.</span></span>

<span data-ttu-id="24fdf-107">Standardmäßig übergibt Visual Basic Parameter nach Verweis (als Zeiger).</span><span class="sxs-lookup"><span data-stu-id="24fdf-107">By default, Visual Basic passes parameters by reference (as pointers).</span></span> <span data-ttu-id="24fdf-108">Parameter, die nur als Wert übermittelt werden sollen, werden durch das Schlüsselwort **ByVal** angegeben.</span><span class="sxs-lookup"><span data-stu-id="24fdf-108">Parameters that are meant to be passed by value only are specified by the keyword **ByVal**.</span></span> <span data-ttu-id="24fdf-109">Beispielsweise entspricht der  **ganzzahlige** Parameter " **ByVal**" in Visual Basic einem **kurzen** Parameter in C++, wohingegen ein **ByRef**- **Parameter in** Visual Basic einem **kurzen \*** Parameter entspricht.</span><span class="sxs-lookup"><span data-stu-id="24fdf-109">For example, a **ByVal** Â  **Integer** parameter in Visual Basic is equivalent to a **short** parameter in C++, whereas a **ByRef** Â  **Integer** parameter in Visual Basic is equivalent to a **short\*** parameter.</span></span>

<span data-ttu-id="24fdf-110">Ein Parameter, der in Visual Basic **als Zeichenfolge** deklariert ist, wird als Zeiger auf einen **BSTR** in C++ deklariert.</span><span class="sxs-lookup"><span data-stu-id="24fdf-110">A parameter that is declared **As String** in Visual Basic is declared as a pointer to a **BSTR** in C++.</span></span> <span data-ttu-id="24fdf-111">Das Festlegen eines Zeichen folgen Zeigers auf **null** in C++ entspricht dem Festlegen der Zeichenfolge auf die **vbNullString** -Konstante in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="24fdf-111">Setting a string pointer to **NULL** in C++ is equivalent to setting the string to the **vbNullString** constant in Visual Basic.</span></span> <span data-ttu-id="24fdf-112">Das übergeben einer Zeichenfolge der Länge 0 (null) an eine Funktion, die für den Empfang von **null** vorgesehen ist, funktioniert nicht, da dadurch ein Zeiger auf eine Zeichenfolge der Länge 0 (null) anstatt auf einen NULL-Zeiger übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="24fdf-112">Passing a zero-length string ("") to a function designed to receive **NULL** does not work, because this passes a pointer to a zero-length string instead of a zero pointer.</span></span>

<span data-ttu-id="24fdf-113">C++ und Visual Basic unterscheiden sich geringfügig von der Darstellung von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="24fdf-113">C++ and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="24fdf-114">In C++ werden Eigenschaften als ein Satz von Accessorfunktionen dargestellt, der den Eigenschafts Wert festlegt und einen, der den Eigenschafts Wert abruft.</span><span class="sxs-lookup"><span data-stu-id="24fdf-114">In C++, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="24fdf-115">In Visual Basic werden Eigenschaften als einzelnes Element dargestellt, das zum Abrufen oder Festlegen des Eigenschafts Werts verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="24fdf-115">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24fdf-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="24fdf-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24fdf-117">Übersetzen in C++</span><span class="sxs-lookup"><span data-stu-id="24fdf-117">Translating to C++</span></span>](translating-to-c--.md)
</dt> </dl>

 

 




