---
description: Nachdem ein Effekt erstellt wurde, besteht der erste Schritt darin, den Code zu kompilieren, um auf Syntax Probleme zu überprüfen.
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: Kompilieren eines Effekts (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab6183f2f71b07c482fa24efc4f9fed199216d75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214084"
---
# <a name="compile-an-effect-direct3d-10"></a><span data-ttu-id="f54fc-103">Kompilieren eines Effekts (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f54fc-103">Compile an Effect (Direct3D 10)</span></span>

<span data-ttu-id="f54fc-104">Nachdem ein Effekt erstellt wurde, besteht der erste Schritt darin, den Code zu kompilieren, um auf Syntax Probleme zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f54fc-104">Once an effect has been authored, the first step is to compile the code to check for syntax problems.</span></span> <span data-ttu-id="f54fc-105">Dies erfolgt durch Aufrufen einer der Kompilierungs-APIs (z. b. D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory).</span><span class="sxs-lookup"><span data-stu-id="f54fc-105">This is done by calling one of the compile APIs (like D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory).</span></span> <span data-ttu-id="f54fc-106">Diese API ruft den Effekt Compiler auf fxc.exe der der Compiler ist, der zum Kompilieren von HLSL-Code verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f54fc-106">These API's invoke the effect compiler fxc.exe which is the compiler used to compile HLSL code.</span></span> <span data-ttu-id="f54fc-107">Aus diesem Grund sieht die Syntax für Code in einem Effekt sehr ähnlich wie der HLSL-Code aus (es gibt einige Ausnahmen, die später behandelt werden).</span><span class="sxs-lookup"><span data-stu-id="f54fc-107">This is why the syntax for code in an effect looks very much like HLSL code (there are a few exceptions that will be handled later).</span></span> <span data-ttu-id="f54fc-108">Auf diese Weise befindet sich der Effekt Compiler/HLSL Compiler (fxc.exe) im SDK im Ordner Hilfsprogramme, sodass Sie Ihre Shader (oder Effekte) Offline kompilieren können, wenn Sie auswählen.</span><span class="sxs-lookup"><span data-stu-id="f54fc-108">By the way, the effect compiler/hlsl compiler (fxc.exe) is in the SDK in the utilities folder so that you can compile your shaders (or effects) offline if you choose.</span></span> <span data-ttu-id="f54fc-109">Weitere Informationen finden Sie in der Dokumentation zum Ausführen des Compilers von der Befehlszeile aus.</span><span class="sxs-lookup"><span data-stu-id="f54fc-109">See the documentation for running the compiler from the command line.</span></span>

-   [<span data-ttu-id="f54fc-110">Includes</span><span class="sxs-lookup"><span data-stu-id="f54fc-110">Includes</span></span>](#includes)
-   [<span data-ttu-id="f54fc-111">Makros</span><span class="sxs-lookup"><span data-stu-id="f54fc-111">Macros</span></span>](#macros)
-   [<span data-ttu-id="f54fc-112">HLSL-shaderflags</span><span class="sxs-lookup"><span data-stu-id="f54fc-112">HLSL Shader Flags</span></span>](#hlsl-shader-flags)
-   [<span data-ttu-id="f54fc-113">FX-Flags</span><span class="sxs-lookup"><span data-stu-id="f54fc-113">FX Flags</span></span>](#fx-flags)
-   [<span data-ttu-id="f54fc-114">Überprüfen von Fehlern</span><span class="sxs-lookup"><span data-stu-id="f54fc-114">Checking Errors</span></span>](#checking-errors)
-   [<span data-ttu-id="f54fc-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f54fc-115">Related topics</span></span>](#related-topics)

<span data-ttu-id="f54fc-116">Im folgenden finden Sie ein Beispiel für das Kompilieren einer Effekt Datei (aus dem BasicHLSL10-Beispiel).</span><span class="sxs-lookup"><span data-stu-id="f54fc-116">Here's an example of compiling an effect file (from the BasicHLSL10 sample).</span></span>


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a><span data-ttu-id="f54fc-117">Includes</span><span class="sxs-lookup"><span data-stu-id="f54fc-117">Includes</span></span>

<span data-ttu-id="f54fc-118">Ein Parameter ist eine include-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f54fc-118">One parameter is an include interface.</span></span> <span data-ttu-id="f54fc-119">Generieren Sie eine dieser Dateien, wenn Sie ein angepasstes Verhalten beim Lesen einer Includedatei einschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="f54fc-119">Generate one of these if you want to include a customized behavior when reading an include file.</span></span> <span data-ttu-id="f54fc-120">Dieses benutzerdefinierte Verhalten wird jedes Mal ausgeführt, wenn ein Effekt (der den Include-Zeiger verwendet) erstellt wird oder wenn ein Effekt (der den Include-Zeiger verwendet) kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="f54fc-120">This custom behavior is executed each time an effect (that uses the include pointer) is created or when an effect (that uses the include pointer) is compiled.</span></span> <span data-ttu-id="f54fc-121">Um das angepasste include-Verhalten zu implementieren, leiten Sie eine Klasse von der include-Schnittstelle ab</span><span class="sxs-lookup"><span data-stu-id="f54fc-121">To implement customized include behavior, derive a class from the Include interface.</span></span> <span data-ttu-id="f54fc-122">Dies bietet zwei Methoden für die Klasse: Öffnen und schließen.</span><span class="sxs-lookup"><span data-stu-id="f54fc-122">This provides your class two methods: Open and Close.</span></span> <span data-ttu-id="f54fc-123">Implementieren Sie das benutzerdefinierte Verhalten in den Open-und Close-Methoden.</span><span class="sxs-lookup"><span data-stu-id="f54fc-123">Implement the custom behavior in the Open and Close methods.</span></span>

## <a name="macros"></a><span data-ttu-id="f54fc-124">Makros</span><span class="sxs-lookup"><span data-stu-id="f54fc-124">Macros</span></span>

<span data-ttu-id="f54fc-125">Die Effekt Kompilierung kann auch einen Zeiger auf Makros annehmen, die an anderer Stelle definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f54fc-125">Effect compilation can also take a pointer to macros that are defined elsewhere.</span></span> <span data-ttu-id="f54fc-126">Nehmen Sie beispielsweise an, dass Sie den Effekt in BasicHLSL10 ändern, um zwei Makros zu verwenden: NULL und eins.</span><span class="sxs-lookup"><span data-stu-id="f54fc-126">For example, suppose you were to modify the effect in BasicHLSL10, to use two macros: zero and one.</span></span> <span data-ttu-id="f54fc-127">Der Effekt Code, der die beiden Makros verwendet, wird hier dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f54fc-127">The effect code that uses the two macros is shown here.</span></span>


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



<span data-ttu-id="f54fc-128">Hier ist die Deklaration für die beiden Makros.</span><span class="sxs-lookup"><span data-stu-id="f54fc-128">Here is the declaration for the two macros.</span></span>


```
D3D_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



<span data-ttu-id="f54fc-129">Die Makros sind ein mit Null endendes Array von Makros. Dabei ist jedes Makro mit einer [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="f54fc-129">The macros are a NULL terminated array of macros; where each macro is defined with a [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) struct.</span></span>

<span data-ttu-id="f54fc-130">Ändern Sie abschließend den Kompilierungs Effekt-Befehl, um einen Zeiger auf die Makros zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="f54fc-130">Lastly, modify the compile effect call to take a pointer to the macros.</span></span>


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a><span data-ttu-id="f54fc-131">HLSL-shaderflags</span><span class="sxs-lookup"><span data-stu-id="f54fc-131">HLSL Shader Flags</span></span>

<span data-ttu-id="f54fc-132">Shaderflags geben Shader-Einschränkungen für den HLSL-Compiler an.</span><span class="sxs-lookup"><span data-stu-id="f54fc-132">Shader flags specify shader constraints to the HLSL compiler.</span></span> <span data-ttu-id="f54fc-133">Diese Flags wirken sich auf den vom Shader-Compiler generierten Code aus, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="f54fc-133">These flags impact the code generated by the shader compiler including:</span></span>

-   <span data-ttu-id="f54fc-134">Überlegungen zur Größe: Optimieren Sie den Code.</span><span class="sxs-lookup"><span data-stu-id="f54fc-134">Size considerations: optimize the code.</span></span>
-   <span data-ttu-id="f54fc-135">Überlegungen zum Debuggen: einschließlich Debuginformationen, verhindern der Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="f54fc-135">Debug considerations: including debug information, preventing flow control.</span></span>
-   <span data-ttu-id="f54fc-136">Überlegungen zur Hardware: das Kompilierungs Ziel und ob ein Shader auf Legacy Hardware ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f54fc-136">Hardware considerations: the compile target and whether or not a shader can run on legacy hardware.</span></span>

<span data-ttu-id="f54fc-137">Im Allgemeinen können diese Flags logisch kombiniert werden, vorausgesetzt, dass Sie nicht zwei widersprüchliche Merkmale angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="f54fc-137">In general, these flags can be logically combined, assuming you have not specified two conflicting characteristics.</span></span> <span data-ttu-id="f54fc-138">Eine Auflistung der Flags finden Sie unter [Effect-Konstanten (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f54fc-138">For a listing of the flags see [Effect Constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span></span>

## <a name="fx-flags"></a><span data-ttu-id="f54fc-139">FX-Flags</span><span class="sxs-lookup"><span data-stu-id="f54fc-139">FX Flags</span></span>

<span data-ttu-id="f54fc-140">Diese Flags werden beim Erstellen eines Effekts verwendet, um entweder das Kompilierungs Verhalten oder das Lauf Zeit Effekt Verhalten zu definieren.</span><span class="sxs-lookup"><span data-stu-id="f54fc-140">These flags used when creating an effect to define either compilation behavior or runtime effect behavior.</span></span> <span data-ttu-id="f54fc-141">Eine Auflistung der Flags finden Sie unter [Effect-Konstanten (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f54fc-141">For a listing of the flags see [Effect Constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span></span>

## <a name="checking-errors"></a><span data-ttu-id="f54fc-142">Überprüfen von Fehlern</span><span class="sxs-lookup"><span data-stu-id="f54fc-142">Checking Errors</span></span>

<span data-ttu-id="f54fc-143">Wenn während der Kompilierung ein Fehler auftritt, gibt die API eine Schnittstelle zurück, die die vom Effekt Compiler zurückgegebenen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="f54fc-143">If during compilation, an error occurs, the API returns an interface which contains the errors returned from the effect compiler.</span></span> <span data-ttu-id="f54fc-144">Diese Schnittstelle wird als ID3D10Blob bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f54fc-144">This interface is called ID3D10Blob.</span></span> <span data-ttu-id="f54fc-145">Er ist jedoch nicht direkt lesbar. durch Zurückgeben eines Zeigers auf den Puffer, der die Daten enthält (eine Zeichenfolge), können alle Kompilierungsfehler angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f54fc-145">It is not directly readable, however, by returning a pointer to the buffer that contains the data (which is a string), you can see any compilation errors.</span></span>

<span data-ttu-id="f54fc-146">In diesem Beispiel wurde ein Fehler in die basichlsl. FX-Auswirkung eingefügt, indem die erste Variablen Deklaration zweimal kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f54fc-146">In this example, an error was introduced into the BasicHLSL.fx effect by copying the first variable declaration twice.</span></span>


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



<span data-ttu-id="f54fc-147">Dieser Fehler hat bewirkt, dass der Compiler den folgenden Fehler zurückgibt, wie im folgenden Screenshot des Fensters Überwachen in Microsoft Visual Studio gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f54fc-147">This error caused the compiler to return the following error, as shown in the following screen shot of the watch window in Microsoft Visual Studio.</span></span>

![Screenshot des Fensters "Überwachen von Visual Studio"](images/effect-compile-errors-2.jpg)

<span data-ttu-id="f54fc-149&quot;>Da der Fehler in einem LPVOID-Zeiger zurückgegeben wird, wandeln Sie ihn in eine Zeichenfolge im Überwachungs Fenster um.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f54fc-149&quot;>Since the error is returned in a LPVOID pointer, cast it to a character string in the watch window.</span></span>

<span data-ttu-id=&quot;f54fc-150&quot;>Hier ist der Code, mit dem der Fehler aus der fehlgeschlagenen Kompilierung zurückgegeben wird.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f54fc-150&quot;>Here is the code used to return the error from the failed compile.</span></span>


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3D10Blob* l_pBlob_Effect = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L&quot;BasicHLSL10.fx" );
hr = D3DX10CompileEffectFromFile( str, NULL, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors );

LPVOID l_pError = NULL;
if( l_pBlob_Errors )
{
    l_pError = l_pBlob_Errors->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a><span data-ttu-id="f54fc-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f54fc-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f54fc-152">Rendern eines Effekts (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f54fc-152">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



