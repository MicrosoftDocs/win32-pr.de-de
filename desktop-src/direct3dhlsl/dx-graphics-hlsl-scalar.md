---
title: Skalare Typen
description: Skalare Typen
ms.assetid: bf24d27f-2720-4268-bc74-fc46afedb9aa
keywords:
- Skalare Typen HLSL
topic_type:
- apiref
api_name:
- Scalar Types
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 7198932c6edb91e6f797b232b6c980976f3696a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "103761895"
---
# <a name="scalar-types"></a><span data-ttu-id="ed383-104">Skalare Typen</span><span class="sxs-lookup"><span data-stu-id="ed383-104">Scalar Types</span></span>


<span data-ttu-id="ed383-105">HLSL unterstützt mehrere skalare Datentypen:</span><span class="sxs-lookup"><span data-stu-id="ed383-105">HLSL supports several scalar data types:</span></span>

-   <span data-ttu-id="ed383-106">**bool** -true oder false.</span><span class="sxs-lookup"><span data-stu-id="ed383-106">**bool** - true or false.</span></span>
-   <span data-ttu-id="ed383-107">**int** -32-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="ed383-107">**int** - 32-bit signed integer.</span></span>
-   <span data-ttu-id="ed383-108">**uint** -32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="ed383-108">**uint** - 32-bit unsigned integer.</span></span>
-   <span data-ttu-id="ed383-109">**DWORD** -32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="ed383-109">**dword** - 32-bit unsigned integer.</span></span>
-   <span data-ttu-id="ed383-110">**halb** -16-Bit-Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="ed383-110">**half** - 16-bit floating point value.</span></span> <span data-ttu-id="ed383-111">Dieser Datentyp wird nur für die sprach Kompatibilität bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ed383-111">This data type is provided only for language compatibility.</span></span> <span data-ttu-id="ed383-112">Direct3D 10-Shader-Ziele ordnen alle halb Datentypen float-Datentypen zu.</span><span class="sxs-lookup"><span data-stu-id="ed383-112">Direct3D 10 shader targets map all half data types to float data types.</span></span> <span data-ttu-id="ed383-113">Ein halber Datentyp kann nicht für eine einheitliche globale Variable verwendet werden (verwenden Sie das/GEC-Flag, wenn diese Funktion gewünscht ist).</span><span class="sxs-lookup"><span data-stu-id="ed383-113">A half data type cannot be used on a uniform global variable (use the /Gec flag if this functionality is desired).</span></span>
-   <span data-ttu-id="ed383-114">Gleit Komma Wert **float** -32-Bit.</span><span class="sxs-lookup"><span data-stu-id="ed383-114">**float** - 32-bit floating point value.</span></span>
-   <span data-ttu-id="ed383-115">**Double** -64-Bit-Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="ed383-115">**double** - 64-bit floating point value.</span></span> <span data-ttu-id="ed383-116">Werte mit doppelter Genauigkeit können nicht als Eingaben und Ausgaben für einen Stream verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed383-116">You cannot use double precision values as inputs and outputs for a stream.</span></span> <span data-ttu-id="ed383-117">Um Werte mit doppelter Genauigkeit zwischen Shadern zu übergeben, deklarieren Sie jedes **Double** als Paar von **uint** -Datentypen.</span><span class="sxs-lookup"><span data-stu-id="ed383-117">To pass double precision values between shaders, declare each **double** as a pair of **uint** data types.</span></span> <span data-ttu-id="ed383-118">Verwenden Sie dann die [**asuint**](asuint.md) -Funktion, um jedes **Double** in das Paar **von uint** s und die [**AsDouble**](asdouble.md) -Funktion zu packen, um das Paar von **uint** s wieder in den **Double**-Typ zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="ed383-118">Then, use the [**asuint**](asuint.md) function to pack each **double** into the pair of **uint** s and the [**asdouble**](asdouble.md) function to unpack the pair of **uint** s back into the **double**.</span></span>

<span data-ttu-id="ed383-119">Ab Windows 8 unterstützt HLSL auch skalare Datentypen mit minimaler Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="ed383-119">Starting with Windows 8 HLSL also supports minimum precision scalar data types.</span></span> <span data-ttu-id="ed383-120">Grafiktreiber können Skalardatentypen mit minimaler Genauigkeit implementieren, indem Sie eine beliebige Genauigkeit angeben, die größer oder gleich der angegebenen bitgenauigkeit ist.</span><span class="sxs-lookup"><span data-stu-id="ed383-120">Graphics drivers can implement minimum precision scalar data types by using any precision greater than or equal to their specified bit precision.</span></span> <span data-ttu-id="ed383-121">Es wird empfohlen, sich nicht auf das Spannen-oder Wrapping Verhalten zu verlassen, das von einer bestimmten zugrunde liegenden Genauigkeit abhängt</span><span class="sxs-lookup"><span data-stu-id="ed383-121">We recommend not to rely on clamping or wrapping behavior that depends on specific underlying precision.</span></span> <span data-ttu-id="ed383-122">Beispielsweise kann der Grafiktreiber Arithmetik für einen **min16float** -Wert mit vollständiger 32-Bit-Genauigkeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed383-122">For example, the graphics driver might execute arithmetic on a **min16float** value at full 32-bit precision.</span></span>

