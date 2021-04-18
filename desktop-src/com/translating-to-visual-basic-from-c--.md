---
title: Übersetzen in Visual Basic von C++
description: Übersetzen in Visual Basic von C++
ms.assetid: fce7ea25-cb24-4cc4-8f36-0e8aed2f3ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba519cbdb0305fe3a2eae4cc8e658fdde1eac3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340216"
---
# <a name="translating-to-visual-basic-from-c"></a><span data-ttu-id="9cd18-103">Übersetzen in Visual Basic von C++</span><span class="sxs-lookup"><span data-stu-id="9cd18-103">Translating to Visual Basic from C++</span></span>

<span data-ttu-id="9cd18-104">Mithilfe der Programmiersprache C++ können Entwickler direkt auf den Speicher zugreifen, in dem eine bestimmte Variable gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="9cd18-104">Using the C++ programming language, developers can directly access the memory that stores a particular variable.</span></span> <span data-ttu-id="9cd18-105">Speicher Zeiger bieten diesen direkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="9cd18-105">Memory pointers provide this direct access.</span></span> <span data-ttu-id="9cd18-106">In Visual Basic werden Zeiger für Sie behandelt.</span><span class="sxs-lookup"><span data-stu-id="9cd18-106">In Visual Basic, pointers are handled for you.</span></span> <span data-ttu-id="9cd18-107">Beispielsweise ist ein Parameter, der als Zeiger auf ein **int** in C++ deklariert ist, mit einem Parameter identisch, der in Visual Basic als **ByRef**- **Ganzzahl** deklariert wurde.</span><span class="sxs-lookup"><span data-stu-id="9cd18-107">For example, a parameter declared as a pointer to an **int** in C++ is equivalent to a parameter declared in Visual Basic as a **ByRef** **Integer**.</span></span>

<span data-ttu-id="9cd18-108">Ein Parameter, der in Visual Basic **als Zeichenfolge** deklariert ist, wird als Zeiger auf einen **BSTR** in C++ deklariert.</span><span class="sxs-lookup"><span data-stu-id="9cd18-108">A parameter that is declared **As String** in Visual Basic is declared as a pointer to a **BSTR** in C++.</span></span> <span data-ttu-id="9cd18-109">Das Festlegen eines Zeichen folgen Zeigers auf **null** in C++ entspricht dem Festlegen der Zeichenfolge auf die **vbNullString** -Konstante in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9cd18-109">Setting a string pointer to **NULL** in C++ is equivalent to setting the string to the **vbNullString** constant in Visual Basic.</span></span> <span data-ttu-id="9cd18-110">Das übergeben einer Zeichenfolge der Länge 0 ("") an eine Funktion, die für den Empfang von **null** vorgesehen ist, funktioniert nicht, da dadurch ein Zeiger auf eine Zeichenfolge der Länge 0 (null) anstatt auf einen NULL-Zeiger übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9cd18-110">Passing in a zero-length string ("") to a function designed to receive **NULL** does not work, as this passes a pointer to a zero-length string instead of a zero pointer.</span></span>

<span data-ttu-id="9cd18-111">C++ unterstützt Datencontainer, d.. Strukturen und Unions, die in den frühen Versionen von Visual Basic keine Entsprechungen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9cd18-111">C++ supports data containers, namely structures and unions, that have no equivalent in early versions of Visual Basic.</span></span> <span data-ttu-id="9cd18-112">Aus diesem Grund wrappen com-Objekte in der Regel Informationen, die normalerweise in Strukturen und Unions in Objektklassen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="9cd18-112">For this reason, COM objects typically wrap information that usually is stored in structures and unions in object classes.</span></span> <span data-ttu-id="9cd18-113">Einige COM-Objekte enthalten jedoch möglicherweise Strukturen, die dazu führen, dass die Visual Basic auf Teile der Methoden oder Funktionen des Objekts nicht zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="9cd18-113">Some COM objects, however, may contain structures, causing portions of the object's methods or functionality to be inaccessible to Visual Basic.</span></span>

<span data-ttu-id="9cd18-114">Einige C++-Datentypen werden in Visual Basic nicht unterstützt, z. b. unsignierte Typen und **HWND** -Typen.</span><span class="sxs-lookup"><span data-stu-id="9cd18-114">Some C++ data types are not supported in Visual Basic, for example unsigned types and **HWND** types.</span></span> <span data-ttu-id="9cd18-115">Methoden, die diese Datentypen akzeptieren oder zurückgeben, sind in Visual Basic nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9cd18-115">Methods that accept or return these data types are not available in Visual Basic.</span></span>

<span data-ttu-id="9cd18-116">In Visual Basic werden die mit Automation kompatiblen Datentypen als interne Datentypen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9cd18-116">Visual Basic uses Automation-compatible data types as its internal data types.</span></span> <span data-ttu-id="9cd18-117">Daher sind C++-Datentypen, die Automatisierungs kompatibel sind, auch mit Visual Basic kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9cd18-117">Thus, C++ data types that are Automation-compatible are also compatible with Visual Basic.</span></span> <span data-ttu-id="9cd18-118">Datentypen, die nicht Automatisierungs kompatibel sind, können möglicherweise nicht in Visual Basic konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="9cd18-118">Data types that are not Automation-compatible may not be able to be converted to Visual Basic.</span></span>

<span data-ttu-id="9cd18-119">In der folgenden Tabelle werden die Datentypen aufgelistet, die von Visual Basic und ihren **VarType** -Entsprechungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9cd18-119">The following table lists the data types are supported by Visual Basic and their **VARTYPE** equivalents.</span></span> <span data-ttu-id="9cd18-120">**VarType** ist eine Enumeration, die die Arten von Automatisierungs Varianten auflistet.</span><span class="sxs-lookup"><span data-stu-id="9cd18-120">**VARTYPE** is an enumeration that lists the Automation variant types.</span></span>



