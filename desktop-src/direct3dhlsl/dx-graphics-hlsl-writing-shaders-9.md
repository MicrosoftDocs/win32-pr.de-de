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
ms.openlocfilehash: 64a64d08518cb987850c87da3fb19c264519a7f7
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335384"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a><span data-ttu-id="e1867-103">Schreiben von HLSL-Shadern in Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="e1867-103">Writing HLSL Shaders in Direct3D 9</span></span>

-   [<span data-ttu-id="e1867-104">Vertex-Shader– Grundlagen</span><span class="sxs-lookup"><span data-stu-id="e1867-104">Vertex-Shader Basics</span></span>](#vertex-shader-basics)
-   [<span data-ttu-id="e1867-105">Pixel-Shader– Grundlagen</span><span class="sxs-lookup"><span data-stu-id="e1867-105">Pixel-Shader Basics</span></span>](#pixel-shader-basics)
    -   [<span data-ttu-id="e1867-106">Texturphase und Samplerzustände</span><span class="sxs-lookup"><span data-stu-id="e1867-106">Texture Stage and Sampler States</span></span>](#texture-stage-and-sampler-states)
    -   [<span data-ttu-id="e1867-107">Pixel-Shadereingaben</span><span class="sxs-lookup"><span data-stu-id="e1867-107">Pixel Shader Inputs</span></span>](#pixel-shader-inputs)
    -   [<span data-ttu-id="e1867-108">Pixel-Shaderausgaben</span><span class="sxs-lookup"><span data-stu-id="e1867-108">Pixel Shader Outputs</span></span>](#pixel-shader-outputs)
-   [<span data-ttu-id="e1867-109">Shadereingaben und Shadervariablen</span><span class="sxs-lookup"><span data-stu-id="e1867-109">Shader Inputs and Shader Variables</span></span>](#shader-inputs-and-shader-variables)
    -   [<span data-ttu-id="e1867-110">Deklarieren von Shadervariablen</span><span class="sxs-lookup"><span data-stu-id="e1867-110">Declaring Shader Variables</span></span>](#declaring-shader-variables)
    -   [<span data-ttu-id="e1867-111">Uniform Shader-Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1867-111">Uniform Shader Inputs</span></span>](#uniform-shader-inputs)
    -   [<span data-ttu-id="e1867-112">Unterschiedliche Shadereingaben und -semantik</span><span class="sxs-lookup"><span data-stu-id="e1867-112">Varying Shader Inputs and Semantics</span></span>](#varying-shader-inputs-and-semantics)
    -   [<span data-ttu-id="e1867-113">Sampler und Texturobjekte</span><span class="sxs-lookup"><span data-stu-id="e1867-113">Samplers and Texture Objects</span></span>](#samplers-and-texture-objects)
-   [<span data-ttu-id="e1867-114">Schreiben von Funktionen</span><span class="sxs-lookup"><span data-stu-id="e1867-114">Writing Functions</span></span>](#writing-functions)
-   [<span data-ttu-id="e1867-115">Flusssteuerung</span><span class="sxs-lookup"><span data-stu-id="e1867-115">Flow Control</span></span>](#flow-control)
-   [<span data-ttu-id="e1867-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e1867-116">Related topics</span></span>](#related-topics)

## <a name="vertex-shader-basics"></a><span data-ttu-id="e1867-117">Vertex-Shader Grundlagen</span><span class="sxs-lookup"><span data-stu-id="e1867-117">Vertex-Shader Basics</span></span>

<span data-ttu-id="e1867-118">Wenn der Vorgang ausgeführt wird, ersetzt ein programmierbarer Vertex-Shader die Scheitelpunktverarbeitung, die von der Microsoft Direct3D-Grafikpipeline durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1867-118">When in operation, a programmable vertex shader replaces the vertex processing done by the Microsoft Direct3D graphics pipeline.</span></span> <span data-ttu-id="e1867-119">Bei Verwendung eines Vertex-Shaders werden Zustandsinformationen zu Transformations- und Beleuchtungsvorgängen von der festen Funktionspipeline ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e1867-119">While using a vertex shader, state information regarding transformation and lighting operations is ignored by the fixed function pipeline.</span></span> <span data-ttu-id="e1867-120">Wenn der Vertex-Shader deaktiviert ist und die Verarbeitung fester Funktionen zurückgegeben wird, gelten alle aktuellen Zustandseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="e1867-120">When the vertex shader is disabled and fixed function processing is returned, all current state settings apply.</span></span>

<span data-ttu-id="e1867-121">Das Mosaik von Primitiven hoher Ordnung sollte vor der Ausführung des Vertex-Shaders erfolgen.</span><span class="sxs-lookup"><span data-stu-id="e1867-121">Tessellation of high-order primitives should be done before the vertex shader executes.</span></span> <span data-ttu-id="e1867-122">Implementierungen, die nach der Shaderverarbeitung ein Oberflächen-Mosaik durchführen, müssen dies auf eine Weise tun, die für die Anwendung und den Shadercode nicht offensichtlich ist.</span><span class="sxs-lookup"><span data-stu-id="e1867-122">Implementations that perform surface tessellation after the shader processing must do so in a way that is not apparent to the application and shader code.</span></span>

<span data-ttu-id="e1867-123">Ein Vertex-Shader muss mindestens die Scheitelpunktposition im homogenen Clipbereich ausgeben.</span><span class="sxs-lookup"><span data-stu-id="e1867-123">As a minimum, a vertex shader must output vertex position in homogeneous clip space.</span></span> <span data-ttu-id="e1867-124">Optional kann der Vertex-Shader Texturkoordinaten, Scheitelpunktfarbe, Scheitelpunktbeleuchtung, Lichtfaktoren und so weiter ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="e1867-124">Optionally, the vertex shader can output texture coordinates, vertex color, vertex lighting, fog factors, and so on.</span></span>

## <a name="pixel-shader-basics"></a><span data-ttu-id="e1867-125">Pixel-Shader Grundlagen</span><span class="sxs-lookup"><span data-stu-id="e1867-125">Pixel-Shader Basics</span></span>

<span data-ttu-id="e1867-126">Die Pixelverarbeitung wird von Pixel-Shadern auf einzelnen Pixeln ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1867-126">Pixel processing is performed by pixel shaders on individual pixels.</span></span> <span data-ttu-id="e1867-127">Pixel-Shader arbeiten zusammen mit Vertex-Shadern. Die Ausgabe eines Vertex-Shaders stellt die Eingaben für einen Pixel-Shader zur Verwendung.</span><span class="sxs-lookup"><span data-stu-id="e1867-127">Pixel shaders work in concert with vertex shaders; the output of a vertex shader provides the inputs for a pixel shader.</span></span> <span data-ttu-id="e1867-128">Andere Pixeloperationen (Blending, Schablonenoperationen und Renderzielblending) erfolgen nach der Ausführung des Shaders.</span><span class="sxs-lookup"><span data-stu-id="e1867-128">Other pixel operations (fog blending, stencil operations, and render-target blending) occur after execution of the shader.</span></span>

### <a name="texture-stage-and-sampler-states"></a><span data-ttu-id="e1867-129">Texturstufe und Samplerzustände</span><span class="sxs-lookup"><span data-stu-id="e1867-129">Texture Stage and Sampler States</span></span>

<span data-ttu-id="e1867-130">Ein Pixel-Shader ersetzt die vom Multitexturblender angegebene Pixelblendingfunktion vollständig, einschließlich vorgängen, die zuvor durch die Texturstufenzustände definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="e1867-130">A pixel shader completely replaces the pixel-blending functionality specified by the multi-texture blender including operations previously defined by the texture stage states.</span></span> <span data-ttu-id="e1867-131">Textursstichproben- und Filtervorgänge, die von den Standardtexturstufenzuständen für Minierung, Vergrößerung, MIP-Filterung und die Wrap-Adressierungsmodi gesteuert wurden, können in Shadern initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-131">Texture sampling and filtering operations which were controlled by the standard texture stage states for minification, magnification, mip filtering, and the wrap addressing modes, can be initialized in shaders.</span></span> <span data-ttu-id="e1867-132">Die Anwendung kann diese Zustände ändern, ohne dass der aktuell gebundene Shader neu entiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="e1867-132">The application is free to change these states without requiring the regeneration of the currently bound shader.</span></span> <span data-ttu-id="e1867-133">Das Festlegen des Zustands kann noch einfacher werden, wenn Ihre Shader innerhalb eines Effekts entworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="e1867-133">Setting state can be made even easier if your shaders are designed within an effect.</span></span>

### <a name="pixel-shader-inputs"></a><span data-ttu-id="e1867-134">Pixel-Shadereingaben</span><span class="sxs-lookup"><span data-stu-id="e1867-134">Pixel Shader Inputs</span></span>

<span data-ttu-id="e1867-135">Für die Pixel-Shaderversionen ps \_ 1 1 - ps 2 0 werden diffuse und specular-Farben im Bereich von 0 bis 1 überschniffen (klammert), bevor sie vom \_ \_ \_ Shader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-135">For pixel shader versions ps\_1\_1 - ps\_2\_0, diffuse and specular colors are saturated (clamped) in the range 0 to 1 before use by the shader.</span></span>

<span data-ttu-id="e1867-136">Für die Eingabe von Farbwerten für den Pixel-Shader wird angenommen, dass sie perspektivisch korrekt sind, aber dies ist (für alle Hardware) nicht garantiert.</span><span class="sxs-lookup"><span data-stu-id="e1867-136">Color values input to the pixel shader are assumed to be perspective correct, but this is not guaranteed (for all hardware).</span></span> <span data-ttu-id="e1867-137">Farben, die aus Texturkoordinaten entnommen werden, werden perspektivisch korrekt durchgeitert und während der Iteration an den Bereich 0 bis 1 geklammert.</span><span class="sxs-lookup"><span data-stu-id="e1867-137">Colors sampled from texture coordinates are iterated in a perspective correct manner, and are clamped to the 0 to 1 range during iteration.</span></span>

### <a name="pixel-shader-outputs"></a><span data-ttu-id="e1867-138">Pixel-Shader-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1867-138">Pixel Shader Outputs</span></span>

<span data-ttu-id="e1867-139">Für die Pixel-Shaderversionen ps 1 1 - ps 1 4 entspricht das vom Pixel-Shader ausgegebene Ergebnis dem Inhalt \_ \_ des \_ \_ Registers r0.</span><span class="sxs-lookup"><span data-stu-id="e1867-139">For pixel shader versions ps\_1\_1 - ps\_1\_4, the result emitted by the pixel shader is the contents of register r0.</span></span> <span data-ttu-id="e1867-140">Alles, was sie enthält, wenn der Shader die Verarbeitung abgeschlossen hat, wird an die Phase und den Renderzielblender gesendet.</span><span class="sxs-lookup"><span data-stu-id="e1867-140">Whatever it contains when the shader completes processing is sent to the fog stage and render-target blender.</span></span>

<span data-ttu-id="e1867-141">Bei Pixel-Shaderversionen ps 2 0 und höher wird die Ausgabefarbe von \_ \_ oC0 - oC4 ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="e1867-141">For pixel shader versions ps\_2\_0 and above, output color is emitted from oC0 - oC4.</span></span>

## <a name="shader-inputs-and-shader-variables"></a><span data-ttu-id="e1867-142">Shadereingaben und Shadervariablen</span><span class="sxs-lookup"><span data-stu-id="e1867-142">Shader Inputs and Shader Variables</span></span>

-   [<span data-ttu-id="e1867-143">Deklarieren von Shadervariablen</span><span class="sxs-lookup"><span data-stu-id="e1867-143">Declaring Shader Variables</span></span>](#declaring-shader-variables)
-   [<span data-ttu-id="e1867-144">Uniform Shader-Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1867-144">Uniform Shader Inputs</span></span>](#uniform-shader-inputs)
-   [<span data-ttu-id="e1867-145">Unterschiedliche Shadereingaben und -semantik</span><span class="sxs-lookup"><span data-stu-id="e1867-145">Varying Shader Inputs and Semantics</span></span>](#varying-shader-inputs-and-semantics)
-   [<span data-ttu-id="e1867-146">Sampler und Texturobjekte</span><span class="sxs-lookup"><span data-stu-id="e1867-146">Samplers and Texture Objects</span></span>](#samplers-and-texture-objects)

### <a name="declaring-shader-variables"></a><span data-ttu-id="e1867-147">Deklarieren von Shadervariablen</span><span class="sxs-lookup"><span data-stu-id="e1867-147">Declaring Shader Variables</span></span>

<span data-ttu-id="e1867-148">Die einfachste Variablendeklaration enthält einen Typ und einen Variablennamen, z. B. diese Gleitkommadeklaration:</span><span class="sxs-lookup"><span data-stu-id="e1867-148">The simplest variable declaration includes a type and a variable name, such as this floating-point declaration:</span></span>


```
float fVar;
```



<span data-ttu-id="e1867-149">Sie können eine Variable in derselben Anweisung initialisieren.</span><span class="sxs-lookup"><span data-stu-id="e1867-149">You can initialize a variable in the same statement.</span></span>


```
float fVar = 3.1f;
```



<span data-ttu-id="e1867-150">Ein Array von Variablen kann deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-150">An array of variables can be declared,</span></span>


```
int iVar[3];
```



<span data-ttu-id="e1867-151">oder in derselben Anweisung deklariert und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="e1867-151">or declared and initialized in the same statement.</span></span>


```
int iVar[3] = {1,2,3};
```



<span data-ttu-id="e1867-152">Hier sind einige Deklarationen, die viele der Merkmale von HLSL-Variablen (High-Level Shader Language) veranschaulichen:</span><span class="sxs-lookup"><span data-stu-id="e1867-152">Here are a few declarations that demonstrate many of the characteristics of high-level shader language (HLSL) variables:</span></span>


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



<span data-ttu-id="e1867-153">Datendeklarationen können einen beliebigen gültigen Typ verwenden, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="e1867-153">Data declarations can use any valid type including:</span></span>

-   [<span data-ttu-id="e1867-154">Datentypen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1867-154">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
-   [<span data-ttu-id="e1867-155">Vektortyp (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1867-155">Vector Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-vector.md)
-   [<span data-ttu-id="e1867-156">Matrixtyp (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1867-156">Matrix Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-matrix.md)
-   [<span data-ttu-id="e1867-157">Shadertyp (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1867-157">Shader Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-shader.md)
-   [<span data-ttu-id="e1867-158">Samplertyp (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1867-158">Sampler Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-sampler.md)
-   [<span data-ttu-id="e1867-159">Benutzerdefinierter Typ (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1867-159">User-Defined Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-user-defined.md)

<span data-ttu-id="e1867-160">Ein Shader kann Variablen, Argumente und Funktionen der obersten Ebene aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e1867-160">A shader can have top-level variables, arguments, and functions.</span></span>


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



<span data-ttu-id="e1867-161">Variablen der obersten Ebene werden außerhalb aller Funktionen deklariert.</span><span class="sxs-lookup"><span data-stu-id="e1867-161">Top-level variables are declared outside of all functions.</span></span> <span data-ttu-id="e1867-162">Argumente der obersten Ebene sind Parameter für eine Funktion der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="e1867-162">Top-level arguments are parameters to a top-level function.</span></span> <span data-ttu-id="e1867-163">Eine Funktion der obersten Ebene ist jede Funktion, die von der Anwendung aufgerufen wird (im Gegensatz zu einer Funktion, die von einer anderen Funktion aufgerufen wird).</span><span class="sxs-lookup"><span data-stu-id="e1867-163">A top-level function is any function called by the application (as opposed to a function that is called by another function).</span></span>

### <a name="uniform-shader-inputs"></a><span data-ttu-id="e1867-164">Uniform Shader Inputs</span><span class="sxs-lookup"><span data-stu-id="e1867-164">Uniform Shader Inputs</span></span>

<span data-ttu-id="e1867-165">Vertex- und Pixel-Shader akzeptieren zwei Arten von Eingabedaten: variierend und einheitlich.</span><span class="sxs-lookup"><span data-stu-id="e1867-165">Vertex and pixel shaders accept two kinds of input data: varying and uniform.</span></span> <span data-ttu-id="e1867-166">Die variierende Eingabe sind die Daten, die für jede Ausführung des Shaders eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="e1867-166">The varying input is the data that is unique to each execution of the shader.</span></span> <span data-ttu-id="e1867-167">Bei einem Vertex-Shader stammen die unterschiedlichen Daten (z. B. Position, Normal usw.) aus den Scheitelpunktstreams.</span><span class="sxs-lookup"><span data-stu-id="e1867-167">For a vertex shader, the varying data (for example: position, normal, etc.) comes from the vertex streams.</span></span> <span data-ttu-id="e1867-168">Die einheitlichen Daten (z. B. Materialfarbe, Welttransformation usw.) sind für mehrere Ausführungen eines Shaders konstant.</span><span class="sxs-lookup"><span data-stu-id="e1867-168">The uniform data (for example: material color, world transform, etc.) is constant for multiple executions of a shader.</span></span> <span data-ttu-id="e1867-169">Für Diejenigen, die mit den Shadermodellen der Assembly vertraut sind, werden einheitliche Daten durch konstante Register und unterschiedliche Daten durch die Register v und t angegeben.</span><span class="sxs-lookup"><span data-stu-id="e1867-169">For those familiar with the assembly shader models, uniform data is specified by constant registers and varying data by the v and t registers.</span></span>

<span data-ttu-id="e1867-170">Einheitliche Daten können mit zwei Methoden angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-170">Uniform data can be specified by two methods.</span></span> <span data-ttu-id="e1867-171">Die gängigste Methode ist das Deklarieren globaler Variablen und deren Verwendung innerhalb eines Shaders.</span><span class="sxs-lookup"><span data-stu-id="e1867-171">The most common method is to declare global variables and use them within a shader.</span></span> <span data-ttu-id="e1867-172">Jede Verwendung globaler Variablen innerhalb eines Shaders führt dazu, dass diese Variable der Liste der für diesen Shader erforderlichen einheitlichen Variablen hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e1867-172">Any use of global variables within a shader will result in adding that variable to the list of uniform variables required by that shader.</span></span> <span data-ttu-id="e1867-173">Die zweite Methode besteht im Markieren eines Eingabeparameters der Shaderfunktion der obersten Ebene als einheitlich.</span><span class="sxs-lookup"><span data-stu-id="e1867-173">The second method is to mark an input parameter of the top-level shader function as uniform.</span></span> <span data-ttu-id="e1867-174">Diese Kennzeichnung gibt an, dass die gegebene Variable der Liste der einheitlichen Variablen hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1867-174">This marking specifies that the given variable should be added to the list of uniform variables.</span></span>

<span data-ttu-id="e1867-175">Einheitliche Variablen, die von einem Shader verwendet werden, werden über die konstante Tabelle an die Anwendung zurück übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e1867-175">Uniform variables used by a shader are communicated back to the application via the constant table.</span></span> <span data-ttu-id="e1867-176">Die Konstantentabelle ist der Name der Symboltabelle, die definiert, wie die von einem Shader verwendeten Uniformvariablen in die Konstantenregister passen.</span><span class="sxs-lookup"><span data-stu-id="e1867-176">The constant table is the name for the symbol table that defines how the uniform variables used by a shader fit into the constant registers.</span></span> <span data-ttu-id="e1867-177">Die Parameter der einheitlichen Funktion werden im Gegensatz zu den globalen Variablen in der Konstantentabelle mit einem Dollarzeichen ($) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e1867-177">The uniform function parameters appear in the constant table prepended with a dollar sign ($), unlike the global variables.</span></span> <span data-ttu-id="e1867-178">Das Dollarzeichen ist erforderlich, um Namenskollisionen zwischen lokalen einheitlichen Eingaben und globalen Variablen mit demselben Namen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="e1867-178">The dollar sign is required to avoid name collisions between local uniform inputs and global variables of the same name.</span></span>

<span data-ttu-id="e1867-179">Die Konstantentabelle enthält die konstanten Registerpositionen aller vom Shader verwendeten einheitlichen Variablen.</span><span class="sxs-lookup"><span data-stu-id="e1867-179">The constant table contains the constant register locations of all uniform variables used by the shader.</span></span> <span data-ttu-id="e1867-180">Die Tabelle enthält auch die Typinformationen und den Standardwert, sofern angegeben.</span><span class="sxs-lookup"><span data-stu-id="e1867-180">The table also includes the type information and the default value, if specified.</span></span>

### <a name="varying-shader-inputs-and-semantics"></a><span data-ttu-id="e1867-181">Variierende Shadereingaben und Semantik</span><span class="sxs-lookup"><span data-stu-id="e1867-181">Varying Shader Inputs and Semantics</span></span>

<span data-ttu-id="e1867-182">Unterschiedliche Eingabeparameter (einer Shaderfunktion der obersten Ebene) müssen entweder mit einem semantischen oder einem uniform-Schlüsselwort gekennzeichnet werden, das angibt, dass der Wert für die Ausführung des Shaders konstant ist.</span><span class="sxs-lookup"><span data-stu-id="e1867-182">Varying input parameters (of a top-level shader function) must be marked either with a semantic or uniform keyword indicating the value is constant for the execution of the shader.</span></span> <span data-ttu-id="e1867-183">Wenn eine Shadereingabe der obersten Ebene nicht mit einem semantischen oder einheitlichen Schlüsselwort markiert ist, kann der Shader nicht kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-183">If a top-level shader input is not marked with a semantic or uniform keyword, then the shader will fail to compile.</span></span>

<span data-ttu-id="e1867-184">Die Eingabesemantik ist ein Name, der verwendet wird, um die gegebene Eingabe mit einer Ausgabe des vorherigen Teils der Grafikpipeline zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="e1867-184">The input semantic is a name used to link the given input to an output of the previous part of the graphics pipeline.</span></span> <span data-ttu-id="e1867-185">Beispielsweise wird die eingabesemantische POSITION0 von den Vertex-Shadern verwendet, um anzugeben, wo die Positionsdaten aus dem Scheitelpunktpuffer verknüpft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e1867-185">For example, the input semantic POSITION0 is used by the vertex shaders to specify where the position data from the vertex buffer should be linked.</span></span>

<span data-ttu-id="e1867-186">Pixels- und Vertex-Shader verfügen aufgrund der verschiedenen Teile der Grafikpipeline, die in die einzelnen Shadereinheiten eingeht, über unterschiedliche Sätze von Eingabesemantik.</span><span class="sxs-lookup"><span data-stu-id="e1867-186">Pixel and vertex shaders have different sets of input semantics due to the different parts of the graphics pipeline that feed into each shader unit.</span></span> <span data-ttu-id="e1867-187">Die Vertex-Shader-Eingabesemantik beschreibt die Pro-Scheitelpunkt-Informationen (z.B. Position, Normal, Texturkoordinaten, Farbe, Tangens, Binormal usw.), die aus einem Scheitelpunktpuffer in ein Formular geladen werden sollen, das vom Vertex-Shader genutzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e1867-187">Vertex shader input semantics describe the per-vertex information (for example: position, normal, texture coordinates, color, tangent, binormal, etc.) to be loaded from a vertex buffer into a form that can be consumed by the vertex shader.</span></span> <span data-ttu-id="e1867-188">Die Eingabesemantik ist direkt der Verwendung der Scheitelpunktdeklaration und dem Verwendungsindex zu zuordnen.</span><span class="sxs-lookup"><span data-stu-id="e1867-188">The input semantics directly map to the vertex declaration usage and the usage index.</span></span>

<span data-ttu-id="e1867-189">Die Pixel-Shader-Eingabesemantik beschreibt die Informationen, die von der Rasterungseinheit pro Pixel bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-189">Pixel shader input semantics describe the information that is provided per pixel by the rasterization unit.</span></span> <span data-ttu-id="e1867-190">Die Daten werden generiert, indem zwischen ausgaben des Vertex-Shaders für jeden Scheitelpunkt des aktuellen Primitiven interpoliert wird.</span><span class="sxs-lookup"><span data-stu-id="e1867-190">The data is generated by interpolating between outputs of the vertex shader for each vertex of the current primitive.</span></span> <span data-ttu-id="e1867-191">Die grundlegende Pixel-Shader-Eingabesemantik verknüpfen die Ausgabefarbe und Texturkoordinateninformationen mit Eingabeparametern.</span><span class="sxs-lookup"><span data-stu-id="e1867-191">The basic pixel shader input semantics link the output color and texture coordinate information to input parameters.</span></span>

<span data-ttu-id="e1867-192">Die Eingabesemantik kann der Shadereingabe mit zwei Methoden zugewiesen werden:</span><span class="sxs-lookup"><span data-stu-id="e1867-192">Input semantics can be assigned to shader input by two methods:</span></span>

-   <span data-ttu-id="e1867-193">Anfügen eines Doppelpunkts und des semantischen Namens an die Parameterdeklaration.</span><span class="sxs-lookup"><span data-stu-id="e1867-193">Appending a colon and the semantic name to the parameter declaration.</span></span>
-   <span data-ttu-id="e1867-194">Definieren einer Eingabestruktur mit Eingabesemantik, die jedem Strukturmitglied zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e1867-194">Defining an input structure with input semantics assigned to each structure member.</span></span>

<span data-ttu-id="e1867-195">Vertex- und Pixel-Shader stellen Ausgabedaten für die nachfolgende Grafikpipelinephase zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e1867-195">Vertex and pixel shaders provide output data to the subsequent graphics pipeline stage.</span></span> <span data-ttu-id="e1867-196">Ausgabesemantik wird verwendet, um anzugeben, wie vom Shader generierte Daten mit den Eingaben der nächsten Phase verknüpft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e1867-196">Output semantics are used to specify how data generated by the shader should be linked to the inputs of the next stage.</span></span> <span data-ttu-id="e1867-197">Beispielsweise wird die Ausgabesemantik für einen Vertex-Shader verwendet, um die Ausgaben der Interpolatoren im Rasterizer zu verknüpfen, um die Eingabedaten für den Pixel-Shader zu generieren.</span><span class="sxs-lookup"><span data-stu-id="e1867-197">For example, the output semantics for a vertex shader are used to link the outputs of the interpolators in the rasterizer to generate the input data for the pixel shader.</span></span> <span data-ttu-id="e1867-198">Bei den Pixel-Shader-Ausgaben handelt es sich um die Werte, die der Alphablendingeinheit für jedes der Renderziele bereitgestellt werden, oder um den Tiefenwert, der in den Tiefenpuffer geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="e1867-198">The pixel shader outputs are the values provided to the alpha blending unit for each of the render targets or the depth value written to the depth buffer.</span></span>

<span data-ttu-id="e1867-199">Die Vertex-Shader-Ausgabesemantik wird verwendet, um den Shader sowohl mit dem Pixel-Shader als auch mit der Rasterizer-Stufe zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="e1867-199">Vertex shader output semantics are used to link the shader both to the pixel shader and to the rasterizer stage.</span></span> <span data-ttu-id="e1867-200">Ein Vertex-Shader, der vom Rasterizer genutzt und nicht für den Pixelshader verfügbar gemacht wird, muss mindestens Positionsdaten generieren.</span><span class="sxs-lookup"><span data-stu-id="e1867-200">A vertex shader that is consumed by the rasterizer and not exposed to the pixel shader must generate position data as a minimum.</span></span> <span data-ttu-id="e1867-201">Vertex-Shader, die Texturkoordinaten- und Farbdaten generieren, stellen diese Daten nach Abschluss der Interpolation an einen Pixel-Shader bereit.</span><span class="sxs-lookup"><span data-stu-id="e1867-201">Vertex shaders that generate texture coordinate and color data provide that data to a pixel shader after interpolation is done.</span></span>

<span data-ttu-id="e1867-202">Die Ausgabesemantik des Pixelshaders bindet die Ausgabefarben eines Pixelshaders an das richtige Renderziel.</span><span class="sxs-lookup"><span data-stu-id="e1867-202">Pixel shader output semantics bind the output colors of a pixel shader with the correct render target.</span></span> <span data-ttu-id="e1867-203">Die Ausgabefarbe des Pixelshaders ist mit der Alphablendphase verknüpft, die bestimmt, wie die Zielrenderziele geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-203">The pixel shader output color is linked to the alpha blend stage, which determines how the destination render targets are modified.</span></span> <span data-ttu-id="e1867-204">Die Pixel-Shader-Tiefenausgabe kann verwendet werden, um die Zieltiefewerte an der aktuellen Rasterposition zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e1867-204">The pixel shader depth output can be used to change the destination depth values at the current raster location.</span></span> <span data-ttu-id="e1867-205">Die Tiefenausgabe und mehrere Renderziele werden nur bei einigen Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1867-205">The depth output and multiple render targets are only supported with some shader models.</span></span>

<span data-ttu-id="e1867-206">Die Syntax für die Ausgabesemantik ist identisch mit der Syntax zum Angeben der Eingabesemantik.</span><span class="sxs-lookup"><span data-stu-id="e1867-206">The syntax for output semantics is identical to the syntax for specifying input semantics.</span></span> <span data-ttu-id="e1867-207">Die Semantik kann entweder direkt für Parameter angegeben werden, die als "out"-Parameter deklariert sind, oder während der Definition einer Struktur zugewiesen werden, die entweder als "out"-Parameter oder als Rückgabewert einer Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e1867-207">The semantics can be either specified directly on parameters declared as "out" parameters or assigned during the definition of a structure that either returned as an "out" parameter or the return value of a function.</span></span>

<span data-ttu-id="e1867-208">Semantik identifiziert, woher Daten stammen.</span><span class="sxs-lookup"><span data-stu-id="e1867-208">Semantics identify where data comes from.</span></span> <span data-ttu-id="e1867-209">Semantik sind optionale Bezeichner, die Shadereingaben und -ausgaben identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e1867-209">Semantics are optional identifiers that identify shader inputs and outputs.</span></span> <span data-ttu-id="e1867-210">Semantik wird an einer von drei Stellen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="e1867-210">Semantics appear in one of three places:</span></span>

-   <span data-ttu-id="e1867-211">Nach einem Strukturmember.</span><span class="sxs-lookup"><span data-stu-id="e1867-211">After a structure member.</span></span>
-   <span data-ttu-id="e1867-212">Nach einem Argument in der Eingabeargumentliste einer Funktion.</span><span class="sxs-lookup"><span data-stu-id="e1867-212">After an argument in a function's input argument list.</span></span>
-   <span data-ttu-id="e1867-213">Nach der Eingabeargumentliste der Funktion.</span><span class="sxs-lookup"><span data-stu-id="e1867-213">After the function's input argument list.</span></span>

<span data-ttu-id="e1867-214">In diesem Beispiel wird eine -Struktur verwendet, um eine oder mehrere Vertex-Shadereingaben bereitzustellen, und eine andere -Struktur, um eine oder mehrere Vertex-Shaderausgaben bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e1867-214">This example uses a structure to provide one or more vertex shader inputs, and another structure to provide one or more vertex shader outputs.</span></span> <span data-ttu-id="e1867-215">Jeder der Strukturmember verwendet eine Semantik.</span><span class="sxs-lookup"><span data-stu-id="e1867-215">Each of the structure members uses a semantic.</span></span>


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



<span data-ttu-id="e1867-216">Die Eingabestruktur identifiziert die Daten aus dem Scheitelpunktpuffer, der die Shadereingaben bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e1867-216">The input structure identifies the data from the vertex buffer that will provide the shader inputs.</span></span> <span data-ttu-id="e1867-217">Dieser Shader ordnet die Daten aus den Elementen position, normal und blendweight des Vertexpuffers in Vertex-Shaderregister zu.</span><span class="sxs-lookup"><span data-stu-id="e1867-217">This shader maps the data from the position, normal, and blendweight elements of the vertex buffer into vertex shader registers.</span></span> <span data-ttu-id="e1867-218">Der Eingabedatentyp muss nicht genau mit dem Datentyp der Scheitelpunktdeklaration übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e1867-218">The input data type does not have to exactly match the vertex declaration data type.</span></span> <span data-ttu-id="e1867-219">Wenn sie nicht genau übereinstimmen, werden die Scheitelpunktdaten automatisch in den HLSL-Datentyp konvertiert, wenn sie in die Shaderregister geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-219">If it doesn't exactly match, the vertex data will automatically be converted into the HLSL's data type when it is written into the shader registers.</span></span> <span data-ttu-id="e1867-220">Wenn die normalen Daten beispielsweise von der Anwendung als UINT-Typ definiert wurden, werden sie beim Lesen durch den Shader in float3 konvertiert.</span><span class="sxs-lookup"><span data-stu-id="e1867-220">For instance, if the normal data were defined to be of type UINT by the application, it would be converted into a float3 when read by the shader.</span></span>

<span data-ttu-id="e1867-221">Wenn die Daten im Scheitelpunktstream weniger Komponenten als der entsprechende Shaderdatentyp enthalten, werden die fehlenden Komponenten mit 0 initialisiert (mit Ausnahme von w, das mit 1 initialisiert wird).</span><span class="sxs-lookup"><span data-stu-id="e1867-221">If the data in the vertex stream contains fewer components than the corresponding shader data type, the missing components will be initialized to 0 (except for w, which is initialized to 1).</span></span>

<span data-ttu-id="e1867-222">Die Eingabesemantik ähnelt den Werten in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span><span class="sxs-lookup"><span data-stu-id="e1867-222">Input semantics are similar to the values in the [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span></span>

<span data-ttu-id="e1867-223">Die Ausgabestruktur identifiziert die Vertex-Shader-Ausgabeparameter der Position und Farbe.</span><span class="sxs-lookup"><span data-stu-id="e1867-223">The output structure identifies the vertex shader output parameters of position and color.</span></span> <span data-ttu-id="e1867-224">Diese Ausgaben werden von der Pipeline für die Dreiecksrasterung (bei primitiver Verarbeitung) verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1867-224">These outputs will be used by the pipeline for triangle rasterization (in primitive processing).</span></span> <span data-ttu-id="e1867-225">Die als Positionsdaten markierte Ausgabe gibt die Position eines Scheitelpunkts im homogenen Raum an.</span><span class="sxs-lookup"><span data-stu-id="e1867-225">The output marked as position data denotes the position of a vertex in homogeneous space.</span></span> <span data-ttu-id="e1867-226">Ein Vertex-Shader muss mindestens Positionsdaten generieren.</span><span class="sxs-lookup"><span data-stu-id="e1867-226">As a minimum, a vertex shader must generate position data.</span></span> <span data-ttu-id="e1867-227">Die Position des Bildschirmraums wird berechnet, nachdem der Vertex-Shader abgeschlossen wurde, indem die Koordinate (x, y, z) durch w dividiert wird.</span><span class="sxs-lookup"><span data-stu-id="e1867-227">The screen space position is computed after the vertex shader completes by dividing the (x, y, z) coordinate by w.</span></span> <span data-ttu-id="e1867-228">Im Bildschirmbereich sind -1 und 1 die minimalen und maximalen x- und y-Werte der Grenzen des Viewports, während z für Z-Puffertests verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e1867-228">In screen space, -1 and 1 are the minimum and maximum x and y values of the boundaries of the viewport, while z is used for z-buffer testing.</span></span>

<span data-ttu-id="e1867-229">Die Ausgabesemantik ähnelt auch den Werten in [**D3DDECLUSAGE.**](/windows/desktop/direct3d9/d3ddeclusage)</span><span class="sxs-lookup"><span data-stu-id="e1867-229">Output semantics are also similar to the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span></span> <span data-ttu-id="e1867-230">Im Allgemeinen kann eine Ausgabestruktur für einen Vertex-Shader auch als Eingabestruktur für einen Pixel-Shader verwendet werden, vorausgesetzt, der Pixel-Shader liest nicht aus einer Variablen, die mit der Position, Punktgröße oder Semantik markiert ist.</span><span class="sxs-lookup"><span data-stu-id="e1867-230">In general, an output structure for a vertex shader can also be used as the input structure for a pixel shader, provided the pixel shader does not read from any variable marked with the position, point size, or fog semantics.</span></span> <span data-ttu-id="e1867-231">Diese Semantik ist Skalarwerten pro Scheitelpunkt zugeordnet, die nicht von einem Pixel-Shader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-231">These semantics are associated with per-vertex scalar values that are not used by a pixel shader.</span></span> <span data-ttu-id="e1867-232">Wenn diese Werte für den Pixel-Shader benötigt werden, können sie in eine andere Ausgabevariable kopiert werden, die eine Pixel-Shadersemantik verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1867-232">If these values are needed for the pixel shader, they can be copied into another output variable that uses a pixel shader semantic.</span></span>

<span data-ttu-id="e1867-233">Globale Variablen werden Registern automatisch vom Compiler zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e1867-233">Global variables are assigned to registers automatically by the compiler.</span></span> <span data-ttu-id="e1867-234">Globale Variablen werden auch als einheitliche Parameter bezeichnet, da der Inhalt der Variablen für alle Pixel identisch ist, die jedes Mal verarbeitet werden, wenn der Shader aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e1867-234">Global variables are also called uniform parameters because the contents of the variable is the same for all pixels processed each time the shader is called.</span></span> <span data-ttu-id="e1867-235">Die Register sind in der Konstantentabelle enthalten, die mithilfe der [**ID3DXConstantTable-Schnittstelle gelesen werden**](/windows/desktop/direct3d9/id3dxconstanttable) kann.</span><span class="sxs-lookup"><span data-stu-id="e1867-235">The registers are contained in the constant table, which can be read using the [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) interface.</span></span>

<span data-ttu-id="e1867-236">Eingabesemantik für Pixel-Shader ordnen Werte bestimmten Hardwareregistern für den Transport zwischen Vertex-Shadern und Pixel-Shadern zu.</span><span class="sxs-lookup"><span data-stu-id="e1867-236">Input semantics for pixel shaders map values into specific hardware registers for transport between vertex shaders and pixel shaders.</span></span> <span data-ttu-id="e1867-237">Jeder Registertyp verfügt über bestimmte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e1867-237">Each register type has specific properties.</span></span> <span data-ttu-id="e1867-238">Da es derzeit nur zwei Semantiken für Farb- und Texturkoordinaten gibt, ist es üblich, dass die meisten Daten auch dann als Texturkoordinate markiert werden, wenn dies nicht dere ist.</span><span class="sxs-lookup"><span data-stu-id="e1867-238">Because there are currently only two semantics for color and texture coordinates, it is common for most data to be marked as a texture coordinate even when it is not.</span></span>

<span data-ttu-id="e1867-239">Beachten Sie, dass die Vertex-Shader-Ausgabestruktur eine Eingabe mit Positionsdaten verwendet hat, die nicht vom Pixelshader verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e1867-239">Notice that the vertex shader output structure used an input with position data, which is not used by the pixel shader.</span></span> <span data-ttu-id="e1867-240">HLSL ermöglicht gültige Ausgabedaten eines Vertex-Shaders, die keine gültigen Eingabedaten für einen Pixel-Shader sind, vorausgesetzt, dass im Pixelshader nicht darauf verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e1867-240">HLSL allows valid output data of a vertex shader that is not valid input data for a pixel shader, provided that it is not referenced in the pixel shader.</span></span>

<span data-ttu-id="e1867-241">Eingabeargumente können auch Arrays sein.</span><span class="sxs-lookup"><span data-stu-id="e1867-241">Input arguments can also be arrays.</span></span> <span data-ttu-id="e1867-242">Semantik wird automatisch vom Compiler für jedes Element des Arrays erhöht.</span><span class="sxs-lookup"><span data-stu-id="e1867-242">Semantics are automatically incremented by the compiler for each element of the array.</span></span> <span data-ttu-id="e1867-243">Betrachten Sie beispielsweise die folgende explizite Deklaration:</span><span class="sxs-lookup"><span data-stu-id="e1867-243">For instance, consider the following explicit declaration:</span></span>


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



<span data-ttu-id="e1867-244">Die oben angegebene explizite Deklaration entspricht der folgenden Deklaration, deren Semantik automatisch vom Compiler erhöht wird:</span><span class="sxs-lookup"><span data-stu-id="e1867-244">The explicit declaration given above is equivalent to the following declaration that will have semantics automatically incremented by the compiler:</span></span>


```
float4 Sparkle(float4 Position : POSITION,
                 float3 Col[2] : COLOR0,
                 float3 Tex[4] : TEXCOORD0) : COLOR0
{
   // shader statements
   ...
```



<span data-ttu-id="e1867-245">Genau wie die Eingabesemantik identifiziert die Ausgabesemantik die Datenverwendung für Pixel-Shader-Ausgabedaten.</span><span class="sxs-lookup"><span data-stu-id="e1867-245">Just like input semantics, output semantics identify data usage for pixel shader output data.</span></span> <span data-ttu-id="e1867-246">Viele Pixelshader schreiben nur in eine Ausgabefarbe.</span><span class="sxs-lookup"><span data-stu-id="e1867-246">Many pixel shaders write to only one output color.</span></span> <span data-ttu-id="e1867-247">Pixel-Shader können einen Tiefenwert auch gleichzeitig in ein oder mehrere Renderziele schreiben (bis zu vier).</span><span class="sxs-lookup"><span data-stu-id="e1867-247">Pixel shaders can also write out a depth value into one or more multiple render targets at the same time (up to four).</span></span> <span data-ttu-id="e1867-248">Wie Vertex-Shader verwenden Pixel-Shader eine -Struktur, um mehr als eine Ausgabe zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="e1867-248">Like vertex shaders, pixel shaders use a structure to return more than one output.</span></span> <span data-ttu-id="e1867-249">Dieser Shader schreibt 0 in die Farbkomponenten sowie in die Tiefenkomponente.</span><span class="sxs-lookup"><span data-stu-id="e1867-249">This shader writes 0 to the color components, as well as to the depth component.</span></span>


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



<span data-ttu-id="e1867-250">Die Pixel-Shader-Ausgabefarben müssen vom Typ float4 sein.</span><span class="sxs-lookup"><span data-stu-id="e1867-250">Pixel shader output colors must be of type float4.</span></span> <span data-ttu-id="e1867-251">Beim Schreiben mehrerer Farben müssen alle Ausgabefarben zusammenhängend verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-251">When writing multiple colors, all output colors must be used contiguously.</span></span> <span data-ttu-id="e1867-252">Anders ausgedrückt: [COLOR1](dx-graphics-hlsl-semantics.md) kann nur dann eine Ausgabe sein, wenn [COLOR0](dx-graphics-hlsl-semantics.md) bereits geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="e1867-252">In other words, [COLOR1](dx-graphics-hlsl-semantics.md) cannot be an output unless [COLOR0](dx-graphics-hlsl-semantics.md) has already been written.</span></span> <span data-ttu-id="e1867-253">Die Pixel-Shader-Tiefenausgabe muss vom Typ float1 sein.</span><span class="sxs-lookup"><span data-stu-id="e1867-253">Pixel shader depth output must be of type float1.</span></span>

### <a name="samplers-and-texture-objects"></a><span data-ttu-id="e1867-254">Sampler und Texturobjekte</span><span class="sxs-lookup"><span data-stu-id="e1867-254">Samplers and Texture Objects</span></span>

<span data-ttu-id="e1867-255">Ein Sampler enthält den Samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="e1867-255">A sampler contains sampler state.</span></span> <span data-ttu-id="e1867-256">Der Samplerzustand gibt die Textur an, für die Stichproben entnommen werden sollen, und steuert die Filterung, die während der Stichprobenentnahme erfolgt.</span><span class="sxs-lookup"><span data-stu-id="e1867-256">Sampler state specifies the texture to be sampled, and controls the filtering that is done during sampling.</span></span> <span data-ttu-id="e1867-257">Es sind drei Dinge erforderlich, um eine Textur zu beproben:</span><span class="sxs-lookup"><span data-stu-id="e1867-257">Three things are required to sample a texture:</span></span>

-   <span data-ttu-id="e1867-258">Eine Textur</span><span class="sxs-lookup"><span data-stu-id="e1867-258">A texture</span></span>
-   <span data-ttu-id="e1867-259">Ein Sampler (mit Samplerzustand)</span><span class="sxs-lookup"><span data-stu-id="e1867-259">A sampler (with sampler state)</span></span>
-   <span data-ttu-id="e1867-260">Eine Samplinganweisung</span><span class="sxs-lookup"><span data-stu-id="e1867-260">A sampling instruction</span></span>

<span data-ttu-id="e1867-261">Sampler können mit Texturen und dem Samplerzustand initialisiert werden, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="e1867-261">Samplers can be initialized with textures and sampler state as shown here:</span></span>


```
sampler s = sampler_state 
{ 
  texture = NULL; 
  mipfilter = LINEAR; 
};
```



<span data-ttu-id="e1867-262">Im Folgenden finden Sie ein Beispiel für den Code zum Beispiel für eine 2D-Textur:</span><span class="sxs-lookup"><span data-stu-id="e1867-262">Here's an example of the code to sample a 2D texture:</span></span>


```
texture tex0;
sampler2D s_2D;

float2 sample_2D(float2 tex : TEXCOORD0) : COLOR
{
  return tex2D(s_2D, tex);
}
```



<span data-ttu-id="e1867-263">Die Textur wird mit einer Texturvariablen tex0 deklariert.</span><span class="sxs-lookup"><span data-stu-id="e1867-263">The texture is declared with a texture variable tex0.</span></span>

<span data-ttu-id="e1867-264">In diesem Beispiel wird eine Samplervariable mit dem Namen s \_ 2D deklariert.</span><span class="sxs-lookup"><span data-stu-id="e1867-264">In this example, a sampler variable named s\_2D is declared.</span></span> <span data-ttu-id="e1867-265">Der Sampler enthält den Samplerzustand in geschweiften Klammern.</span><span class="sxs-lookup"><span data-stu-id="e1867-265">The sampler contains the sampler state inside of curly braces.</span></span> <span data-ttu-id="e1867-266">Dies schließt die Textur ein, für die Stichproben entnommen werden, und optional den Filterzustand (d. h. Umbruchmodi, Filtermodi usw.).</span><span class="sxs-lookup"><span data-stu-id="e1867-266">This includes the texture that will be sampled and, optionally, the filter state (that is, wrap modes, filter modes, etc.).</span></span> <span data-ttu-id="e1867-267">Wenn der Samplerzustand weggelassen wird, wird ein Standardzustand des Samplers angewendet, der lineare Filterung und einen Umbruchmodus für die Texturkoordinaten an.</span><span class="sxs-lookup"><span data-stu-id="e1867-267">If the sampler state is omitted, a default sampler state is applied specifying linear filtering and a wrap mode for the texture coordinates.</span></span> <span data-ttu-id="e1867-268">Die Samplerfunktion verwendet eine Gleitkommatexturkoordinate mit zwei Komponenten und gibt eine Zwei-Komponenten-Farbe zurück.</span><span class="sxs-lookup"><span data-stu-id="e1867-268">The sampler function takes a two-component floating-point texture coordinate, and returns a two-component color.</span></span> <span data-ttu-id="e1867-269">Dies wird mit dem Rückgabetyp float2 dargestellt und stellt Daten in den roten und grünen Komponenten dar.</span><span class="sxs-lookup"><span data-stu-id="e1867-269">This is represented with the float2 return type and represents data in the red and green components.</span></span>

<span data-ttu-id="e1867-270">Es werden vier Typen von Samplern definiert (siehe Schlüsselwörter [),](dx-graphics-hlsl-appendix.md)und Textursuchen werden von den systeminternen Funktionen ausgeführt: [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**tex3D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE(s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md).</span><span class="sxs-lookup"><span data-stu-id="e1867-270">Four types of samplers are defined (see [Keywords](dx-graphics-hlsl-appendix.md)) and texture lookups are performed by the intrinsic functions: [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**tex3D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE(s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md).</span></span> <span data-ttu-id="e1867-271">Hier ist ein Beispiel für die 3D-Stichprobenentnahme:</span><span class="sxs-lookup"><span data-stu-id="e1867-271">Here is an example of 3D sampling:</span></span>


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



<span data-ttu-id="e1867-272">Diese Samplerdeklaration verwendet den Standardmäßigen Samplerzustand für die Filtereinstellungen und den Adressmodus.</span><span class="sxs-lookup"><span data-stu-id="e1867-272">This sampler declaration uses default sampler state for the filter settings and address mode.</span></span>

<span data-ttu-id="e1867-273">Hier ist das entsprechende Beispiel für die Cubesstichprobe:</span><span class="sxs-lookup"><span data-stu-id="e1867-273">Here is the corresponding cube sampling example:</span></span>


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



<span data-ttu-id="e1867-274">Und schließlich ist hier das Beispiel für die 1D-Stichprobenentnahme:</span><span class="sxs-lookup"><span data-stu-id="e1867-274">And finally, here is the 1D sampling example:</span></span>


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



<span data-ttu-id="e1867-275">Da die Runtime keine 1D-Texturen unterstützt, verwendet der Compiler eine 2D-Textur mit dem Wissen, dass die y-Koordinate unwichtig ist.</span><span class="sxs-lookup"><span data-stu-id="e1867-275">Because the runtime does not support 1D textures, the compiler will use a 2D texture with the knowledge that the y-coordinate is unimportant.</span></span> <span data-ttu-id="e1867-276">Da [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) als 2D-Textursuche implementiert wird, kann der Compiler die y-Komponente effizient auswählen.</span><span class="sxs-lookup"><span data-stu-id="e1867-276">Since [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) is implemented as a 2D texture lookup, the compiler is free to choose the y-component in an efficient manner.</span></span> <span data-ttu-id="e1867-277">In einigen seltenen Szenarien kann der Compiler keine effiziente y-Komponente auswählen. In diesem Fall gibt er eine Warnung aus.</span><span class="sxs-lookup"><span data-stu-id="e1867-277">In some rare scenarios, the compiler cannot choose an efficient y-component, in which case it will issue a warning.</span></span>


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



<span data-ttu-id="e1867-278">Dieses spezielle Beispiel ist ineffizient, da der Compiler die Eingabekoordinate in ein anderes Register verschieben muss (da eine 1D-Suche als 2D-Suche implementiert und die Texturkoordinate als float1 deklariert wird).</span><span class="sxs-lookup"><span data-stu-id="e1867-278">This particular example is inefficient because the compiler must move the input coordinate into another register (because a 1D lookup is implemented as a 2D lookup and the texture coordinate is declared as a float1).</span></span> <span data-ttu-id="e1867-279">Wenn der Code mithilfe einer float2-Eingabe anstelle von float1 umgeschrieben wird, kann der Compiler die Eingabetexturkoordinate verwenden, da er weiß, dass y mit etwas initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e1867-279">If the code is rewritten using a float2 input instead of a float1, the compiler can use the input texture coordinate because it knows that y is initialized to something.</span></span>


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



<span data-ttu-id="e1867-280">Alle Texturs lookups können mit "bias" oder "proj" (d.h. [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**texCUBEproj (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)) angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-280">All texture lookups can be appended with "bias" or "proj" (that is, [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**texCUBEproj (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)).</span></span> <span data-ttu-id="e1867-281">Mit dem Suffix "proj" wird die Texturkoordinate durch die w-Komponente geteilt.</span><span class="sxs-lookup"><span data-stu-id="e1867-281">With the "proj" suffix, the texture coordinate is divided by the w-component.</span></span> <span data-ttu-id="e1867-282">Mit "Bias" wird die Mip-Ebene von der w-Komponente verschoben.</span><span class="sxs-lookup"><span data-stu-id="e1867-282">With "bias," the mip level is shifted by the w-component.</span></span> <span data-ttu-id="e1867-283">Daher nehmen alle Texturs lookups mit einem Suffix immer eine float4-Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="e1867-283">Thus, all texture lookups with a suffix always take a float4 input.</span></span> <span data-ttu-id="e1867-284">[**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) und [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignorieren die yz- bzw. z-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="e1867-284">[**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) and [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignore the yz- and z-components respectively.</span></span>

<span data-ttu-id="e1867-285">Sampler können auch im Array verwendet werden, obwohl derzeit kein Back-End den dynamischen Arrayzugriff auf Sampler unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1867-285">Samplers may also be used in array, although no back end currently supports dynamic array access of samplers.</span></span> <span data-ttu-id="e1867-286">Daher ist Folgendes gültig, da es zur Kompilierzeit aufgelöst werden kann:</span><span class="sxs-lookup"><span data-stu-id="e1867-286">Therefore, the following is valid because it can be resolved at compile time:</span></span>


```
tex2D(s[0],tex)
```



<span data-ttu-id="e1867-287">Dieses Beispiel ist jedoch ungültig.</span><span class="sxs-lookup"><span data-stu-id="e1867-287">However, this example is not valid.</span></span>


```
tex2D(s[a],tex)
```



<span data-ttu-id="e1867-288">Der dynamische Zugriff auf Sampler ist in erster Linie für das Schreiben von Programmen mit Literalschleifen nützlich.</span><span class="sxs-lookup"><span data-stu-id="e1867-288">Dynamic access of samplers is primarily useful for writing programs with literal loops.</span></span> <span data-ttu-id="e1867-289">Der folgende Code veranschaulicht den Zugriff auf Samplerarrays:</span><span class="sxs-lookup"><span data-stu-id="e1867-289">The following code illustrates sampler array accessing:</span></span>


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
> <span data-ttu-id="e1867-290">Mithilfe der Microsoft Direct3D-Debuglaufzeit können Sie Konflikte zwischen der Anzahl der Komponenten in einer Textur und einem Sampler abfangen.</span><span class="sxs-lookup"><span data-stu-id="e1867-290">Using the Microsoft Direct3D debug runtime can help you catch mismatches between the number of components in a texture and a sampler.</span></span>

 

## <a name="writing-functions"></a><span data-ttu-id="e1867-291">Schreiben von Funktionen</span><span class="sxs-lookup"><span data-stu-id="e1867-291">Writing Functions</span></span>

<span data-ttu-id="e1867-292">Funktionen untergliedern große Aufgaben in kleinere Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="e1867-292">Functions break large tasks into smaller ones.</span></span> <span data-ttu-id="e1867-293">Kleine Aufgaben lassen sich einfacher debuggen und können wiederverwendet werden, sobald sie sich bewährt haben.</span><span class="sxs-lookup"><span data-stu-id="e1867-293">Small tasks are easier to debug and can be reused, once proven.</span></span> <span data-ttu-id="e1867-294">Funktionen können verwendet werden, um Details anderer Funktionen auszublenden, wodurch ein Programm, das aus Funktionen besteht, einfacher zu verfolgen ist.</span><span class="sxs-lookup"><span data-stu-id="e1867-294">Functions can be used to hide details of other functions, which makes a program composed of functions easier to follow.</span></span>

<span data-ttu-id="e1867-295">HLSL-Funktionen ähneln C-Funktionen auf verschiedene Weise: Sie enthalten sowohl eine Definition als auch einen Funktionskörper und deklarieren Rückgabetypen und Argumentlisten.</span><span class="sxs-lookup"><span data-stu-id="e1867-295">HLSL functions are similar to C functions in several ways: They both contain a definition and a function body and they both declare return types and argument lists.</span></span> <span data-ttu-id="e1867-296">Wie C-Funktionen werden bei der HLSL-Überprüfung die Argumente, Argumenttypen und der Rückgabewert während der Shaderkompilierung überprüft.</span><span class="sxs-lookup"><span data-stu-id="e1867-296">Like C functions, HLSL validation does type checking on the arguments, argument types, and the return value during shader compilation.</span></span>

<span data-ttu-id="e1867-297">Im Gegensatz zu C-Funktionen verwenden HLSL-Einstiegspunktfunktionen Semantik, um Funktionsargumente an Shadereingaben und -ausgaben zu binden (HLSL-Funktionen, die intern als Semantik bezeichnet werden).</span><span class="sxs-lookup"><span data-stu-id="e1867-297">Unlike C functions, HLSL entry point functions use semantics to bind function arguments to shader inputs and outputs (HLSL functions called internally ignore semantics).</span></span> <span data-ttu-id="e1867-298">Dies erleichtert das Binden von Pufferdaten an einen Shader und das Binden von Shader-Ausgaben an Shadereingaben.</span><span class="sxs-lookup"><span data-stu-id="e1867-298">This makes it easier to bind buffer data to a shader, and bind shader outputs to shader inputs.</span></span>

<span data-ttu-id="e1867-299">Eine Funktion enthält eine Deklaration und einen Text, und die Deklaration muss dem Text voran gehen.</span><span class="sxs-lookup"><span data-stu-id="e1867-299">A function contains a declaration and a body, and the declaration must precede the body.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



<span data-ttu-id="e1867-300">Die Funktionsdeklaration enthält alles vor den geschweiften Klammern:</span><span class="sxs-lookup"><span data-stu-id="e1867-300">The function declaration includes everything in front of the curly braces:</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



<span data-ttu-id="e1867-301">Eine Funktionsdeklaration enthält:</span><span class="sxs-lookup"><span data-stu-id="e1867-301">A function declaration contains:</span></span>

-   <span data-ttu-id="e1867-302">Ein Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="e1867-302">A return type</span></span>
-   <span data-ttu-id="e1867-303">Ein Funktionsname</span><span class="sxs-lookup"><span data-stu-id="e1867-303">A function name</span></span>
-   <span data-ttu-id="e1867-304">Eine Argumentliste (optional)</span><span class="sxs-lookup"><span data-stu-id="e1867-304">An argument list (optional)</span></span>
-   <span data-ttu-id="e1867-305">Eine Ausgabesemantik (optional)</span><span class="sxs-lookup"><span data-stu-id="e1867-305">An output semantic (optional)</span></span>
-   <span data-ttu-id="e1867-306">Eine Anmerkung (optional)</span><span class="sxs-lookup"><span data-stu-id="e1867-306">An annotation (optional)</span></span>

<span data-ttu-id="e1867-307">Der Rückgabetyp kann jeder der grundlegenden HLSL-Datentypen sein, z. B. float4:</span><span class="sxs-lookup"><span data-stu-id="e1867-307">The return type can be any of the HLSL basic data types such as a float4:</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
   ...
}
```



<span data-ttu-id="e1867-308">Der Rückgabetyp kann eine Struktur sein, die bereits definiert wurde:</span><span class="sxs-lookup"><span data-stu-id="e1867-308">The return type can be a structure that has already been defined:</span></span>


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



<span data-ttu-id="e1867-309">Wenn die Funktion keinen Wert zurück gibt, kann void als Rückgabetyp verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-309">If the function does not return a value, void can be used as the return type.</span></span>


```
void VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



<span data-ttu-id="e1867-310">Der Rückgabetyp wird immer zuerst in einer Funktionsdeklaration angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e1867-310">The return type always appears first in a function declaration.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



<span data-ttu-id="e1867-311">Eine Argumentliste deklariert die Eingabeargumente für eine Funktion.</span><span class="sxs-lookup"><span data-stu-id="e1867-311">An argument list declares the input arguments to a function.</span></span> <span data-ttu-id="e1867-312">Sie kann auch Werte deklarieren, die zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-312">It may also declare values that will be returned.</span></span> <span data-ttu-id="e1867-313">Einige Argumente sind sowohl Eingabe- als auch Ausgabeargumente.</span><span class="sxs-lookup"><span data-stu-id="e1867-313">Some arguments are both input and output arguments.</span></span> <span data-ttu-id="e1867-314">Hier ist ein Beispiel für einen Shader, der vier Eingabeargumente verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1867-314">Here is an example of a shader that takes four input arguments.</span></span>


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



<span data-ttu-id="e1867-315">Diese Funktion gibt eine endgültige Farbe zurück, die eine Mischung aus einem Texturbeispiel und der hellen Farbe ist.</span><span class="sxs-lookup"><span data-stu-id="e1867-315">This function returns a final color, that is a blend of a texture sample and the light color.</span></span> <span data-ttu-id="e1867-316">Die Funktion nimmt vier Eingaben entgegen.</span><span class="sxs-lookup"><span data-stu-id="e1867-316">The function takes four inputs.</span></span> <span data-ttu-id="e1867-317">Zwei Eingaben haben Semantik: LightDir hat die [TEXCOORD1-Semantik](dx-graphics-hlsl-semantics.md) und texcrd die [TEXCOORD0-Semantik.](dx-graphics-hlsl-semantics.md)</span><span class="sxs-lookup"><span data-stu-id="e1867-317">Two inputs have semantics: LightDir has the [TEXCOORD1](dx-graphics-hlsl-semantics.md) semantic, and texcrd has the [TEXCOORD0](dx-graphics-hlsl-semantics.md) semantic.</span></span> <span data-ttu-id="e1867-318">Die Semantik bedeutet, dass die Daten für diese Variablen aus dem Scheitelpunktpuffer stammen.</span><span class="sxs-lookup"><span data-stu-id="e1867-318">The semantics mean that the data for these variables will come from the vertex buffer.</span></span> <span data-ttu-id="e1867-319">Obwohl die LightDir-Variable über eine [TEXCOORD1-Semantik](dx-graphics-hlsl-semantics.md) verfügt, ist der Parameter wahrscheinlich keine Texturkoordinate.</span><span class="sxs-lookup"><span data-stu-id="e1867-319">Even though the LightDir variable has a [TEXCOORD1](dx-graphics-hlsl-semantics.md) semantic, the parameter is probably not a texture coordinate.</span></span> <span data-ttu-id="e1867-320">Der TEXCOORDn-Semantiktyp wird häufig verwendet, um eine Semantik für einen Typ zu liefern, der nicht vordefiniert ist (es gibt keine Vertex-Shader-Eingabesemantik für eine lichte Richtung).</span><span class="sxs-lookup"><span data-stu-id="e1867-320">The TEXCOORDn semantic type is often used to supply a semantic for a type that is not predefined (there is no vertex shader input semantic for a light direction).</span></span>

<span data-ttu-id="e1867-321">Die beiden anderen Eingaben LightColor und samp sind mit dem [Schlüsselwort uniform](dx-graphics-hlsl-appendix.md) gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e1867-321">The other two inputs LightColor and samp are labeled with the [uniform](dx-graphics-hlsl-appendix.md) keyword.</span></span> <span data-ttu-id="e1867-322">Dies sind einheitliche Konstanten, die sich zwischen Draw-Aufrufen nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="e1867-322">These are uniform constants that will not change between draw calls.</span></span> <span data-ttu-id="e1867-323">Die Werte für diese Parameter stammen aus globalen Shadervariablen.</span><span class="sxs-lookup"><span data-stu-id="e1867-323">The values for these parameters come from shader global variables.</span></span>

<span data-ttu-id="e1867-324">Argumente können als Eingaben mit dem Schlüsselwort in und Ausgabeargumente mit dem Schlüsselwort out bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-324">Arguments can be labeled as inputs with the in keyword, and output arguments with the out keyword.</span></span> <span data-ttu-id="e1867-325">Argumente können nicht als Verweis übergeben werden. Ein Argument kann jedoch sowohl eine Eingabe als auch eine Ausgabe sein, wenn es mit dem Schlüsselwort inout deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="e1867-325">Arguments cannot be passed by reference; however, an argument can be both an input and an output if it is declared with the inout keyword.</span></span> <span data-ttu-id="e1867-326">Argumente, die an eine Funktion übergeben werden, die mit dem Schlüsselwort inout markiert sind, werden als Kopien des Originals betrachtet, bis die Funktion zurückgegeben wird, und sie werden zurückkopiert.</span><span class="sxs-lookup"><span data-stu-id="e1867-326">Arguments passed to a function that are marked with the inout keyword are considered copies of the original until the function returns, and they are copied back.</span></span> <span data-ttu-id="e1867-327">Hier sehen Sie ein Beispiel für die Verwendung von inout:</span><span class="sxs-lookup"><span data-stu-id="e1867-327">Here's an example using inout:</span></span>


```
void Increment_ByVal(inout float A, inout float B) 
{ 
    A++; B++;
}
```



<span data-ttu-id="e1867-328">Diese Funktion erhöht die Werte in A und B und gibt sie zurück.</span><span class="sxs-lookup"><span data-stu-id="e1867-328">This function increments the values in A and B and returns them.</span></span>

<span data-ttu-id="e1867-329">Der Funktionstext ist der gesamte Code nach der Funktionsdeklaration.</span><span class="sxs-lookup"><span data-stu-id="e1867-329">The function body is all of the code after the function declaration.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



<span data-ttu-id="e1867-330">Der Text besteht aus Anweisungen, die von geschweiften Klammern umgeben sind.</span><span class="sxs-lookup"><span data-stu-id="e1867-330">The body consists of statements which are surrounded by curly braces.</span></span> <span data-ttu-id="e1867-331">Der Funktionstext implementiert alle Funktionen mithilfe von Variablen, Literalen, Ausdrücken und Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="e1867-331">The function body implements all of the functionality using variables, literals, expressions, and statements.</span></span>

<span data-ttu-id="e1867-332">Der Shadertext führt zwei Dinge aus: Er führt eine Matrixmultiplikation aus und gibt ein float4-Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="e1867-332">The shader body does two things: it performs a matrix multiply and returns a float4 result.</span></span> <span data-ttu-id="e1867-333">Die Matrixmultiplikation wird mit der Multiplikationsfunktion [**mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) durchgeführt, die eine Multiplikation der 4x4-Matrix ausführt.</span><span class="sxs-lookup"><span data-stu-id="e1867-333">The matrix multiply is accomplished with the [**mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) function, which performs a 4x4 matrix multiply.</span></span> <span data-ttu-id="e1867-334">**mul (DirectX HLSL)** wird als systeminterne Funktion bezeichnet, da sie bereits in die HLSL-Funktionsbibliothek integriert ist.</span><span class="sxs-lookup"><span data-stu-id="e1867-334">**mul (DirectX HLSL)** is called an intrinsic function because it is already built into the HLSL library of functions.</span></span> <span data-ttu-id="e1867-335">Systeminterne Funktionen werden im nächsten Abschnitt ausführlicher behandelt.</span><span class="sxs-lookup"><span data-stu-id="e1867-335">Intrinsic functions will be covered in more detail in the next section.</span></span>

<span data-ttu-id="e1867-336">Die Matrixmultiplikation kombiniert einen Eingabevektor Pos und eine zusammengesetzte Matrix WorldViewProj.</span><span class="sxs-lookup"><span data-stu-id="e1867-336">The matrix multiply combines an input vector Pos and a composite matrix WorldViewProj.</span></span> <span data-ttu-id="e1867-337">Das Ergebnis sind Positionsdaten, die in den Bildschirmbereich transformiert werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-337">The result is position data transformed into screen space.</span></span> <span data-ttu-id="e1867-338">Dies ist die minimale Vertex-Shaderverarbeitung, die wir tun können.</span><span class="sxs-lookup"><span data-stu-id="e1867-338">This is the minimum vertex shader processing we can do.</span></span> <span data-ttu-id="e1867-339">Wenn wir die Pipeline für feste Funktionen anstelle eines Vertex-Shaders verwenden, können die Vertexdaten nach dieser Transformation gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-339">If we were using the fixed function pipeline instead of a vertex shader, the vertex data could be drawn after doing this transform.</span></span>

<span data-ttu-id="e1867-340">Die letzte Anweisung in einem Funktionskörper ist eine return-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="e1867-340">The last statement in a function body is a return statement.</span></span> <span data-ttu-id="e1867-341">Genau wie C gibt diese Anweisung die Steuerung von der Funktion an die Anweisung zurück, die die Funktion aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="e1867-341">Just like C, this statement returns control from the function to the statement that called the function.</span></span>

<span data-ttu-id="e1867-342">Funktions-Rückgabetypen können beliebige einfache Datentypen sein, die in HLSL definiert sind, einschließlich bool, int half, float und double.</span><span class="sxs-lookup"><span data-stu-id="e1867-342">Function return types can be any of the simple data types defined in HLSL, including bool, int half, float, and double.</span></span> <span data-ttu-id="e1867-343">Rückgabetypen können einen der komplexen Datentypen wie Vektoren und Matrizen sein.</span><span class="sxs-lookup"><span data-stu-id="e1867-343">Return types can be one of the complex data types such as vectors and matrices.</span></span> <span data-ttu-id="e1867-344">HLSL-Typen, die auf Objekte verweisen, können nicht als Rückgabetypen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-344">HLSL types that refer to objects cannot be used as return types.</span></span> <span data-ttu-id="e1867-345">Dies schließt Pixelshader, Vertexshader, Texture und Sampler ein.</span><span class="sxs-lookup"><span data-stu-id="e1867-345">This includes pixelshader, vertexshader, texture, and sampler.</span></span>

<span data-ttu-id="e1867-346">Hier ist ein Beispiel für eine Funktion, die eine -Struktur für einen Rückgabetyp verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1867-346">Here is an example of a function that uses a structure for a return type.</span></span>


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



<span data-ttu-id="e1867-347">Der Rückgabetyp float4 wurde durch die Vs OUTPUT-Struktur ersetzt, die \_ nun einen einzelnen float4-Member enthält.</span><span class="sxs-lookup"><span data-stu-id="e1867-347">The float4 return type has been replaced with the structure VS\_OUTPUT, which now contains a single float4 member.</span></span>

<span data-ttu-id="e1867-348">Eine return-Anweisung signalisiert das Ende einer Funktion.</span><span class="sxs-lookup"><span data-stu-id="e1867-348">A return statement signals the end of a function.</span></span> <span data-ttu-id="e1867-349">Dies ist die einfachste Return-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="e1867-349">This is the simplest return statement.</span></span> <span data-ttu-id="e1867-350">Sie gibt die Steuerung von der Funktion an das aufrufende Programm zurück.</span><span class="sxs-lookup"><span data-stu-id="e1867-350">It returns control from the function to the calling program.</span></span> <span data-ttu-id="e1867-351">Es wird kein Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e1867-351">It returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="e1867-352">Eine return-Anweisung kann einen oder mehrere Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e1867-352">A return statement can return one or more values.</span></span> <span data-ttu-id="e1867-353">In diesem Beispiel wird ein Literalwert zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="e1867-353">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="e1867-354">In diesem Beispiel wird das skalare Ergebnis eines Ausdrucks zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="e1867-354">This example returns the scalar result of an expression:</span></span>


```
return  light.enabled;
```



<span data-ttu-id="e1867-355">In diesem Beispiel wird ein float4-Wert zurückgegeben, der aus einer lokalen Variablen und einem Literal erstellt wurde:</span><span class="sxs-lookup"><span data-stu-id="e1867-355">This example returns a float4 constructed from a local variable and a literal:</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="e1867-356">In diesem Beispiel wird ein float4-Wert zurückgegeben, der aus dem Von einer systeminternen Funktion zurückgegebenen Ergebnis und einigen Literalwerten erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="e1867-356">This example returns a float4 that is constructed from the result returned from an intrinsic function, and a few literal values:</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="e1867-357">In diesem Beispiel wird eine -Struktur zurückgegeben, die einen oder mehrere Member enthält:</span><span class="sxs-lookup"><span data-stu-id="e1867-357">This example returns a structure that contains one or more members:</span></span>


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



## <a name="flow-control"></a><span data-ttu-id="e1867-358">Flusssteuerung</span><span class="sxs-lookup"><span data-stu-id="e1867-358">Flow Control</span></span>

<span data-ttu-id="e1867-359">Die meisten aktuellen Scheitelpunkt- und Pixel-Shaderhardware ist so konzipiert, dass eine Shaderlinie zeilenweisend ausgeführt wird, wobei jede Anweisung einmal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1867-359">Most current vertex and pixel shader hardware is designed to run a shader line by line, executing each instruction once.</span></span> <span data-ttu-id="e1867-360">HLSL unterstützt die Flusssteuerung, einschließlich statischer Verzweigung, prädikatierter Anweisungen, statischer Schleifen, dynamischer Verzweigung und dynamischer Schleifen.</span><span class="sxs-lookup"><span data-stu-id="e1867-360">HLSL supports flow control, which includes static branching, predicated instructions, static looping, dynamic branching, and dynamic looping.</span></span>

<span data-ttu-id="e1867-361">Zuvor führte die Verwendung einer if-Anweisung zu Assemblysprach-Shadercode, der sowohl die if-Seite als auch die andere Seite des Codeflows implementiert.</span><span class="sxs-lookup"><span data-stu-id="e1867-361">Previously, using an if statement resulted in assembly-language shader code that implements both the if side and the else side of the code flow.</span></span> <span data-ttu-id="e1867-362">Im Folgenden finden Sie ein Beispiel für den in HLSL-Code, der für \_ 1 1 kompiliert \_ wurde:</span><span class="sxs-lookup"><span data-stu-id="e1867-362">Here is an example of the in HLSL code that was compiled for vs\_1\_1:</span></span>


```
if (Value > 0)
    oPos = Value1; 
else
    oPos = Value2; 
```



<span data-ttu-id="e1867-363">Und hier ist der resultierende Assemblycode:</span><span class="sxs-lookup"><span data-stu-id="e1867-363">And here is the resulting assembly code:</span></span>


```
// Calculate linear interpolation value in r0.w
mov r1.w, c2.x               
slt r0.w, c3.x, r1.w         
// Linear interpolation between value1 and value2
mov r7, -c1                      
add r2, r7, c0                   
mad oPos, r0.w, r2, c1  
```



<span data-ttu-id="e1867-364">Einige Hardware ermöglicht entweder statisches oder dynamisches Schleifen, aber die meisten erfordern eine lineare Ausführung.</span><span class="sxs-lookup"><span data-stu-id="e1867-364">Some hardware allows for either static or dynamic looping, but most require linear execution.</span></span> <span data-ttu-id="e1867-365">Für die Modelle, die keine Schleifen unterstützen, muss die Registrierung aller Schleifen aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="e1867-365">On the models that do not support looping, all loops must be unrolled.</span></span> <span data-ttu-id="e1867-366">Ein Beispiel hierfür ist das [Beispiel "DepthOfField Sample",](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) das unrollierte Schleifen auch für Ps \_ 1 \_ 1-Shader verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1867-366">An example is the [DepthOfField Sample](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) sample that uses unrolled loops even for ps\_1\_1 shaders.</span></span>

<span data-ttu-id="e1867-367">HLSL bietet jetzt Unterstützung für jede dieser Arten von Flusssteuerung:</span><span class="sxs-lookup"><span data-stu-id="e1867-367">HLSL now includes support for each of these types of flow control:</span></span>

-   <span data-ttu-id="e1867-368">statische Verzweigung</span><span class="sxs-lookup"><span data-stu-id="e1867-368">static branching</span></span>
-   <span data-ttu-id="e1867-369">Prädikatanweisungen</span><span class="sxs-lookup"><span data-stu-id="e1867-369">predicated instructions</span></span>
-   <span data-ttu-id="e1867-370">Statisches Schleifen</span><span class="sxs-lookup"><span data-stu-id="e1867-370">static looping</span></span>
-   <span data-ttu-id="e1867-371">Dynamische Verzweigung</span><span class="sxs-lookup"><span data-stu-id="e1867-371">dynamic branching</span></span>
-   <span data-ttu-id="e1867-372">Dynamisches Schleifening</span><span class="sxs-lookup"><span data-stu-id="e1867-372">dynamic looping</span></span>

<span data-ttu-id="e1867-373">Statische Verzweigung ermöglicht das Ein- oder Ausschalten von Shadercodeblöcken basierend auf einer booleschen Shaderkonstante.</span><span class="sxs-lookup"><span data-stu-id="e1867-373">Static branching allows blocks of shader code to be switched on or off based on a Boolean shader constant.</span></span> <span data-ttu-id="e1867-374">Dies ist eine praktische Methode zum Aktivieren oder Deaktivieren von Codepfaden basierend auf dem Typ des objekts, das gerade gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="e1867-374">This is a convenient method for enabling or disabling code paths based on the type of object currently being rendered.</span></span> <span data-ttu-id="e1867-375">Zwischen Draw-Aufrufen können Sie entscheiden, welche Features Sie mit dem aktuellen Shader unterstützen möchten, und dann die booleschen Flags festlegen, die zum Abrufen dieses Verhaltens erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e1867-375">Between draw calls, you can decide which features you want to support with the current shader and then set the Boolean flags required to get that behavior.</span></span> <span data-ttu-id="e1867-376">Alle Anweisungen, die von einer booleschen Konstante deaktiviert werden, werden während der Shaderausführung übersprungen.</span><span class="sxs-lookup"><span data-stu-id="e1867-376">Any statements that are disabled by a Boolean constant are skipped during shader execution.</span></span>

<span data-ttu-id="e1867-377">Die vertrautste Branchunterstützung ist dynamische Verzweigung.</span><span class="sxs-lookup"><span data-stu-id="e1867-377">The most familiar branching support is dynamic branching.</span></span> <span data-ttu-id="e1867-378">Bei dynamischer Verzweigung befindet sich die Vergleichsbedingung in einer Variablen, was bedeutet, dass der Vergleich für jeden Scheitelpunkt oder jedes Pixel zur Laufzeit erfolgt (im Gegensatz zum Vergleich zur Kompilierzeit oder zwischen zwei Zeichnen-Aufrufen).</span><span class="sxs-lookup"><span data-stu-id="e1867-378">With dynamic branching, the comparison condition resides in a variable, which means that the comparison is done for each vertex or each pixel at run time (as opposed to the comparison occurring at compile time, or between two draw calls).</span></span> <span data-ttu-id="e1867-379">Die Leistungstreffer sind die Kosten für den Branch plus die Kosten der Anweisungen auf der Seite des Branchs.</span><span class="sxs-lookup"><span data-stu-id="e1867-379">The performance hit is the cost of the branch plus the cost of the instructions on the side of the branch taken.</span></span> <span data-ttu-id="e1867-380">Dynamische Verzweigung wird in Shadermodell 3 oder höher implementiert.</span><span class="sxs-lookup"><span data-stu-id="e1867-380">Dynamic branching is implemented in shader model 3 or higher.</span></span> <span data-ttu-id="e1867-381">Die Optimierung von Shadern, die mit diesen Modellen funktionieren, ähnelt der Optimierung von Code, der auf einer CPU ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1867-381">Optimizing shaders that work with these models is similar to optimizing code that runs on a CPU.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1867-382">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1867-382">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1867-383">Programmieranleitung für HLSL</span><span class="sxs-lookup"><span data-stu-id="e1867-383">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 