-   <span data-ttu-id="ed383-123">**min16float** -minimaler 16-Bit-Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="ed383-123">**min16float** - minimum 16-bit floating point value.</span></span>
-   <span data-ttu-id="ed383-124">**min10float** -minimaler 10-Bit-Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="ed383-124">**min10float** - minimum 10-bit floating point value.</span></span>
-   <span data-ttu-id="ed383-125">**min16int** -minimale 16-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="ed383-125">**min16int** - minimum 16-bit signed integer.</span></span>
-   <span data-ttu-id="ed383-126">**min12int** -minimale 12-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="ed383-126">**min12int** - minimum 12-bit signed integer.</span></span>
-   <span data-ttu-id="ed383-127">**min16uint** -minimale 16-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="ed383-127">**min16uint** - minimum 16-bit unsigned integer.</span></span>

<span data-ttu-id="ed383-128">Weitere Informationen zu skalaren literalen finden Sie unter [Grammatik](dx-graphics-hlsl-appendix-grammar.md).</span><span class="sxs-lookup"><span data-stu-id="ed383-128">For more information about scalar literals, see [Grammar](dx-graphics-hlsl-appendix-grammar.md).</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ed383-129">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="ed383-129">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="ed383-130">In Direct3D 10 sind die folgenden Typen Modifizierer für den float-Typ.</span><span class="sxs-lookup"><span data-stu-id="ed383-130">In Direct3D 10, the following types are modifiers to the float type.</span></span><br/>
<ul>
<li><span data-ttu-id="ed383-131"><strong>snorm float</strong> - IEEE 32-Bit mit Vorzeichen-normalisierter Gleit Komma Zahl im Bereich von 1 bis 1 einschließlich.</span><span class="sxs-lookup"><span data-stu-id="ed383-131"><strong>snorm float</strong> - IEEE 32-bit signed-normalized float in range -1 to 1 inclusive.</span></span></li>
<li><span data-ttu-id="ed383-132"><strong>unorm float</strong> - IEEE 32-Bit ohne Vorzeichen-normalisierte Gleit Komma Zahl im Bereich von 0 bis 1 einschließlich.</span><span class="sxs-lookup"><span data-stu-id="ed383-132"><strong>unorm float</strong> - IEEE 32-bit unsigned-normalized float in range 0 to 1 inclusive.</span></span></li>
</ul>
<span data-ttu-id="ed383-133">Hier sehen Sie z. b. eine 4-komponentendeklaration mit Vorzeichen und normalisierte float-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ed383-133">For example, here is a 4-component signed-normalized float-variable declaration.</span></span><br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>snorm float4 fourComponentIEEEFloat;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 

## <a name="string-type"></a><span data-ttu-id="ed383-134">Zeichenfolgentyp</span><span class="sxs-lookup"><span data-stu-id="ed383-134">String Type</span></span>

<span data-ttu-id="ed383-135">HLSL unterstützt auch einen **Zeichen** Folgentyp, der eine ASCII-Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="ed383-135">HLSL also supports a **string** type, which is an ASCII string.</span></span> <span data-ttu-id="ed383-136">Es sind keine Vorgänge oder Zustände vorhanden, die Zeichen folgen akzeptieren, aber Effekte können Zeichen folgen Parameter und Anmerkungen Abfragen.</span><span class="sxs-lookup"><span data-stu-id="ed383-136">There are no operations or states that accept strings, but effects can query string parameters and annotations.</span></span>

## <a name="example"></a><span data-ttu-id="ed383-137">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ed383-137">Example</span></span>

```c
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```

## <a name="see-also"></a><span data-ttu-id="ed383-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ed383-138">See also</span></span>



* [<span data-ttu-id="ed383-139">Deklarieren von skalaren Typen</span><span class="sxs-lookup"><span data-stu-id="ed383-139">Declaring Scalar Types</span></span>](./dx-graphics-hlsl-writing-shaders-9.md#declaring-shader-variables)
* [<span data-ttu-id="ed383-140">Datentypen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ed383-140">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)