| <span data-ttu-id="9cd18-121">Datentyp in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9cd18-121">Visual Basic data type</span></span>  | <span data-ttu-id="9cd18-122">VarType-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="9cd18-122">VARTYPE equivalent</span></span>                |
|-------------------------|-----------------------------------|
| <span data-ttu-id="9cd18-123">**Integer**</span><span class="sxs-lookup"><span data-stu-id="9cd18-123">**Integer**</span></span><br/>  | <span data-ttu-id="9cd18-124">16 Bit, signiert, VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="9cd18-124">16 bit, signed, VT\_I2</span></span><br/> |
| <span data-ttu-id="9cd18-125">**Long**</span><span class="sxs-lookup"><span data-stu-id="9cd18-125">**Long**</span></span><br/>     | <span data-ttu-id="9cd18-126">32 Bit, signiert, VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9cd18-126">32 bit, signed, VT\_I4</span></span><br/> |
| <span data-ttu-id="9cd18-127">**Datum**</span><span class="sxs-lookup"><span data-stu-id="9cd18-127">**Date**</span></span><br/>     | <span data-ttu-id="9cd18-128">VT- \_ Datum</span><span class="sxs-lookup"><span data-stu-id="9cd18-128">VT\_DATE</span></span><br/>               |
| <span data-ttu-id="9cd18-129">**Währung**</span><span class="sxs-lookup"><span data-stu-id="9cd18-129">**Currency**</span></span><br/> | <span data-ttu-id="9cd18-130">VT- \_ CY</span><span class="sxs-lookup"><span data-stu-id="9cd18-130">VT\_CY</span></span><br/>                 |
| <span data-ttu-id="9cd18-131">**Object**</span><span class="sxs-lookup"><span data-stu-id="9cd18-131">**Object**</span></span><br/>   | <span data-ttu-id="9cd18-132">\*VT \_ -Verteilung</span><span class="sxs-lookup"><span data-stu-id="9cd18-132">\*VT\_DISPATCH</span></span><br/>         |
| <span data-ttu-id="9cd18-133">**String**</span><span class="sxs-lookup"><span data-stu-id="9cd18-133">**String**</span></span><br/>   | <span data-ttu-id="9cd18-134">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="9cd18-134">VT\_BSTR</span></span><br/>               |
| <span data-ttu-id="9cd18-135">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="9cd18-135">**Boolean**</span></span><br/>  | <span data-ttu-id="9cd18-136">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="9cd18-136">VT\_BOOL</span></span><br/>               |
| <span data-ttu-id="9cd18-137">**Währung**</span><span class="sxs-lookup"><span data-stu-id="9cd18-137">**Currency**</span></span><br/> | <span data-ttu-id="9cd18-138">VT ( \_ dezimal)</span><span class="sxs-lookup"><span data-stu-id="9cd18-138">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="9cd18-139">**Single**</span><span class="sxs-lookup"><span data-stu-id="9cd18-139">**Single**</span></span><br/>   | <span data-ttu-id="9cd18-140">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="9cd18-140">VT\_R4</span></span><br/>                 |
| <span data-ttu-id="9cd18-141">**Double**</span><span class="sxs-lookup"><span data-stu-id="9cd18-141">**Double**</span></span><br/>   | <span data-ttu-id="9cd18-142">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="9cd18-142">VT\_R8</span></span><br/>                 |
| <span data-ttu-id="9cd18-143">**Dezimal**</span><span class="sxs-lookup"><span data-stu-id="9cd18-143">**Decimal**</span></span><br/>  | <span data-ttu-id="9cd18-144">VT ( \_ dezimal)</span><span class="sxs-lookup"><span data-stu-id="9cd18-144">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="9cd18-145">**Byte**</span><span class="sxs-lookup"><span data-stu-id="9cd18-145">**Byte**</span></span><br/>     | <span data-ttu-id="9cd18-146">VT ( \_ dezimal)</span><span class="sxs-lookup"><span data-stu-id="9cd18-146">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="9cd18-147">**Konfigur**</span><span class="sxs-lookup"><span data-stu-id="9cd18-147">**Variant**</span></span><br/>  | <span data-ttu-id="9cd18-148">VT- \_ Variante</span><span class="sxs-lookup"><span data-stu-id="9cd18-148">VT\_VARIANT</span></span><br/>            |



 

<span data-ttu-id="9cd18-149">Alle Parameter in Visual Basic, sofern Sie nicht mit dem Schlüsselwort **ByVal** gekennzeichnet sind, werden als Verweis (als Zeiger) anstatt als Wert übermittelt.</span><span class="sxs-lookup"><span data-stu-id="9cd18-149">All parameters in Visual Basic, unless labeled with the keyword **ByVal**, are passed by reference (as pointers) instead of by value.</span></span>

<span data-ttu-id="9cd18-150">C++ und Visual Basic unterscheiden sich geringfügig von der Darstellung von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9cd18-150">C++ and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="9cd18-151">In C++ werden Eigenschaften als ein Satz von Accessorfunktionen dargestellt, der den Eigenschafts Wert festlegt und einen, der den Eigenschafts Wert abruft.</span><span class="sxs-lookup"><span data-stu-id="9cd18-151">In C++, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="9cd18-152">In Visual Basic werden Eigenschaften als einzelnes Element dargestellt, das zum Abrufen oder Festlegen des Eigenschafts Werts verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9cd18-152">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cd18-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9cd18-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cd18-154">Übersetzen in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9cd18-154">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 





