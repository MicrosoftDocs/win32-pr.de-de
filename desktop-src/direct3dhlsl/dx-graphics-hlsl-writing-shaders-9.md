---
title: Schreiben von HLSL-Shadern in Direct3D 9
description: Schreiben von HLSL-Shadern in Direct3D 9
ms.assetid: 7db6b264-c96c-4298-9b8a-d0c488390e4e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 504a1d9ff5a2aa2b37227f0016cdc97d28d967fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039378"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a><span data-ttu-id="39c07-103">Schreiben von HLSL-Shadern in Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="39c07-103">Writing HLSL Shaders in Direct3D 9</span></span>

-   [<span data-ttu-id="39c07-104">Vertex-Shader-Grundlagen</span><span class="sxs-lookup"><span data-stu-id="39c07-104">Vertex-Shader Basics</span></span>](#vertex-shader-basics)
-   [<span data-ttu-id="39c07-105">Grundlagen des Pixel-Shaders</span><span class="sxs-lookup"><span data-stu-id="39c07-105">Pixel-Shader Basics</span></span>](#pixel-shader-basics)
    -   [<span data-ttu-id="39c07-106">Textur Stufen und samplerzustände</span><span class="sxs-lookup"><span data-stu-id="39c07-106">Texture Stage and Sampler States</span></span>](#texture-stage-and-sampler-states)
    -   [<span data-ttu-id="39c07-107">Pixel-shadereingaben</span><span class="sxs-lookup"><span data-stu-id="39c07-107">Pixel Shader Inputs</span></span>](#pixel-shader-inputs)
    -   [<span data-ttu-id="39c07-108">Pixel-Shader-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39c07-108">Pixel Shader Outputs</span></span>](#pixel-shader-outputs)
-   [<span data-ttu-id="39c07-109">Shadereingaben und shadervariablen</span><span class="sxs-lookup"><span data-stu-id="39c07-109">Shader Inputs and Shader Variables</span></span>](#shader-inputs-and-shader-variables)
    -   [<span data-ttu-id="39c07-110">Deklarieren von shadervariablen</span><span class="sxs-lookup"><span data-stu-id="39c07-110">Declaring Shader Variables</span></span>](#declaring-shader-variables)
    -   [<span data-ttu-id="39c07-111">Einheitliche shadereingaben</span><span class="sxs-lookup"><span data-stu-id="39c07-111">Uniform Shader Inputs</span></span>](#uniform-shader-inputs)
    -   [<span data-ttu-id="39c07-112">Variierende shadereingaben und-Semantik</span><span class="sxs-lookup"><span data-stu-id="39c07-112">Varying Shader Inputs and Semantics</span></span>](#varying-shader-inputs-and-semantics)
    -   [<span data-ttu-id="39c07-113">Samplers und Textur Objekte</span><span class="sxs-lookup"><span data-stu-id="39c07-113">Samplers and Texture Objects</span></span>](#samplers-and-texture-objects)
-   [<span data-ttu-id="39c07-114">Schreiben von Funktionen</span><span class="sxs-lookup"><span data-stu-id="39c07-114">Writing Functions</span></span>](#writing-functions)
-   [<span data-ttu-id="39c07-115">Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="39c07-115">Flow Control</span></span>](#flow-control)
-   [<span data-ttu-id="39c07-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39c07-116">Related topics</span></span>](#related-topics)

## <a name="vertex-shader-basics"></a><span data-ttu-id="39c07-117">Grundlagen zu Vertex-Shader</span><span class="sxs-lookup"><span data-stu-id="39c07-117">Vertex-Shader Basics</span></span>

<span data-ttu-id="39c07-118">Bei einem Vorgang ersetzt ein programmierbarer Vertexshader die Scheitelpunkt Verarbeitung, die durch die Microsoft Direct3D-Grafik Pipeline durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39c07-118">When in operation, a programmable vertex shader replaces the vertex processing done by the Microsoft Direct3D graphics pipeline.</span></span> <span data-ttu-id="39c07-119">Bei der Verwendung eines Scheitelpunkt-Shaders werden Zustandsinformationen zu Transformations-und Beleuchtungs Vorgängen von der Fixed-Funktions Pipeline ignoriert.</span><span class="sxs-lookup"><span data-stu-id="39c07-119">While using a vertex shader, state information regarding transformation and lighting operations is ignored by the fixed function pipeline.</span></span> <span data-ttu-id="39c07-120">Wenn der Vertex-Shader deaktiviert ist und die Verarbeitung fester Funktionen zurückgegeben wird, gelten alle aktuellen Zustands Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="39c07-120">When the vertex shader is disabled and fixed function processing is returned, all current state settings apply.</span></span>

<span data-ttu-id="39c07-121">Vor der Ausführung des Vertexshaders sollte vor der Ausführung des Scheitelpunkt-Shaders ein Mosaik Prozess erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-121">Tessellation of high-order primitives should be done before the vertex shader executes.</span></span> <span data-ttu-id="39c07-122">Implementierungen, die nach der shaderverarbeitung das Oberflächen Mosaik ausführen, müssen dies auf eine Weise tun, die für die Anwendung und den Shader-Code nicht offensichtlich ist.</span><span class="sxs-lookup"><span data-stu-id="39c07-122">Implementations that perform surface tessellation after the shader processing must do so in a way that is not apparent to the application and shader code.</span></span>

<span data-ttu-id="39c07-123">Ein Vertex-Shader muss mindestens eine Scheitelpunkt Position im homogenen Clip Bereich ausgeben.</span><span class="sxs-lookup"><span data-stu-id="39c07-123">As a minimum, a vertex shader must output vertex position in homogeneous clip space.</span></span> <span data-ttu-id="39c07-124">Optional kann der Vertex-Shader Texturkoordinaten, Scheitelpunkt Farben, Scheitelpunkt Beleuchtung, Nebel Faktoren usw. ausgeben.</span><span class="sxs-lookup"><span data-stu-id="39c07-124">Optionally, the vertex shader can output texture coordinates, vertex color, vertex lighting, fog factors, and so on.</span></span>

## <a name="pixel-shader-basics"></a><span data-ttu-id="39c07-125">Grundlagen zu Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="39c07-125">Pixel-Shader Basics</span></span>

<span data-ttu-id="39c07-126">Die Pixel Verarbeitung erfolgt durch Pixel-Shader in einzelnen Pixeln.</span><span class="sxs-lookup"><span data-stu-id="39c07-126">Pixel processing is performed by pixel shaders on individual pixels.</span></span> <span data-ttu-id="39c07-127">Pixel-Shader arbeiten mit Vertex-Shadern. die Ausgabe eines Vertex-Shaders stellt die Eingaben für einen PixelShader bereit.</span><span class="sxs-lookup"><span data-stu-id="39c07-127">Pixel shaders work in concert with vertex shaders; the output of a vertex shader provides the inputs for a pixel shader.</span></span> <span data-ttu-id="39c07-128">Andere Pixel Vorgänge (Nebel-Blending, Schablone-Vorgänge und renderzielmischung) treten nach der Ausführung des Shaders auf.</span><span class="sxs-lookup"><span data-stu-id="39c07-128">Other pixel operations (fog blending, stencil operations, and render-target blending) occur after execution of the shader.</span></span>

### <a name="texture-stage-and-sampler-states"></a><span data-ttu-id="39c07-129">Textur Stufen und samplerzustände</span><span class="sxs-lookup"><span data-stu-id="39c07-129">Texture Stage and Sampler States</span></span>

<span data-ttu-id="39c07-130">Ein Pixelshader ersetzt vollständig die Pixel Mischungs Funktionen, die durch den Multitexture-Blender angegeben werden, einschließlich Vorgängen, die zuvor durch den Text der Textur Stufe definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="39c07-130">A pixel shader completely replaces the pixel-blending functionality specified by the multi-texture blender including operations previously defined by the texture stage states.</span></span> <span data-ttu-id="39c07-131">Textur Sampling-und Filter Vorgänge, die von den standardmäßigen Textur Phasen für Minimierung, Vergrößerung, MIP-Filterung und Umbruch Adressierungs Modi gesteuert wurden, können in Shadern initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-131">Texture sampling and filtering operations which were controlled by the standard texture stage states for minification, magnification, mip filtering, and the wrap addressing modes, can be initialized in shaders.</span></span> <span data-ttu-id="39c07-132">Die Anwendung kann diese Zustände ändern, ohne dass der derzeit gebundene Shader neu generiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="39c07-132">The application is free to change these states without requiring the regeneration of the currently bound shader.</span></span> <span data-ttu-id="39c07-133">Das Festlegen des Zustands kann sogar noch einfacher gemacht werden, wenn die Shader innerhalb eines Effekts entworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="39c07-133">Setting state can be made even easier if your shaders are designed within an effect.</span></span>

### <a name="pixel-shader-inputs"></a><span data-ttu-id="39c07-134">Pixel-shadereingaben</span><span class="sxs-lookup"><span data-stu-id="39c07-134">Pixel Shader Inputs</span></span>

<span data-ttu-id="39c07-135">Bei Pixel-Shader-Versionen PS \_ 1 \_ 1-PS \_ 2 \_ 0 sind diffuse und Glanz Farben im Bereich von 0 bis 1 erschöpft (geklammert), bevor Sie vom Shader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-135">For pixel shader versions ps\_1\_1 - ps\_2\_0, diffuse and specular colors are saturated (clamped) in the range 0 to 1 before use by the shader.</span></span>

<span data-ttu-id="39c07-136">Die Eingabe von Farbwerten für den Pixelshader wird als Perspektive angesehen, aber dies ist nicht garantiert (für alle Hardware).</span><span class="sxs-lookup"><span data-stu-id="39c07-136">Color values input to the pixel shader are assumed to be perspective correct, but this is not guaranteed (for all hardware).</span></span> <span data-ttu-id="39c07-137">Farben, die aus Texturkoordinaten entnommen werden, werden in einer Perspektive ordnungsgemäß durchlaufen und während der Iterationen an den Bereich von 0 bis 1 gebunden.</span><span class="sxs-lookup"><span data-stu-id="39c07-137">Colors sampled from texture coordinates are iterated in a perspective correct manner, and are clamped to the 0 to 1 range during iteration.</span></span>

### <a name="pixel-shader-outputs"></a><span data-ttu-id="39c07-138">Pixel-Shader-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39c07-138">Pixel Shader Outputs</span></span>

<span data-ttu-id="39c07-139">Bei Pixel-Shader-Versionen PS \_ 1 \_ 1-PS \_ 1 \_ 4 ist das vom Pixelshader ausgegebene Ergebnis der Inhalt von Register R0.</span><span class="sxs-lookup"><span data-stu-id="39c07-139">For pixel shader versions ps\_1\_1 - ps\_1\_4, the result emitted by the pixel shader is the contents of register r0.</span></span> <span data-ttu-id="39c07-140">Alles, was es enthält, wenn der Shader die Verarbeitung abschließt, wird an die Nebel-und Renderziel-Blender gesendet.</span><span class="sxs-lookup"><span data-stu-id="39c07-140">Whatever it contains when the shader completes processing is sent to the fog stage and render-target blender.</span></span>

<span data-ttu-id="39c07-141">Bei Pixel-Shader-Versionen PS \_ 2 \_ 0 und höher wird die Ausgabe Farbe von oC0-oC4 ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="39c07-141">For pixel shader versions ps\_2\_0 and above, output color is emitted from oC0 - oC4.</span></span>

## <a name="shader-inputs-and-shader-variables"></a><span data-ttu-id="39c07-142">Shadereingaben und shadervariablen</span><span class="sxs-lookup"><span data-stu-id="39c07-142">Shader Inputs and Shader Variables</span></span>

-   [<span data-ttu-id="39c07-143">Deklarieren von shadervariablen</span><span class="sxs-lookup"><span data-stu-id="39c07-143">Declaring Shader Variables</span></span>](#declaring-shader-variables)
-   [<span data-ttu-id="39c07-144">Einheitliche shadereingaben</span><span class="sxs-lookup"><span data-stu-id="39c07-144">Uniform Shader Inputs</span></span>](#uniform-shader-inputs)
-   [<span data-ttu-id="39c07-145">Variierende shadereingaben und-Semantik</span><span class="sxs-lookup"><span data-stu-id="39c07-145">Varying Shader Inputs and Semantics</span></span>](#varying-shader-inputs-and-semantics)
-   [<span data-ttu-id="39c07-146">Samplers und Textur Objekte</span><span class="sxs-lookup"><span data-stu-id="39c07-146">Samplers and Texture Objects</span></span>](#samplers-and-texture-objects)

### <a name="declaring-shader-variables"></a><span data-ttu-id="39c07-147">Deklarieren von shadervariablen</span><span class="sxs-lookup"><span data-stu-id="39c07-147">Declaring Shader Variables</span></span>

<span data-ttu-id="39c07-148">Die einfachste Variablen Deklaration enthält einen Typ und einen Variablennamen, wie z. b. diese Gleit Komma Deklaration:</span><span class="sxs-lookup"><span data-stu-id="39c07-148">The simplest variable declaration includes a type and a variable name, such as this floating-point declaration:</span></span>


```
float fVar;
```



<span data-ttu-id="39c07-149">Sie können eine Variable in derselben Anweisung initialisieren.</span><span class="sxs-lookup"><span data-stu-id="39c07-149">You can initialize a variable in the same statement.</span></span>


```
float fVar = 3.1f;
```



<span data-ttu-id="39c07-150">Ein Array von Variablen kann deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-150">An array of variables can be declared,</span></span>


```
int iVar[3];
```



<span data-ttu-id="39c07-151">oder in derselben Anweisung deklariert und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="39c07-151">or declared and initialized in the same statement.</span></span>


```
int iVar[3] = {1,2,3};
```



<span data-ttu-id="39c07-152">Im folgenden finden Sie einige Deklarationen, die viele der Merkmale von HLSL-Variablen (High-Level Shader Language) veranschaulichen:</span><span class="sxs-lookup"><span data-stu-id="39c07-152">Here are a few declarations that demonstrate many of the characteristics of high-level shader language (HLSL) variables:</span></span>


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



<span data-ttu-id="39c07-153">Datendeklarationen können einen beliebigen gültigen Typ verwenden, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="39c07-153">Data declarations can use any valid type including:</span></span>

-   [<span data-ttu-id="39c07-154">Datentypen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39c07-154">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
-   [<span data-ttu-id="39c07-155">Vector Type (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39c07-155">Vector Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-vector.md)
-   [<span data-ttu-id="39c07-156">Matrixtyp (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39c07-156">Matrix Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-matrix.md)
-   [<span data-ttu-id="39c07-157">Shadertyp (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39c07-157">Shader Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-shader.md)
-   [<span data-ttu-id="39c07-158">Sampltyp (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39c07-158">Sampler Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-sampler.md)
-   [<span data-ttu-id="39c07-159">Benutzerdefinierter Typ (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39c07-159">User-Defined Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-user-defined.md)

<span data-ttu-id="39c07-160">Ein Shader kann Variablen, Argumente und Funktionen der obersten Ebene aufweisen.</span><span class="sxs-lookup"><span data-stu-id="39c07-160">A shader can have top-level variables, arguments, and functions.</span></span>


```
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



<span data-ttu-id="39c07-161">Variablen der obersten Ebene werden außerhalb aller Funktionen deklariert.</span><span class="sxs-lookup"><span data-stu-id="39c07-161">Top-level variables are declared outside of all functions.</span></span> <span data-ttu-id="39c07-162">Argumente der obersten Ebene sind Parameter für eine Funktion der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="39c07-162">Top-level arguments are parameters to a top-level function.</span></span> <span data-ttu-id="39c07-163">Eine Funktion der obersten Ebene ist jede Funktion, die von der Anwendung aufgerufen wird (im Gegensatz zu einer Funktion, die von einer anderen Funktion aufgerufen wird).</span><span class="sxs-lookup"><span data-stu-id="39c07-163">A top-level function is any function called by the application (as opposed to a function that is called by another function).</span></span>

### <a name="uniform-shader-inputs"></a><span data-ttu-id="39c07-164">Einheitliche shadereingaben</span><span class="sxs-lookup"><span data-stu-id="39c07-164">Uniform Shader Inputs</span></span>

<span data-ttu-id="39c07-165">Scheitelpunkt-und Pixel-Shader akzeptieren zwei Arten von Eingabedaten: unterschiedlich und einheitlich.</span><span class="sxs-lookup"><span data-stu-id="39c07-165">Vertex and pixel shaders accept two kinds of input data: varying and uniform.</span></span> <span data-ttu-id="39c07-166">Die unterschiedliche Eingabe sind die Daten, die für jede Ausführung des Shaders eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="39c07-166">The varying input is the data that is unique to each execution of the shader.</span></span> <span data-ttu-id="39c07-167">Bei einem Vertex-Shader stammen die unterschiedlichen Daten (z. b. Position, normal usw.) aus den vertexstreams.</span><span class="sxs-lookup"><span data-stu-id="39c07-167">For a vertex shader, the varying data (for example: position, normal, etc.) comes from the vertex streams.</span></span> <span data-ttu-id="39c07-168">Die einheitlichen Daten (z. b. Material Color, World Transform usw.) sind für mehrere Ausführungen eines Shaders konstant.</span><span class="sxs-lookup"><span data-stu-id="39c07-168">The uniform data (for example: material color, world transform, etc.) is constant for multiple executions of a shader.</span></span> <span data-ttu-id="39c07-169">Für diejenigen, die mit den assemblyshader-Modellen vertraut sind, werden einheitliche Daten durch konstante Register und abweichende Daten durch die v-und t-Register angegeben.</span><span class="sxs-lookup"><span data-stu-id="39c07-169">For those familiar with the assembly shader models, uniform data is specified by constant registers and varying data by the v and t registers.</span></span>

<span data-ttu-id="39c07-170">Einheitliche Daten können durch zwei Methoden angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-170">Uniform data can be specified by two methods.</span></span> <span data-ttu-id="39c07-171">Die gängigste Methode besteht darin, globale Variablen zu deklarieren und in einem Shader zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39c07-171">The most common method is to declare global variables and use them within a shader.</span></span> <span data-ttu-id="39c07-172">Jede Verwendung von globalen Variablen in einem Shader führt dazu, dass diese Variable der Liste der für diesen Shader erforderlichen, einheitlichen Variablen hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="39c07-172">Any use of global variables within a shader will result in adding that variable to the list of uniform variables required by that shader.</span></span> <span data-ttu-id="39c07-173">Die zweite Methode besteht darin, einen Eingabeparameter der Shader-Funktion der obersten Ebene als einheitlich zu markieren.</span><span class="sxs-lookup"><span data-stu-id="39c07-173">The second method is to mark an input parameter of the top-level shader function as uniform.</span></span> <span data-ttu-id="39c07-174">Diese Markierung gibt an, dass die angegebene Variable der Liste der einheitlichen Variablen hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="39c07-174">This marking specifies that the given variable should be added to the list of uniform variables.</span></span>

<span data-ttu-id="39c07-175">Von einem Shader verwendete einheitliche Variablen werden über die Konstante Tabelle an die Anwendung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="39c07-175">Uniform variables used by a shader are communicated back to the application via the constant table.</span></span> <span data-ttu-id="39c07-176">Die Konstante Tabelle ist der Name für die Symboltabelle, der definiert, wie die von einem Shader verwendeten einheitlichen Variablen in die Konstanten Register passen.</span><span class="sxs-lookup"><span data-stu-id="39c07-176">The constant table is the name for the symbol table that defines how the uniform variables used by a shader fit into the constant registers.</span></span> <span data-ttu-id="39c07-177">Die Parameter der einheitlichen Funktion erscheinen in der Konstanten Tabelle, der ein Dollarzeichen ($) vorangestellt ist, im Gegensatz zu den globalen Variablen.</span><span class="sxs-lookup"><span data-stu-id="39c07-177">The uniform function parameters appear in the constant table prepended with a dollar sign ($), unlike the global variables.</span></span> <span data-ttu-id="39c07-178">Das Dollarzeichen ist erforderlich, um Namenskollisionen zwischen lokalen, einheitlichen Eingaben und globalen Variablen mit demselben Namen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="39c07-178">The dollar sign is required to avoid name collisions between local uniform inputs and global variables of the same name.</span></span>

<span data-ttu-id="39c07-179">Die Konstante Tabelle enthält die Konstanten Register Speicherorte aller vom Shader verwendeten einheitlichen Variablen.</span><span class="sxs-lookup"><span data-stu-id="39c07-179">The constant table contains the constant register locations of all uniform variables used by the shader.</span></span> <span data-ttu-id="39c07-180">Die Tabelle enthält auch die Typinformationen und den Standardwert, falls angegeben.</span><span class="sxs-lookup"><span data-stu-id="39c07-180">The table also includes the type information and the default value, if specified.</span></span>

### <a name="varying-shader-inputs-and-semantics"></a><span data-ttu-id="39c07-181">Variierende shadereingaben und-Semantik</span><span class="sxs-lookup"><span data-stu-id="39c07-181">Varying Shader Inputs and Semantics</span></span>

<span data-ttu-id="39c07-182">Abweichende Eingabeparameter (einer shaderfunktion der obersten Ebene) müssen entweder mit einem Semantic-oder Uniform-Schlüsselwort markiert werden, das angibt, dass der Wert für die Ausführung des Shaders konstant ist.</span><span class="sxs-lookup"><span data-stu-id="39c07-182">Varying input parameters (of a top-level shader function) must be marked either with a semantic or uniform keyword indicating the value is constant for the execution of the shader.</span></span> <span data-ttu-id="39c07-183">Wenn eine Shader-Eingabe der obersten Ebene nicht mit einem Semantic-oder Uniform-Schlüsselwort gekennzeichnet ist, kann der Shader nicht kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-183">If a top-level shader input is not marked with a semantic or uniform keyword, then the shader will fail to compile.</span></span>

<span data-ttu-id="39c07-184">Die Eingabe Semantik ist ein Name, der verwendet wird, um die angegebene Eingabe mit einer Ausgabe des vorherigen Teils der Grafik Pipeline zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="39c07-184">The input semantic is a name used to link the given input to an output of the previous part of the graphics pipeline.</span></span> <span data-ttu-id="39c07-185">Beispielsweise wird die Eingabe Semantik POSITION0 von den Vertexshadern verwendet, um anzugeben, wo die Positionsdaten aus dem Vertex-Puffer verknüpft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="39c07-185">For example, the input semantic POSITION0 is used by the vertex shaders to specify where the position data from the vertex buffer should be linked.</span></span>

<span data-ttu-id="39c07-186">Pixel-und Vertex-Shader haben unterschiedliche Sätze der Eingabe Semantik, da die verschiedenen Teile der Grafik Pipeline in jede shadereinheit eingecheckt werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-186">Pixel and vertex shaders have different sets of input semantics due to the different parts of the graphics pipeline that feed into each shader unit.</span></span> <span data-ttu-id="39c07-187">Die Vertex-Shader-Eingabe Semantik beschreibt die pro-Vertex-Informationen (z. b. Position, normal, Texturkoordinaten, Farbe, Tangens, Binormal usw.), die aus einem Vertex-Puffer in ein Formular geladen werden sollen, das vom Vertexshader verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="39c07-187">Vertex shader input semantics describe the per-vertex information (for example: position, normal, texture coordinates, color, tangent, binormal, etc.) to be loaded from a vertex buffer into a form that can be consumed by the vertex shader.</span></span> <span data-ttu-id="39c07-188">Die Eingabe Semantik wird direkt der Vertex-Deklarations Verwendung und dem Verwendungs Index zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="39c07-188">The input semantics directly map to the vertex declaration usage and the usage index.</span></span>

<span data-ttu-id="39c07-189">Die Pixel-Shader-Eingabe Semantik beschreibt die Informationen, die pro Pixel von der rasterisierungseinheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-189">Pixel shader input semantics describe the information that is provided per pixel by the rasterization unit.</span></span> <span data-ttu-id="39c07-190">Die Daten werden durch Interpolation zwischen Ausgaben des Vertex-Shaders für jeden Scheitelpunkt des aktuellen primitiven generiert.</span><span class="sxs-lookup"><span data-stu-id="39c07-190">The data is generated by interpolating between outputs of the vertex shader for each vertex of the current primitive.</span></span> <span data-ttu-id="39c07-191">Die grundlegende Pixel-Shader-Eingabe Semantik verknüpft die Ausgabe Farbe und die Texturkoordinaten Informationen mit den Eingabe Parametern.</span><span class="sxs-lookup"><span data-stu-id="39c07-191">The basic pixel shader input semantics link the output color and texture coordinate information to input parameters.</span></span>

<span data-ttu-id="39c07-192">Die Eingabe Semantik kann Shader-Eingaben mit zwei Methoden zugewiesen werden:</span><span class="sxs-lookup"><span data-stu-id="39c07-192">Input semantics can be assigned to shader input by two methods:</span></span>

-   <span data-ttu-id="39c07-193">Anhängen eines Doppelpunkts und des semantischen namens an die Parameter Deklaration.</span><span class="sxs-lookup"><span data-stu-id="39c07-193">Appending a colon and the semantic name to the parameter declaration.</span></span>
-   <span data-ttu-id="39c07-194">Definieren einer Eingabe Struktur mit der Eingabe Semantik, die jedem Strukturmember zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="39c07-194">Defining an input structure with input semantics assigned to each structure member.</span></span>

<span data-ttu-id="39c07-195">Vertex-und Pixel-Shader stellen Ausgabedaten für die nachfolgende Grafik Pipeline Phase bereit.</span><span class="sxs-lookup"><span data-stu-id="39c07-195">Vertex and pixel shaders provide output data to the subsequent graphics pipeline stage.</span></span> <span data-ttu-id="39c07-196">Die Ausgabe Semantik wird verwendet, um anzugeben, wie Daten, die vom Shader generiert werden, mit den Eingaben der nächsten Stufe verknüpft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="39c07-196">Output semantics are used to specify how data generated by the shader should be linked to the inputs of the next stage.</span></span> <span data-ttu-id="39c07-197">Beispielsweise wird die Ausgabe Semantik für einen Vertex-Shader verwendet, um die Ausgaben der Interpolatoren im Raster zu verknüpfen, um die Eingabedaten für den Pixelshader zu generieren.</span><span class="sxs-lookup"><span data-stu-id="39c07-197">For example, the output semantics for a vertex shader are used to link the outputs of the interpolators in the rasterizer to generate the input data for the pixel shader.</span></span> <span data-ttu-id="39c07-198">Die Pixel-Shader-Ausgaben sind die Werte, die für die Alpha Mischungs Einheit für jedes der Renderziele bereitgestellt werden, oder der in den tiefen Puffer geschriebene tiefen Wert.</span><span class="sxs-lookup"><span data-stu-id="39c07-198">The pixel shader outputs are the values provided to the alpha blending unit for each of the render targets or the depth value written to the depth buffer.</span></span>

<span data-ttu-id="39c07-199">Die Vertex-Shader-Ausgabe Semantik wird verwendet, um den Shader sowohl mit dem Pixelshader als auch mit der Raster-Stufe zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="39c07-199">Vertex shader output semantics are used to link the shader both to the pixel shader and to the rasterizer stage.</span></span> <span data-ttu-id="39c07-200">Ein Vertexshader, der vom Raster genutzt wird und nicht für den Pixelshader verfügbar gemacht wird, muss die Positionsdaten als minimal generieren.</span><span class="sxs-lookup"><span data-stu-id="39c07-200">A vertex shader that is consumed by the rasterizer and not exposed to the pixel shader must generate position data as a minimum.</span></span> <span data-ttu-id="39c07-201">Vertexshader, die Texturkoordinaten und Farbdaten generieren, stellen diese Daten einem Pixelshader nach dem Durchführen der Interpolation zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="39c07-201">Vertex shaders that generate texture coordinate and color data provide that data to a pixel shader after interpolation is done.</span></span>

<span data-ttu-id="39c07-202">Die Pixel-Shader-Ausgabe Semantik bindet die Ausgabe Farben eines Pixelshaders mit dem richtigen Renderziel.</span><span class="sxs-lookup"><span data-stu-id="39c07-202">Pixel shader output semantics bind the output colors of a pixel shader with the correct render target.</span></span> <span data-ttu-id="39c07-203">Die Pixel-Shader-Ausgabe Farbe ist mit der Alpha Blend-Phase verknüpft, die bestimmt, wie die zielrenderziele geändert werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-203">The pixel shader output color is linked to the alpha blend stage, which determines how the destination render targets are modified.</span></span> <span data-ttu-id="39c07-204">Die Ausgabe der Pixel-Shader-Tiefe kann verwendet werden, um die Ziel tiefen Werte an der aktuellen Raster Position zu ändern.</span><span class="sxs-lookup"><span data-stu-id="39c07-204">The pixel shader depth output can be used to change the destination depth values at the current raster location.</span></span> <span data-ttu-id="39c07-205">Die tiefen Ausgabe und mehrere Renderingziele werden nur mit einigen shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39c07-205">The depth output and multiple render targets are only supported with some shader models.</span></span>

<span data-ttu-id="39c07-206">Die Syntax für die Ausgabe Semantik ist mit der Syntax zum Angeben der Eingabe Semantik identisch.</span><span class="sxs-lookup"><span data-stu-id="39c07-206">The syntax for output semantics is identical to the syntax for specifying input semantics.</span></span> <span data-ttu-id="39c07-207">Die Semantik kann entweder direkt für Parameter angegeben werden, die als "out"-Parameter deklariert oder während der Definition einer Struktur zugewiesen werden, die entweder als "out"-Parameter oder als Rückgabewert einer Funktion zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="39c07-207">The semantics can be either specified directly on parameters declared as "out" parameters or assigned during the definition of a structure that either returned as an "out" parameter or the return value of a function.</span></span>

<span data-ttu-id="39c07-208">Die Semantik identifiziert, woher die Daten stammen.</span><span class="sxs-lookup"><span data-stu-id="39c07-208">Semantics identify where data comes from.</span></span> <span data-ttu-id="39c07-209">Semantik sind optionale Bezeichner zur Identifizierung von shadereingaben und-Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="39c07-209">Semantics are optional identifiers that identify shader inputs and outputs.</span></span> <span data-ttu-id="39c07-210">Die Semantik wird an einem von drei Stellen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="39c07-210">Semantics appear in one of three places:</span></span>

-   <span data-ttu-id="39c07-211">Nach einem Strukturmember.</span><span class="sxs-lookup"><span data-stu-id="39c07-211">After a structure member.</span></span>
-   <span data-ttu-id="39c07-212">Nach einem Argument in der Eingabe Argumentliste einer Funktion.</span><span class="sxs-lookup"><span data-stu-id="39c07-212">After an argument in a function's input argument list.</span></span>
-   <span data-ttu-id="39c07-213">Nach der Eingabe Argumentliste der Funktion.</span><span class="sxs-lookup"><span data-stu-id="39c07-213">After the function's input argument list.</span></span>

<span data-ttu-id="39c07-214">In diesem Beispiel wird eine-Struktur verwendet, um eine oder mehrere vertexshadereingaben bereitzustellen, und eine weitere-Struktur, um eine oder mehrere vertexshaderausgaben bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="39c07-214">This example uses a structure to provide one or more vertex shader inputs, and another structure to provide one or more vertex shader outputs.</span></span> <span data-ttu-id="39c07-215">Jedes der Strukturmember verwendet eine Semantik.</span><span class="sxs-lookup"><span data-stu-id="39c07-215">Each of the structure members uses a semantic.</span></span>


```
vector vClr;

struct VS_INPUT
{
    float4 vPosition : POSITION;
    float3 vNormal : NORMAL;
    float4 vBlendWeights : BLENDWEIGHT;
};

struct VS_OUTPUT
{
    float4  vPosition : POSITION;
    float4  vDiffuse : COLOR;

};

float4x4 mWld1;
float4x4 mWld2;
float4x4 mWld3;
float4x4 mWld4;

float Len;
float4 vLight;

float4x4 mTot;

VS_OUTPUT VS_Skinning_Example(const VS_INPUT v, uniform float len=100)
{
    VS_OUTPUT out;

    // Skin position (to world space)
    float3 vPosition = 
        mul(v.vPosition, (float4x3) mWld1) * v.vBlendWeights.x +
        mul(v.vPosition, (float4x3) mWld2) * v.vBlendWeights.y +
        mul(v.vPosition, (float4x3) mWld3) * v.vBlendWeights.z +
        mul(v.vPosition, (float4x3) mWld4) * v.vBlendWeights.w;
    // Skin normal (to world space)
    float3 vNormal =
        mul(v.vNormal, (float3x3) mWld1) * v.vBlendWeights.x + 
        mul(v.vNormal, (float3x3) mWld2) * v.vBlendWeights.y + 
        mul(v.vNormal, (float3x3) mWld3) * v.vBlendWeights.z + 
        mul(v.vNormal, (float3x3) mWld4) * v.vBlendWeights.w;
    
    // Output stuff
    out.vPosition    = mul(float4(vPosition + vNormal * Len, 1), mTot);
    out.vDiffuse  = dot(vLight,vNormal);

    return out;
}
```



<span data-ttu-id="39c07-216">Die Eingabe Struktur identifiziert die Daten aus dem Vertex-Puffer, der die shadereingaben bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="39c07-216">The input structure identifies the data from the vertex buffer that will provide the shader inputs.</span></span> <span data-ttu-id="39c07-217">Dieser Shader ordnet die Daten aus den Positionen "Position", "Normal" und "blendweight" des Vertexpuffers den Vertex-Shader-Registern zu.</span><span class="sxs-lookup"><span data-stu-id="39c07-217">This shader maps the data from the position, normal, and blendweight elements of the vertex buffer into vertex shader registers.</span></span> <span data-ttu-id="39c07-218">Der Eingabe Datentyp muss nicht exakt mit dem Datentyp der Vertex-Deklaration übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="39c07-218">The input data type does not have to exactly match the vertex declaration data type.</span></span> <span data-ttu-id="39c07-219">Wenn Sie nicht genau übereinstimmt, werden die Scheitelpunkt Daten automatisch in den Datentyp von HLSL konvertiert, wenn Sie in die Shader-Register geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-219">If it doesn't exactly match, the vertex data will automatically be converted into the HLSL's data type when it is written into the shader registers.</span></span> <span data-ttu-id="39c07-220">Wenn beispielsweise die normalen Daten vom Typ uint von der Anwendung definiert wurden, werden Sie beim Lesen durch den Shader in eine float3 konvertiert.</span><span class="sxs-lookup"><span data-stu-id="39c07-220">For instance, if the normal data were defined to be of type UINT by the application, it would be converted into a float3 when read by the shader.</span></span>

<span data-ttu-id="39c07-221">Wenn die Daten im vertexstream weniger Komponenten als der entsprechende shaderdatentyp enthalten, werden die fehlenden Komponenten mit 0 initialisiert (mit Ausnahme von w, die auf 1 initialisiert wird).</span><span class="sxs-lookup"><span data-stu-id="39c07-221">If the data in the vertex stream contains fewer components than the corresponding shader data type, the missing components will be initialized to 0 (except for w, which is initialized to 1).</span></span>

<span data-ttu-id="39c07-222">Die Eingabe Semantik ähnelt den Werten in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span><span class="sxs-lookup"><span data-stu-id="39c07-222">Input semantics are similar to the values in the [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span></span>

<span data-ttu-id="39c07-223">Die Ausgabestruktur identifiziert die Scheitelpunkt-Shader-Ausgabeparameter von Position und Farbe.</span><span class="sxs-lookup"><span data-stu-id="39c07-223">The output structure identifies the vertex shader output parameters of position and color.</span></span> <span data-ttu-id="39c07-224">Diese Ausgaben werden von der Pipeline für die Dreiecks rasterisierung (in primitiver Verarbeitung) verwendet.</span><span class="sxs-lookup"><span data-stu-id="39c07-224">These outputs will be used by the pipeline for triangle rasterization (in primitive processing).</span></span> <span data-ttu-id="39c07-225">Die als Positionsdaten markierte Ausgabe bezeichnet die Position eines Scheitel Punkts in homogenem Raum.</span><span class="sxs-lookup"><span data-stu-id="39c07-225">The output marked as position data denotes the position of a vertex in homogeneous space.</span></span> <span data-ttu-id="39c07-226">Ein Vertex-Shader muss mindestens Positionsdaten generieren.</span><span class="sxs-lookup"><span data-stu-id="39c07-226">As a minimum, a vertex shader must generate position data.</span></span> <span data-ttu-id="39c07-227">Die Position des Bildschirm Raums wird berechnet, nachdem der Vertexshader abgeschlossen ist, indem die (x, y, z)-Koordinate durch w dividiert wird.</span><span class="sxs-lookup"><span data-stu-id="39c07-227">The screen space position is computed after the vertex shader completes by dividing the (x, y, z) coordinate by w.</span></span> <span data-ttu-id="39c07-228">Im Bildschirmbereich sind-1 und 1 die minimalen und maximalen x-und y-Werte der Grenzen des Viewports, während z zum Testen von z-Puffern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="39c07-228">In screen space, -1 and 1 are the minimum and maximum x and y values of the boundaries of the viewport, while z is used for z-buffer testing.</span></span>

<span data-ttu-id="39c07-229">Die Ausgabe Semantik ähnelt auch den Werten in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span><span class="sxs-lookup"><span data-stu-id="39c07-229">Output semantics are also similar to the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span></span> <span data-ttu-id="39c07-230">Im Allgemeinen kann eine Ausgabestruktur für einen Vertex-Shader auch als Eingabe Struktur für einen PixelShader verwendet werden, vorausgesetzt, der Pixelshader liest nicht aus einer Variablen, die mit der Position, der Punktgröße oder der Semantik des Diagramms gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="39c07-230">In general, an output structure for a vertex shader can also be used as the input structure for a pixel shader, provided the pixel shader does not read from any variable marked with the position, point size, or fog semantics.</span></span> <span data-ttu-id="39c07-231">Diese Semantik wird mit pro-Vertex-Skalarwerten verknüpft, die nicht von einem Pixelshader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-231">These semantics are associated with per-vertex scalar values that are not used by a pixel shader.</span></span> <span data-ttu-id="39c07-232">Wenn diese Werte für den Pixelshader erforderlich sind, können Sie in eine andere Ausgabevariable kopiert werden, die eine Pixel-Shader-Semantik verwendet.</span><span class="sxs-lookup"><span data-stu-id="39c07-232">If these values are needed for the pixel shader, they can be copied into another output variable that uses a pixel shader semantic.</span></span>

<span data-ttu-id="39c07-233">Globale Variablen werden vom Compiler automatisch registriert.</span><span class="sxs-lookup"><span data-stu-id="39c07-233">Global variables are assigned to registers automatically by the compiler.</span></span> <span data-ttu-id="39c07-234">Globale Variablen werden auch als einheitliche Parameter bezeichnet, da der Inhalt der Variablen bei jedem Aufruf des Shaders identisch für alle Pixel ist, die verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-234">Global variables are also called uniform parameters because the contents of the variable is the same for all pixels processed each time the shader is called.</span></span> <span data-ttu-id="39c07-235">Die Register sind in der Konstanten Tabelle enthalten, die mit der [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) -Schnittstelle gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="39c07-235">The registers are contained in the constant table, which can be read using the [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) interface.</span></span>

<span data-ttu-id="39c07-236">Die Eingabe Semantik für Pixel-Shader ordnet Werte bestimmten Hardware Registern für den Transport zwischen Scheitelpunkt-Shadern und Pixel-Shadern zu.</span><span class="sxs-lookup"><span data-stu-id="39c07-236">Input semantics for pixel shaders map values into specific hardware registers for transport between vertex shaders and pixel shaders.</span></span> <span data-ttu-id="39c07-237">Jeder registriungstyp verfügt über bestimmte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="39c07-237">Each register type has specific properties.</span></span> <span data-ttu-id="39c07-238">Da zurzeit nur zwei Semantik für Farb-und Texturkoordinaten vorhanden ist, werden die meisten Daten häufig als Texturkoordinaten gekennzeichnet, auch wenn dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="39c07-238">Because there are currently only two semantics for color and texture coordinates, it is common for most data to be marked as a texture coordinate even when it is not.</span></span>

<span data-ttu-id="39c07-239">Beachten Sie, dass die Vertex-Shader-Ausgabestruktur eine Eingabe mit Positionsdaten verwendet hat, die nicht vom Pixelshader verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="39c07-239">Notice that the vertex shader output structure used an input with position data, which is not used by the pixel shader.</span></span> <span data-ttu-id="39c07-240">HLSL ermöglicht gültige Ausgabedaten eines Vertexshaders, bei dem es sich nicht um gültige Eingabedaten für einen PixelShader handelt, vorausgesetzt, dass im Pixelshader nicht auf Sie verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="39c07-240">HLSL allows valid output data of a vertex shader that is not valid input data for a pixel shader, provided that it is not referenced in the pixel shader.</span></span>

<span data-ttu-id="39c07-241">Eingabeargumente können auch Arrays sein.</span><span class="sxs-lookup"><span data-stu-id="39c07-241">Input arguments can also be arrays.</span></span> <span data-ttu-id="39c07-242">Die Semantik wird automatisch vom Compiler für jedes Element des Arrays inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="39c07-242">Semantics are automatically incremented by the compiler for each element of the array.</span></span> <span data-ttu-id="39c07-243">Beachten Sie beispielsweise die folgende explizite Deklaration:</span><span class="sxs-lookup"><span data-stu-id="39c07-243">For instance, consider the following explicit declaration:</span></span>


```
struct VS_OUTPUT
{
    float4 Position   : POSITION;
    float3 Diffuse    : COLOR0;
    float3 Specular   : COLOR1;               
    float3 HalfVector : TEXCOORD3;
    float3 Fresnel    : TEXCOORD2;               
    float3 Reflection : TEXCOORD0;               
    float3 NoiseCoord : TEXCOORD1;               
};

float4 Sparkle(VS_OUTPUT In) : COLOR
```



<span data-ttu-id="39c07-244">Die oben angegebene explizite Deklaration entspricht der folgenden Deklaration, deren Semantik vom Compiler automatisch inkrementiert wird:</span><span class="sxs-lookup"><span data-stu-id="39c07-244">The explicit declaration given above is equivalent to the following declaration that will have semantics automatically incremented by the compiler:</span></span>


```
float4 Sparkle(float4 Position : POSITION,
                 float3 Col[2] : COLOR0,
                 float3 Tex[4] : TEXCOORD0) : COLOR0
{
   // shader statements
   ...
```



<span data-ttu-id="39c07-245">Ebenso wie die Eingabe Semantik identifiziert die Ausgabe Semantik die Datenverwendung für die Pixel-Shader-Ausgabedaten.</span><span class="sxs-lookup"><span data-stu-id="39c07-245">Just like input semantics, output semantics identify data usage for pixel shader output data.</span></span> <span data-ttu-id="39c07-246">Viele Pixel-Shader schreiben nur in eine Ausgabe Farbe.</span><span class="sxs-lookup"><span data-stu-id="39c07-246">Many pixel shaders write to only one output color.</span></span> <span data-ttu-id="39c07-247">Pixel-Shader können auch gleichzeitig einen tiefen Wert in ein oder mehrere Renderingziele schreiben (bis zu vier).</span><span class="sxs-lookup"><span data-stu-id="39c07-247">Pixel shaders can also write out a depth value into one or more multiple render targets at the same time (up to four).</span></span> <span data-ttu-id="39c07-248">Wie Vertex-Shader verwenden Pixel-Shader eine-Struktur, um mehr als eine Ausgabe zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="39c07-248">Like vertex shaders, pixel shaders use a structure to return more than one output.</span></span> <span data-ttu-id="39c07-249">Dieser Shader schreibt 0 sowohl in die Farbkomponenten als auch in die tiefen Komponente.</span><span class="sxs-lookup"><span data-stu-id="39c07-249">This shader writes 0 to the color components, as well as to the depth component.</span></span>


```
struct PS_OUTPUT
{
    float4 Color[4] : COLOR0;
    float  Depth  : DEPTH;
};

PS_OUTPUT main(void)
{
    PS_OUTPUT out;

   // Shader statements
   ...

  // Write up to four pixel shader output colors
  out.Color[0] =  ...
  out.Color[1] =  ...
  out.Color[2] =  ...
  out.Color[3] =  ...

  // Write pixel depth 
  out.Depth =  ...

    return out;
}
```



<span data-ttu-id="39c07-250">Die Pixel-Shader-Ausgabe Farben müssen den Typ "float4" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="39c07-250">Pixel shader output colors must be of type float4.</span></span> <span data-ttu-id="39c07-251">Wenn Sie mehrere Farben schreiben, müssen alle Ausgabe Farben zusammenhängend verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-251">When writing multiple colors, all output colors must be used contiguously.</span></span> <span data-ttu-id="39c07-252">Anders ausgedrückt kann [COLOR1](dx-graphics-hlsl-semantics.md) keine Ausgabe sein, es sei denn, [COLOR0](dx-graphics-hlsl-semantics.md) wurde bereits geschrieben.</span><span class="sxs-lookup"><span data-stu-id="39c07-252">In other words, [COLOR1](dx-graphics-hlsl-semantics.md) cannot be an output unless [COLOR0](dx-graphics-hlsl-semantics.md) has already been written.</span></span> <span data-ttu-id="39c07-253">Die Ausgabe der Pixel-Shader-Tiefe muss vom Typ float1 sein.</span><span class="sxs-lookup"><span data-stu-id="39c07-253">Pixel shader depth output must be of type float1.</span></span>

### <a name="samplers-and-texture-objects"></a><span data-ttu-id="39c07-254">Samplers und Textur Objekte</span><span class="sxs-lookup"><span data-stu-id="39c07-254">Samplers and Texture Objects</span></span>

<span data-ttu-id="39c07-255">Ein Sampler enthält den samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="39c07-255">A sampler contains sampler state.</span></span> <span data-ttu-id="39c07-256">Der samplerstatus gibt die zu sammelnde Textur an und steuert die Filterung, die während des Samplings durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39c07-256">Sampler state specifies the texture to be sampled, and controls the filtering that is done during sampling.</span></span> <span data-ttu-id="39c07-257">Zum Beispiel für eine Textur sind drei Schritte erforderlich:</span><span class="sxs-lookup"><span data-stu-id="39c07-257">Three things are required to sample a texture:</span></span>

-   <span data-ttu-id="39c07-258">Eine Textur</span><span class="sxs-lookup"><span data-stu-id="39c07-258">A texture</span></span>
-   <span data-ttu-id="39c07-259">Ein Sampler (mit dem samplerzustand)</span><span class="sxs-lookup"><span data-stu-id="39c07-259">A sampler (with sampler state)</span></span>
-   <span data-ttu-id="39c07-260">Eine Samplings-Anweisung</span><span class="sxs-lookup"><span data-stu-id="39c07-260">A sampling instruction</span></span>

<span data-ttu-id="39c07-261">Samplers können mit Texturen und dem samplerzustand initialisiert werden, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="39c07-261">Samplers can be initialized with textures and sampler state as shown here:</span></span>


```
sampler s = sampler_state 
{ 
  texture = NULL; 
  mipfilter = LINEAR; 
};
```



<span data-ttu-id="39c07-262">Im folgenden finden Sie ein Beispiel für den Code für die Stichprobenentnahme einer 2D-Textur:</span><span class="sxs-lookup"><span data-stu-id="39c07-262">Here's an example of the code to sample a 2D texture:</span></span>


```
texture tex0;
sampler2D s_2D;

float2 sample_2D(float2 tex : TEXCOORD0) : COLOR
{
  return tex2D(s_2D, tex);
}
```



<span data-ttu-id="39c07-263">Die Textur wird mit einer Textur Variablen tex0 deklariert.</span><span class="sxs-lookup"><span data-stu-id="39c07-263">The texture is declared with a texture variable tex0.</span></span>

<span data-ttu-id="39c07-264">In diesem Beispiel wird eine samplervariable mit dem Namen s \_ 2D deklariert.</span><span class="sxs-lookup"><span data-stu-id="39c07-264">In this example, a sampler variable named s\_2D is declared.</span></span> <span data-ttu-id="39c07-265">Der Sampler enthält den samplerstatus in geschweiften Klammern.</span><span class="sxs-lookup"><span data-stu-id="39c07-265">The sampler contains the sampler state inside of curly braces.</span></span> <span data-ttu-id="39c07-266">Dies schließt die Textur ein, die als Stichprobe verwendet wird, und optional den Filter Zustand (d. h. Umbruch Modi, Filtermodi usw.).</span><span class="sxs-lookup"><span data-stu-id="39c07-266">This includes the texture that will be sampled and, optionally, the filter state (that is, wrap modes, filter modes, etc.).</span></span> <span data-ttu-id="39c07-267">Wenn der samplerzustand weggelassen wird, wird ein Standard-samplerstatus angewendet, der lineare Filterung und einen Umbruch Modus für die Texturkoordinaten angibt.</span><span class="sxs-lookup"><span data-stu-id="39c07-267">If the sampler state is omitted, a default sampler state is applied specifying linear filtering and a wrap mode for the texture coordinates.</span></span> <span data-ttu-id="39c07-268">Die samplingfunktion nimmt eine Gleit Komma-Textur Koordinate mit zwei Komponenten an und gibt eine Farbe mit zwei Komponenten zurück.</span><span class="sxs-lookup"><span data-stu-id="39c07-268">The sampler function takes a two-component floating-point texture coordinate, and returns a two-component color.</span></span> <span data-ttu-id="39c07-269">Dies wird durch den float2-Rückgabetyp dargestellt und stellt Daten in den roten und grünen Komponenten dar.</span><span class="sxs-lookup"><span data-stu-id="39c07-269">This is represented with the float2 return type and represents data in the red and green components.</span></span>

<span data-ttu-id="39c07-270">Es sind vier Typen von Samplern definiert (siehe [Schlüsselwörter](dx-graphics-hlsl-appendix.md)), und Textur Suchvorgänge werden von den intrinsischen Funktionen durchgeführt: [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**tex3D (s, t) (DirectX HLSL**](dx-graphics-hlsl-tex3d.md)), [**Texcube (s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md).</span><span class="sxs-lookup"><span data-stu-id="39c07-270">Four types of samplers are defined (see [Keywords](dx-graphics-hlsl-appendix.md)) and texture lookups are performed by the intrinsic functions: [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**tex3D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE(s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md).</span></span> <span data-ttu-id="39c07-271">Hier ist ein Beispiel für die 3D-Stichprobenentnahme:</span><span class="sxs-lookup"><span data-stu-id="39c07-271">Here is an example of 3D sampling:</span></span>


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



<span data-ttu-id="39c07-272">Diese samplerdeklaration verwendet den Standard samplerstatus für die Filtereinstellungen und den Adress Modus.</span><span class="sxs-lookup"><span data-stu-id="39c07-272">This sampler declaration uses default sampler state for the filter settings and address mode.</span></span>

<span data-ttu-id="39c07-273">Hier sehen Sie das entsprechende Beispiel für eine Beispiel-Stichprobe</span><span class="sxs-lookup"><span data-stu-id="39c07-273">Here is the corresponding cube sampling example:</span></span>


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



<span data-ttu-id="39c07-274">Und zum Schluss ist das Beispiel für die 1D-Stichprobenentnahme:</span><span class="sxs-lookup"><span data-stu-id="39c07-274">And finally, here is the 1D sampling example:</span></span>


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



<span data-ttu-id="39c07-275">Da die Common Language Runtime keine 1D-Texturen unterstützt, verwendet der Compiler eine 2D-Textur mit dem wissen, dass die y-Koordinate unwichtig ist.</span><span class="sxs-lookup"><span data-stu-id="39c07-275">Because the runtime does not support 1D textures, the compiler will use a 2D texture with the knowledge that the y-coordinate is unimportant.</span></span> <span data-ttu-id="39c07-276">Da [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) als 2D-Textur Suche implementiert ist, kann der Compiler die y-Komponente auf effiziente Weise auswählen.</span><span class="sxs-lookup"><span data-stu-id="39c07-276">Since [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) is implemented as a 2D texture lookup, the compiler is free to choose the y-component in an efficient manner.</span></span> <span data-ttu-id="39c07-277">In einigen seltenen Szenarios kann der Compiler keine effiziente y-Komponente auswählen. in diesem Fall wird eine Warnung ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="39c07-277">In some rare scenarios, the compiler cannot choose an efficient y-component, in which case it will issue a warning.</span></span>


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



<span data-ttu-id="39c07-278">Dieses spezielle Beispiel ist ineffizient, da der Compiler die eingabekoordinate in ein anderes Register verschieben muss (da eine 1D-Suche als 2D-Suche implementiert wird und die Textur Koordinate als float1 deklariert wird).</span><span class="sxs-lookup"><span data-stu-id="39c07-278">This particular example is inefficient because the compiler must move the input coordinate into another register (because a 1D lookup is implemented as a 2D lookup and the texture coordinate is declared as a float1).</span></span> <span data-ttu-id="39c07-279">Wenn der Code mit einer float2-Eingabe anstelle eines float1 umgeschrieben wird, kann der Compiler die Eingabe Textur Koordinate verwenden, da er weiß, dass y für etwas initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="39c07-279">If the code is rewritten using a float2 input instead of a float1, the compiler can use the input texture coordinate because it knows that y is initialized to something.</span></span>


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



<span data-ttu-id="39c07-280">Alle Textur Suchvorgänge können mit "Bias" oder "proj" angehängt werden (d. h. [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**texcubeproj (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)).</span><span class="sxs-lookup"><span data-stu-id="39c07-280">All texture lookups can be appended with "bias" or "proj" (that is, [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**texCUBEproj (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)).</span></span> <span data-ttu-id="39c07-281">Mit dem Suffix "proj" wird die Textur Koordinate durch die w-Komponente dividiert.</span><span class="sxs-lookup"><span data-stu-id="39c07-281">With the "proj" suffix, the texture coordinate is divided by the w-component.</span></span> <span data-ttu-id="39c07-282">Bei "Bias" wird die MIP-Ebene von der w-Komponente verlagert.</span><span class="sxs-lookup"><span data-stu-id="39c07-282">With "bias," the mip level is shifted by the w-component.</span></span> <span data-ttu-id="39c07-283">Folglich nehmen alle Textur Suchvorgänge mit einem Suffix immer eine float4-Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="39c07-283">Thus, all texture lookups with a suffix always take a float4 input.</span></span> <span data-ttu-id="39c07-284">[**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) und [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignorieren die YZ-und z-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="39c07-284">[**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) and [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignore the yz- and z-components respectively.</span></span>

<span data-ttu-id="39c07-285">Samplers können auch im Array verwendet werden, obwohl das Back-End derzeit keinen Zugriff auf das dynamische Array von Samplern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39c07-285">Samplers may also be used in array, although no back end currently supports dynamic array access of samplers.</span></span> <span data-ttu-id="39c07-286">Daher ist Folgendes gültig, da es zum Zeitpunkt der Kompilierung aufgelöst werden kann:</span><span class="sxs-lookup"><span data-stu-id="39c07-286">Therefore, the following is valid because it can be resolved at compile time:</span></span>


```
tex2D(s[0],tex)
```



<span data-ttu-id="39c07-287">Dieses Beispiel ist jedoch nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="39c07-287">However, this example is not valid.</span></span>


```
tex2D(s[a],tex)
```



<span data-ttu-id="39c07-288">Der dynamische Zugriff von Samplern ist hauptsächlich zum Schreiben von Programmen mit literalschleifen nützlich.</span><span class="sxs-lookup"><span data-stu-id="39c07-288">Dynamic access of samplers is primarily useful for writing programs with literal loops.</span></span> <span data-ttu-id="39c07-289">Der folgende Code veranschaulicht den Zugriff auf samplerarrays:</span><span class="sxs-lookup"><span data-stu-id="39c07-289">The following code illustrates sampler array accessing:</span></span>


```
sampler sm[4];

float4 main(float4 tex[4] : TEXCOORD) : COLOR
{
    float4 retColor = 1;

    for(int i = 0; i < 4;i++)
    {
        retColor *= tex2D(sm[i],tex[i]);
    }

    return retColor;
}
```



> [!Note]
>
> <span data-ttu-id="39c07-290">Die Verwendung der Microsoft Direct3D Debug-Laufzeit kann Ihnen helfen, Konflikte zwischen der Anzahl der Komponenten in einer Textur und einem Sampler abzufangen.</span><span class="sxs-lookup"><span data-stu-id="39c07-290">Using the Microsoft Direct3D debug runtime can help you catch mismatches between the number of components in a texture and a sampler.</span></span>

 

## <a name="writing-functions"></a><span data-ttu-id="39c07-291">Schreiben von Funktionen</span><span class="sxs-lookup"><span data-stu-id="39c07-291">Writing Functions</span></span>

<span data-ttu-id="39c07-292">Funktionen unterbrechen große Aufgaben in kleinere.</span><span class="sxs-lookup"><span data-stu-id="39c07-292">Functions break large tasks into smaller ones.</span></span> <span data-ttu-id="39c07-293">Kleine Aufgaben sind einfacher zu Debuggen und können wieder verwendet werden, sobald Sie sich bewährt haben.</span><span class="sxs-lookup"><span data-stu-id="39c07-293">Small tasks are easier to debug and can be reused, once proven.</span></span> <span data-ttu-id="39c07-294">Funktionen können verwendet werden, um Details anderer Funktionen auszublenden, wodurch ein Programm, das aus Funktionen besteht, einfacher zu befolgen ist.</span><span class="sxs-lookup"><span data-stu-id="39c07-294">Functions can be used to hide details of other functions, which makes a program composed of functions easier to follow.</span></span>

<span data-ttu-id="39c07-295">HLSL-Funktionen ähneln C-Funktionen auf verschiedene Weise: beide enthalten eine Definition und einen Funktions Text und deklarieren sowohl Rückgabe Typen als auch Argumentlisten.</span><span class="sxs-lookup"><span data-stu-id="39c07-295">HLSL functions are similar to C functions in several ways: They both contain a definition and a function body and they both declare return types and argument lists.</span></span> <span data-ttu-id="39c07-296">Wie bei C-Funktionen führt die HLSL-Validierung bei der Shader-Kompilierung eine Typüberprüfung für die Argumente, die Argument Typen und den Rückgabewert durch.</span><span class="sxs-lookup"><span data-stu-id="39c07-296">Like C functions, HLSL validation does type checking on the arguments, argument types, and the return value during shader compilation.</span></span>

<span data-ttu-id="39c07-297">Im Gegensatz zu C-Funktionen verwenden HLSL-Einstiegspunkt Funktionen Semantik, um Funktionsargumente an Shader-Eingaben und-Ausgaben zu binden (HLSL-Funktionen, die intern die Semantik ignorieren).</span><span class="sxs-lookup"><span data-stu-id="39c07-297">Unlike C functions, HLSL entry point functions use semantics to bind function arguments to shader inputs and outputs (HLSL functions called internally ignore semantics).</span></span> <span data-ttu-id="39c07-298">Dies vereinfacht das Binden von Puffer Daten an einen Shader und das Binden von shaderausgaben an shadereingaben.</span><span class="sxs-lookup"><span data-stu-id="39c07-298">This makes it easier to bind buffer data to a shader, and bind shader outputs to shader inputs.</span></span>

<span data-ttu-id="39c07-299">Eine Funktion enthält eine Deklaration und einen Text, und die Deklaration muss dem Text vorangestellt sein.</span><span class="sxs-lookup"><span data-stu-id="39c07-299">A function contains a declaration and a body, and the declaration must precede the body.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



<span data-ttu-id="39c07-300">Die Funktionsdeklaration enthält alles, was vor den geschweiften Klammern liegt:</span><span class="sxs-lookup"><span data-stu-id="39c07-300">The function declaration includes everything in front of the curly braces:</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



<span data-ttu-id="39c07-301">Eine Funktionsdeklaration enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="39c07-301">A function declaration contains:</span></span>

-   <span data-ttu-id="39c07-302">Ein Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="39c07-302">A return type</span></span>
-   <span data-ttu-id="39c07-303">Ein Funktionsname</span><span class="sxs-lookup"><span data-stu-id="39c07-303">A function name</span></span>
-   <span data-ttu-id="39c07-304">Eine Argumentliste (optional)</span><span class="sxs-lookup"><span data-stu-id="39c07-304">An argument list (optional)</span></span>
-   <span data-ttu-id="39c07-305">Eine Ausgabe Semantik (optional)</span><span class="sxs-lookup"><span data-stu-id="39c07-305">An output semantic (optional)</span></span>
-   <span data-ttu-id="39c07-306">Eine Anmerkung (optional)</span><span class="sxs-lookup"><span data-stu-id="39c07-306">An annotation (optional)</span></span>

<span data-ttu-id="39c07-307">Der Rückgabetyp kann jeder der HLSL-Grund Datentypen sein, z. b. ein float4:</span><span class="sxs-lookup"><span data-stu-id="39c07-307">The return type can be any of the HLSL basic data types such as a float4:</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
   ...
}
```



<span data-ttu-id="39c07-308">Der Rückgabetyp kann eine Struktur sein, die bereits definiert wurde:</span><span class="sxs-lookup"><span data-stu-id="39c07-308">The return type can be a structure that has already been defined:</span></span>


```
struct VS_OUTPUT
{
    float4  vPosition        : POSITION;
    float4  vDiffuse         : COLOR;
}; 

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



<span data-ttu-id="39c07-309">Wenn die Funktion keinen Wert zurückgibt, kann void als Rückgabetyp verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-309">If the function does not return a value, void can be used as the return type.</span></span>


```
void VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



<span data-ttu-id="39c07-310">Der Rückgabetyp wird immer zuerst in einer Funktionsdeklaration angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39c07-310">The return type always appears first in a function declaration.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



<span data-ttu-id="39c07-311">Eine Argumentliste deklariert die Eingabeargumente für eine Funktion.</span><span class="sxs-lookup"><span data-stu-id="39c07-311">An argument list declares the input arguments to a function.</span></span> <span data-ttu-id="39c07-312">Es können auch Werte deklariert werden, die zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-312">It may also declare values that will be returned.</span></span> <span data-ttu-id="39c07-313">Einige Argumente sind Eingabe-und Ausgabe Argumente.</span><span class="sxs-lookup"><span data-stu-id="39c07-313">Some arguments are both input and output arguments.</span></span> <span data-ttu-id="39c07-314">Im folgenden finden Sie ein Beispiel für einen Shader, der vier Eingabeargumente annimmt.</span><span class="sxs-lookup"><span data-stu-id="39c07-314">Here is an example of a shader that takes four input arguments.</span></span>


```
float4 Light(float3 LightDir : TEXCOORD1, 
             uniform float4 LightColor,  
             float2 texcrd : TEXCOORD0, 
             uniform sampler samp) : COLOR 
{
    float3 Normal = tex2D(samp,texcrd);

    return dot((Normal*2 - 1), LightDir)*LightColor;
}
```



<span data-ttu-id="39c07-315">Diese Funktion gibt eine endgültige Farbe zurück, bei der es sich um eine Mischung aus einem Textur Beispiel und der hellen Farbe handelt.</span><span class="sxs-lookup"><span data-stu-id="39c07-315">This function returns a final color, that is a blend of a texture sample and the light color.</span></span> <span data-ttu-id="39c07-316">Die Funktion nimmt vier Eingaben an.</span><span class="sxs-lookup"><span data-stu-id="39c07-316">The function takes four inputs.</span></span> <span data-ttu-id="39c07-317">Zwei Eingaben haben eine Semantik: lightdir weist die [TEXCOORD1](dx-graphics-hlsl-semantics.md) -Semantik auf, und texcrd hat die [TEXCOORD0](dx-graphics-hlsl-semantics.md) -Semantik.</span><span class="sxs-lookup"><span data-stu-id="39c07-317">Two inputs have semantics: LightDir has the [TEXCOORD1](dx-graphics-hlsl-semantics.md) semantic, and texcrd has the [TEXCOORD0](dx-graphics-hlsl-semantics.md) semantic.</span></span> <span data-ttu-id="39c07-318">Die Semantik bedeutet, dass die Daten für diese Variablen aus dem Vertex-Puffer stammen.</span><span class="sxs-lookup"><span data-stu-id="39c07-318">The semantics mean that the data for these variables will come from the vertex buffer.</span></span> <span data-ttu-id="39c07-319">Obwohl die lightdir-Variable über eine [TEXCOORD1](dx-graphics-hlsl-semantics.md) -Semantik verfügt, ist der-Parameter wahrscheinlich keine Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="39c07-319">Even though the LightDir variable has a [TEXCOORD1](dx-graphics-hlsl-semantics.md) semantic, the parameter is probably not a texture coordinate.</span></span> <span data-ttu-id="39c07-320">Der semantische Typ texcoordn wird häufig zum Bereitstellen einer Semantik für einen Typ verwendet, der nicht vordefiniert ist (es gibt keine Vertex-Shader-Eingabe Semantik für eine leichte Richtung).</span><span class="sxs-lookup"><span data-stu-id="39c07-320">The TEXCOORDn semantic type is often used to supply a semantic for a type that is not predefined (there is no vertex shader input semantic for a light direction).</span></span>

<span data-ttu-id="39c07-321">Die anderen beiden Eingaben LightColor und SAMP werden mit dem Schlüsselwort [Uniform](dx-graphics-hlsl-appendix.md) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="39c07-321">The other two inputs LightColor and samp are labeled with the [uniform](dx-graphics-hlsl-appendix.md) keyword.</span></span> <span data-ttu-id="39c07-322">Dabei handelt es sich um einheitliche Konstanten, die sich nicht zwischen zeichnen-aufrufen ändern.</span><span class="sxs-lookup"><span data-stu-id="39c07-322">These are uniform constants that will not change between draw calls.</span></span> <span data-ttu-id="39c07-323">Die Werte für diese Parameter stammen aus globalen Shader-Variablen.</span><span class="sxs-lookup"><span data-stu-id="39c07-323">The values for these parameters come from shader global variables.</span></span>

<span data-ttu-id="39c07-324">Argumente können mit dem in-Schlüsselwort als Eingaben gekennzeichnet werden, und es werden Ausgabe Argumente mit dem out-Schlüsselwort ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="39c07-324">Arguments can be labeled as inputs with the in keyword, and output arguments with the out keyword.</span></span> <span data-ttu-id="39c07-325">Argumente können nicht als Verweis übermittelt werden. ein Argument kann jedoch sowohl eine Eingabe als auch eine Ausgabe sein, wenn es mit dem INOUT-Schlüsselwort deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="39c07-325">Arguments cannot be passed by reference; however, an argument can be both an input and an output if it is declared with the inout keyword.</span></span> <span data-ttu-id="39c07-326">Argumente, die an eine Funktion übergebenen werden, die mit dem INOUT-Schlüsselwort gekennzeichnet sind, werden bis zur Rückgabe der Funktion als Kopien des Originals angesehen und zurückkopiert.</span><span class="sxs-lookup"><span data-stu-id="39c07-326">Arguments passed to a function that are marked with the inout keyword are considered copies of the original until the function returns, and they are copied back.</span></span> <span data-ttu-id="39c07-327">Hier ist ein Beispiel für die Verwendung von INOUT:</span><span class="sxs-lookup"><span data-stu-id="39c07-327">Here's an example using inout:</span></span>


```
void Increment_ByVal(inout float A, inout float B) 
{ 
    A++; B++;
}
```



<span data-ttu-id="39c07-328">Diese Funktion erhöht die Werte in A und B und gibt Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="39c07-328">This function increments the values in A and B and returns them.</span></span>

<span data-ttu-id="39c07-329">Der Funktions Rumpf ist der gesamte Code nach der Funktionsdeklaration.</span><span class="sxs-lookup"><span data-stu-id="39c07-329">The function body is all of the code after the function declaration.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



<span data-ttu-id="39c07-330">Der Text besteht aus Anweisungen, die von geschweiften Klammern eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-330">The body consists of statements which are surrounded by curly braces.</span></span> <span data-ttu-id="39c07-331">Der Funktions Rumpf implementiert die gesamte Funktionalität mithilfe von Variablen, Literalen, Ausdrücken und Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="39c07-331">The function body implements all of the functionality using variables, literals, expressions, and statements.</span></span>

<span data-ttu-id="39c07-332">Der Shader-Text hat zwei Dinge: er führt eine Matrix Multiplikation aus und gibt ein float4-Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="39c07-332">The shader body does two things: it performs a matrix multiply and returns a float4 result.</span></span> <span data-ttu-id="39c07-333">Die Matrix Multiplikation erfolgt mit der [**mul-Funktion (DirectX HLSL)**](dx-graphics-hlsl-mul.md) , die eine 4 x 4-Matrix Multiplikation durchführt.</span><span class="sxs-lookup"><span data-stu-id="39c07-333">The matrix multiply is accomplished with the [**mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) function, which performs a 4x4 matrix multiply.</span></span> <span data-ttu-id="39c07-334">**mul (DirectX HLSL)** wird als intrinsische Funktion bezeichnet, da Sie bereits in die HLSL-Bibliotheks Bibliothek integriert ist.</span><span class="sxs-lookup"><span data-stu-id="39c07-334">**mul (DirectX HLSL)** is called an intrinsic function because it is already built into the HLSL library of functions.</span></span> <span data-ttu-id="39c07-335">Intrinsische Funktionen werden im nächsten Abschnitt ausführlicher behandelt.</span><span class="sxs-lookup"><span data-stu-id="39c07-335">Intrinsic functions will be covered in more detail in the next section.</span></span>

<span data-ttu-id="39c07-336">Die Matrix Multiplikation kombiniert eine Eingabe Vektor-POS und eine zusammengesetzte Matrix worldviewproj.</span><span class="sxs-lookup"><span data-stu-id="39c07-336">The matrix multiply combines an input vector Pos and a composite matrix WorldViewProj.</span></span> <span data-ttu-id="39c07-337">Das Ergebnis sind Positionsdaten, die in den Bildschirmbereich transformiert werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-337">The result is position data transformed into screen space.</span></span> <span data-ttu-id="39c07-338">Dies ist die minimale Vertex-Shader-Verarbeitung, die wir durchführen können.</span><span class="sxs-lookup"><span data-stu-id="39c07-338">This is the minimum vertex shader processing we can do.</span></span> <span data-ttu-id="39c07-339">Wenn wir anstelle eines Scheitelpunkt-Shaders die Pipeline mit fester Funktionsweise verwenden, können die Scheitelpunkt Daten nach dieser Transformation gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-339">If we were using the fixed function pipeline instead of a vertex shader, the vertex data could be drawn after doing this transform.</span></span>

<span data-ttu-id="39c07-340">Die letzte Anweisung in einem Funktions Text ist eine Return-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="39c07-340">The last statement in a function body is a return statement.</span></span> <span data-ttu-id="39c07-341">Genau wie bei C gibt diese Anweisung die Steuerung von der-Funktion an die-Anweisung zurück, die die Funktion aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="39c07-341">Just like C, this statement returns control from the function to the statement that called the function.</span></span>

<span data-ttu-id="39c07-342">Funktions Rückgabe Typen können beliebige einfache Datentypen sein, die in HLSL definiert sind, einschließlich bool, int half, float und Double.</span><span class="sxs-lookup"><span data-stu-id="39c07-342">Function return types can be any of the simple data types defined in HLSL, including bool, int half, float, and double.</span></span> <span data-ttu-id="39c07-343">Rückgabe Typen können einer der komplexen Datentypen sein, z. b. Vektoren und Matrizen.</span><span class="sxs-lookup"><span data-stu-id="39c07-343">Return types can be one of the complex data types such as vectors and matrices.</span></span> <span data-ttu-id="39c07-344">HLSL-Typen, die auf-Objekte verweisen, können nicht als Rückgabe Typen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-344">HLSL types that refer to objects cannot be used as return types.</span></span> <span data-ttu-id="39c07-345">Dies schließt Pixelshader, Vertexshader, Texture und Sampler ein.</span><span class="sxs-lookup"><span data-stu-id="39c07-345">This includes pixelshader, vertexshader, texture, and sampler.</span></span>

<span data-ttu-id="39c07-346">Im folgenden finden Sie ein Beispiel für eine Funktion, die eine-Struktur für einen Rückgabetyp verwendet.</span><span class="sxs-lookup"><span data-stu-id="39c07-346">Here is an example of a function that uses a structure for a return type.</span></span>


```
float4x4 WorldViewProj : WORLDVIEWPROJ;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VS_HLL_Example(float4 inPos : POSITION )
{
    VS_OUTPUT Out;

    Out.Pos = mul(inPos,  WorldViewProj );

    return Out;
};
```



<span data-ttu-id="39c07-347">Der float4-Rückgabetyp wurde durch die Struktur vs \_ Output ersetzt, die jetzt einen einzelnen float4-Member enthält.</span><span class="sxs-lookup"><span data-stu-id="39c07-347">The float4 return type has been replaced with the structure VS\_OUTPUT, which now contains a single float4 member.</span></span>

<span data-ttu-id="39c07-348">Eine Return-Anweisung signalisiert das Ende einer Funktion.</span><span class="sxs-lookup"><span data-stu-id="39c07-348">A return statement signals the end of a function.</span></span> <span data-ttu-id="39c07-349">Dies ist die einfachste Return-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="39c07-349">This is the simplest return statement.</span></span> <span data-ttu-id="39c07-350">Sie gibt die Steuerung von der Funktion an das aufrufenden Programm zurück.</span><span class="sxs-lookup"><span data-stu-id="39c07-350">It returns control from the function to the calling program.</span></span> <span data-ttu-id="39c07-351">Es wird kein Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="39c07-351">It returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="39c07-352">Eine Return-Anweisung kann einen oder mehrere Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="39c07-352">A return statement can return one or more values.</span></span> <span data-ttu-id="39c07-353">In diesem Beispiel wird ein Literalwert zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="39c07-353">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="39c07-354">In diesem Beispiel wird das skalare Ergebnis eines Ausdrucks zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="39c07-354">This example returns the scalar result of an expression:</span></span>


```
return  light.enabled = true ;
```



<span data-ttu-id="39c07-355">Dieses Beispiel gibt eine float4 zurück, die aus einer lokalen Variablen und einem Literalwert erstellt wurde:</span><span class="sxs-lookup"><span data-stu-id="39c07-355">This example returns a float4 constructed from a local variable and a literal:</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="39c07-356">In diesem Beispiel wird ein float4-Wert zurückgegeben, der aus dem von einer intrinsischen Funktion zurückgegebenen Ergebnis und einigen Literalwerten erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="39c07-356">This example returns a float4 that is constructed from the result returned from an intrinsic function, and a few literal values:</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="39c07-357">Dieses Beispiel gibt eine-Struktur zurück, die mindestens ein-Element enthält:</span><span class="sxs-lookup"><span data-stu-id="39c07-357">This example returns a structure that contains one or more members:</span></span>


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="flow-control"></a><span data-ttu-id="39c07-358">Flusssteuerung</span><span class="sxs-lookup"><span data-stu-id="39c07-358">Flow Control</span></span>

<span data-ttu-id="39c07-359">Die meisten aktuellen Scheitelpunkt-und Pixel-Shader-Hardware ist darauf ausgelegt, einen Shader zeilenweise auszuführen und jede Anweisung einmal auszuführen.</span><span class="sxs-lookup"><span data-stu-id="39c07-359">Most current vertex and pixel shader hardware is designed to run a shader line by line, executing each instruction once.</span></span> <span data-ttu-id="39c07-360">HLSL unterstützt die Fluss Steuerung, einschließlich statischer Verzweigung, Prädikat Anweisungen, statischer Schleifen, dynamischer Verzweigungen und dynamischer Schleifen.</span><span class="sxs-lookup"><span data-stu-id="39c07-360">HLSL supports flow control, which includes static branching, predicated instructions, static looping, dynamic branching, and dynamic looping.</span></span>

<span data-ttu-id="39c07-361">Früher führte die Verwendung einer if-Anweisung zu einem assemblysprachshader-Code, der sowohl die if-Seite als auch die else-Seite des Code Flusses implementiert.</span><span class="sxs-lookup"><span data-stu-id="39c07-361">Previously, using an if statement resulted in assembly-language shader code that implements both the if side and the else side of the code flow.</span></span> <span data-ttu-id="39c07-362">Im folgenden finden Sie ein Beispiel für den in HLSL-Code, der für vs \_ 1 1 kompiliert wurde \_ :</span><span class="sxs-lookup"><span data-stu-id="39c07-362">Here is an example of the in HLSL code that was compiled for vs\_1\_1:</span></span>


```
if (Value > 0)
    oPos = Value1; 
else
    oPos = Value2; 
```



<span data-ttu-id="39c07-363">Und hier ist der resultierende Assemblycode:</span><span class="sxs-lookup"><span data-stu-id="39c07-363">And here is the resulting assembly code:</span></span>


```
// Calculate linear interpolation value in r0.w
mov r1.w, c2.x               
slt r0.w, c3.x, r1.w         
// Linear interpolation between value1 and value2
mov r7, -c1                      
add r2, r7, c0                   
mad oPos, r0.w, r2, c1  
```



<span data-ttu-id="39c07-364">Einige Hardware ermöglicht entweder statische oder dynamische Schleifen, aber die meisten erfordern eine lineare Ausführung.</span><span class="sxs-lookup"><span data-stu-id="39c07-364">Some hardware allows for either static or dynamic looping, but most require linear execution.</span></span> <span data-ttu-id="39c07-365">Bei den Modellen, die keine Schleifen unterstützen, muss für alle Schleifen ein Rollback ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-365">On the models that do not support looping, all loops must be unrolled.</span></span> <span data-ttu-id="39c07-366">Ein Beispiel hierfür ist das Beispiel " [DepthOfField Sample](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) ", in dem auch für PS \_ 1 1-Shader nicht rollende Schleifen verwendet werden \_ .</span><span class="sxs-lookup"><span data-stu-id="39c07-366">An example is the [DepthOfField Sample](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) sample that uses unrolled loops even for ps\_1\_1 shaders.</span></span>

<span data-ttu-id="39c07-367">HLSL bietet jetzt Unterstützung für die einzelnen Arten der Fluss Steuerung:</span><span class="sxs-lookup"><span data-stu-id="39c07-367">HLSL now includes support for each of these types of flow control:</span></span>

-   <span data-ttu-id="39c07-368">statische Verzweigung</span><span class="sxs-lookup"><span data-stu-id="39c07-368">static branching</span></span>
-   <span data-ttu-id="39c07-369">Prädikat Anweisungen</span><span class="sxs-lookup"><span data-stu-id="39c07-369">predicated instructions</span></span>
-   <span data-ttu-id="39c07-370">statische Schleifen</span><span class="sxs-lookup"><span data-stu-id="39c07-370">static looping</span></span>
-   <span data-ttu-id="39c07-371">dynamische Verzweigungen</span><span class="sxs-lookup"><span data-stu-id="39c07-371">dynamic branching</span></span>
-   <span data-ttu-id="39c07-372">dynamische Schleifen</span><span class="sxs-lookup"><span data-stu-id="39c07-372">dynamic looping</span></span>

<span data-ttu-id="39c07-373">Bei der statischen Verzweigung können Blöcke von shadercode basierend auf einer booleschen Shader-Konstante ein-oder ausgeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="39c07-373">Static branching allows blocks of shader code to be switched on or off based on a Boolean shader constant.</span></span> <span data-ttu-id="39c07-374">Dies ist eine bequeme Methode zum Aktivieren oder Deaktivieren von Codepfade basierend auf dem Typ des Objekts, das gerade gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="39c07-374">This is a convenient method for enabling or disabling code paths based on the type of object currently being rendered.</span></span> <span data-ttu-id="39c07-375">Zwischen zeichnen-aufrufen können Sie entscheiden, welche Features Sie mit dem aktuellen Shader unterstützen möchten, und dann die booleschen Flags festlegen, die zum Erreichen dieses Verhaltens erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="39c07-375">Between draw calls, you can decide which features you want to support with the current shader and then set the Boolean flags required to get that behavior.</span></span> <span data-ttu-id="39c07-376">Alle-Anweisungen, die von einer booleschen Konstante deaktiviert werden, werden während der shaderausführung übersprungen.</span><span class="sxs-lookup"><span data-stu-id="39c07-376">Any statements that are disabled by a Boolean constant are skipped during shader execution.</span></span>

<span data-ttu-id="39c07-377">Die vertraulichste Verzweigungs Unterstützung ist die dynamische Verzweigung.</span><span class="sxs-lookup"><span data-stu-id="39c07-377">The most familiar branching support is dynamic branching.</span></span> <span data-ttu-id="39c07-378">Bei der dynamischen Verzweigung befindet sich die Vergleichs Bedingung in einer Variablen. Dies bedeutet, dass der Vergleich für jeden Scheitelpunkt oder jedes Pixel zur Laufzeit erfolgt (im Gegensatz zum Vergleich, der zur Kompilierzeit oder zwischen zwei zeichnen-aufrufen auftritt).</span><span class="sxs-lookup"><span data-stu-id="39c07-378">With dynamic branching, the comparison condition resides in a variable, which means that the comparison is done for each vertex or each pixel at run time (as opposed to the comparison occurring at compile time, or between two draw calls).</span></span> <span data-ttu-id="39c07-379">Die Leistungseinbußen sind die Kosten der Verzweigung zuzüglich der Kosten für die Anweisungen auf der Seite der Verzweigung.</span><span class="sxs-lookup"><span data-stu-id="39c07-379">The performance hit is the cost of the branch plus the cost of the instructions on the side of the branch taken.</span></span> <span data-ttu-id="39c07-380">Dynamische Verzweigungen werden in Shader-Modell 3 oder höher implementiert.</span><span class="sxs-lookup"><span data-stu-id="39c07-380">Dynamic branching is implemented in shader model 3 or higher.</span></span> <span data-ttu-id="39c07-381">Die Optimierung von Shadern, die mit diesen Modellen funktionieren, ähnelt der Optimierung von Code, der auf einer CPU ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39c07-381">Optimizing shaders that work with these models is similar to optimizing code that runs on a CPU.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39c07-382">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39c07-382">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39c07-383">Programmieranleitung für HLSL</span><span class="sxs-lookup"><span data-stu-id="39c07-383">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 