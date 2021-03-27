---
title: Kompilieren eines Effekts (Direct3D 11)
description: Nachdem ein Effekt erstellt wurde, besteht der nächste Schritt darin, den Code zu kompilieren, um auf Syntax Probleme zu überprüfen.
ms.assetid: 7624d55e-6466-4156-8f31-30f0d25a2883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3df304a7b657af19984008bd90a1be4bfe5219c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948858"
---
# <a name="compile-an-effect-direct3d-11"></a><span data-ttu-id="a6caf-103">Kompilieren eines Effekts (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="a6caf-103">Compile an Effect (Direct3D 11)</span></span>

<span data-ttu-id="a6caf-104">Nachdem ein Effekt erstellt wurde, besteht der nächste Schritt darin, den Code zu kompilieren, um auf Syntax Probleme zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a6caf-104">After an effect has been authored, the next step is to compile the code to check for syntax problems.</span></span>

<span data-ttu-id="a6caf-105">Dies erreichen Sie, indem Sie eine der Kompilierungs-APIs aufrufen ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md)oder [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ).</span><span class="sxs-lookup"><span data-stu-id="a6caf-105">You do so by calling one of the compile APIs ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md), or [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ).</span></span> <span data-ttu-id="a6caf-106">Diese APIs rufen die Auswirkung-Compilerfxc.exe auf, die HLSL-Code kompiliert.</span><span class="sxs-lookup"><span data-stu-id="a6caf-106">These APIs invoke the effect compiler fxc.exe, which compiles HLSL code.</span></span> <span data-ttu-id="a6caf-107">Aus diesem Grund sieht die Syntax für Code in einem Effekt sehr ähnlich wie der HLSL-Code aus.</span><span class="sxs-lookup"><span data-stu-id="a6caf-107">This is why the syntax for code in an effect looks very much like HLSL code.</span></span> <span data-ttu-id="a6caf-108">(Es gibt einige Ausnahmen, die zu einem späteren Zeitpunkt behandelt werden.)</span><span class="sxs-lookup"><span data-stu-id="a6caf-108">(There are a few exceptions that will be handled later).</span></span> <span data-ttu-id="a6caf-109">Der Effekt Compiler/HLSL-Compiler (fxc.exe) steht im SDK im Ordner Hilfsprogramme zur Verfügung, damit shaderer (oder Effekte) Offline kompiliert werden können, wenn Sie auswählen.</span><span class="sxs-lookup"><span data-stu-id="a6caf-109">The effect compiler/hlsl compiler, fxc.exe, is available in the SDK in the utilities folder so that shaders (or effects) can be compiled offline if you choose.</span></span> <span data-ttu-id="a6caf-110">Weitere Informationen finden Sie in der Dokumentation zum Ausführen des Compilers von der Befehlszeile aus.</span><span class="sxs-lookup"><span data-stu-id="a6caf-110">See the documentation for running the compiler from the command line.</span></span>

-   [<span data-ttu-id="a6caf-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a6caf-111">Example</span></span>](#example)
-   [<span data-ttu-id="a6caf-112">Includes</span><span class="sxs-lookup"><span data-stu-id="a6caf-112">Includes</span></span>](#includes)
-   [<span data-ttu-id="a6caf-113">Suchen nach Includedateien</span><span class="sxs-lookup"><span data-stu-id="a6caf-113">Searching for Include Files</span></span>](#searching-for-include-files)
-   [<span data-ttu-id="a6caf-114">Makros</span><span class="sxs-lookup"><span data-stu-id="a6caf-114">Macros</span></span>](#macros)
-   [<span data-ttu-id="a6caf-115">HLSL-shaderflags</span><span class="sxs-lookup"><span data-stu-id="a6caf-115">HLSL Shader Flags</span></span>](#hlsl-shader-flags)
-   [<span data-ttu-id="a6caf-116">FX-Flags</span><span class="sxs-lookup"><span data-stu-id="a6caf-116">FX Flags</span></span>](#fx-flags)
-   [<span data-ttu-id="a6caf-117">Überprüfen von Fehlern</span><span class="sxs-lookup"><span data-stu-id="a6caf-117">Checking Errors</span></span>](#checking-errors)
-   [<span data-ttu-id="a6caf-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6caf-118">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="a6caf-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a6caf-119">Example</span></span>

<span data-ttu-id="a6caf-120">Im folgenden finden Sie ein Beispiel für das Kompilieren einer Effekt Datei.</span><span class="sxs-lookup"><span data-stu-id="a6caf-120">Here's an example of compiling an effect file.</span></span>


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, NULL, &pBlob, &pErrorBlob, NULL );
```



## <a name="includes"></a><span data-ttu-id="a6caf-121">Includes</span><span class="sxs-lookup"><span data-stu-id="a6caf-121">Includes</span></span>

<span data-ttu-id="a6caf-122">Ein Parameter der Compile-APIs ist eine include-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a6caf-122">One parameter of the compile APIs is an include interface.</span></span> <span data-ttu-id="a6caf-123">Generieren Sie eine dieser Optionen, wenn Sie ein angepasstes Verhalten einschließen möchten, wenn der Compiler eine include-Datei liest.</span><span class="sxs-lookup"><span data-stu-id="a6caf-123">Generate one of these if you want to include a customized behavior when the compiler reads an include file.</span></span> <span data-ttu-id="a6caf-124">Der Compiler führt dieses benutzerdefinierte Verhalten jedes Mal aus, wenn er einen Effekt erstellt oder kompiliert (der den Include-Zeiger verwendet).</span><span class="sxs-lookup"><span data-stu-id="a6caf-124">The compiler executes this custom behavior each time it creates or compiles an effect (that uses the include pointer).</span></span> <span data-ttu-id="a6caf-125">Um das angepasste include-Verhalten zu implementieren, leiten Sie eine Klasse von der [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) -Schnittstelle ab</span><span class="sxs-lookup"><span data-stu-id="a6caf-125">To implement customized include behavior, derive a class from the [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) interface.</span></span> <span data-ttu-id="a6caf-126">Dadurch wird die-Klasse mit zwei Methoden bereitstellt: [**Öffnen**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) und [**Schließen**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close).</span><span class="sxs-lookup"><span data-stu-id="a6caf-126">This provides your class with two methods: [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) and [**Close**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close).</span></span> <span data-ttu-id="a6caf-127">Implementieren Sie das benutzerdefinierte Verhalten in diesen Methoden.</span><span class="sxs-lookup"><span data-stu-id="a6caf-127">Implement the custom behavior in these methods.</span></span>

## <a name="searching-for-include-files"></a><span data-ttu-id="a6caf-128">Suchen nach Includedateien</span><span class="sxs-lookup"><span data-stu-id="a6caf-128">Searching for Include Files</span></span>

<span data-ttu-id="a6caf-129">Der Zeiger, den der Compiler im *PPARa entdata* -Parameter an die [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) -Methode Ihres include-Handlers übergibt, verweist möglicherweise nicht auf den Container, der die Includedatei enthält \# , die der Compiler zum Kompilieren Ihres shadercodes benötigt.</span><span class="sxs-lookup"><span data-stu-id="a6caf-129">The pointer that the compiler passes in the *pParentData* parameter to your include handler's [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) method might not point to the container that includes the \#include file that the compiler needs to compile your shader code.</span></span> <span data-ttu-id="a6caf-130">Das heißt, der Compiler kann **null** in *pparameentdata* übergeben.</span><span class="sxs-lookup"><span data-stu-id="a6caf-130">That is, the compiler might pass **NULL** in *pParentData*.</span></span> <span data-ttu-id="a6caf-131">Daher wird empfohlen, dass der include-Handler eine eigene Liste von include-Speicherorten für Inhalt durchsucht.</span><span class="sxs-lookup"><span data-stu-id="a6caf-131">Therefore, we recommend that your include handler search its own list of include locations for content.</span></span> <span data-ttu-id="a6caf-132">Der include-Handler kann neue include-Speicherorte dynamisch hinzufügen, da diese Speicherorte in Aufrufen der **geöffneten** Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="a6caf-132">Your include handler can dynamically add new include locations as it receives those locations in calls to its **Open** method.</span></span>

<span data-ttu-id="a6caf-133">Nehmen Sie im folgenden Beispiel an, dass die Includedateien des Shader-Codes beide im Verzeichnis " *Somewhere else* " gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a6caf-133">In the following example, suppose that the shader code's include files are both stored in the *somewhereelse* directory.</span></span> <span data-ttu-id="a6caf-134">Wenn der Compiler die [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) -Methode des include-Handlers aufruft, um den Inhalt von *Somewhere \\ foo. h* zu öffnen und zu lesen, kann der include-Handler den Speicherort des Verzeichnisses " **Somewhere else** " speichern.</span><span class="sxs-lookup"><span data-stu-id="a6caf-134">When the compiler calls the include handler's [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) method to open and read the contents of *somewhereelse\\foo.h*, the include handler can save the location of the **somewhereelse** directory.</span></span> <span data-ttu-id="a6caf-135">Wenn der Compiler später die **Open** -Methode des includehandlers aufruft, um den Inhalt von *Bar. h* zu öffnen und zu lesen, kann der include-Handler automatisch im Verzeichnis " *Somewhere else* " nach " *Bar. h*" suchen.</span><span class="sxs-lookup"><span data-stu-id="a6caf-135">Later, when the compiler calls the include handler's **Open** method to open and read the contents of *bar.h*, the include handler can automatically search in the *somewhereelse* directory for *bar.h*.</span></span>


```
Main.hlsl:
#include "somewhereelse\foo.h"

Foo.h:
#include "bar.h"
```



## <a name="macros"></a><span data-ttu-id="a6caf-136">Makros</span><span class="sxs-lookup"><span data-stu-id="a6caf-136">Macros</span></span>

<span data-ttu-id="a6caf-137">Die Effekt Kompilierung kann auch einen Zeiger auf Makros annehmen, die an anderer Stelle definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a6caf-137">Effect compilation can also take a pointer to macros that are defined elsewhere.</span></span> <span data-ttu-id="a6caf-138">Nehmen Sie beispielsweise an, Sie möchten die Auswirkung in BasicHLSL10 ändern, um zwei Makros zu verwenden: NULL und eins.</span><span class="sxs-lookup"><span data-stu-id="a6caf-138">For example, suppose you want to modify the effect in BasicHLSL10, to use two macros: zero and one.</span></span> <span data-ttu-id="a6caf-139">Der Effekt Code, der die beiden Makros verwendet, wird hier dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a6caf-139">The effect code that uses the two macros is shown here.</span></span>


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



<span data-ttu-id="a6caf-140">Hier ist die Deklaration für die beiden Makros.</span><span class="sxs-lookup"><span data-stu-id="a6caf-140">Here is the declaration for the two macros.</span></span>


```
D3D10_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



<span data-ttu-id="a6caf-141">Die Makros sind ein mit Null endendes Array von Makros. , wobei jedes Makro mithilfe einer d3d10- [**\_ Shader- \_ Makro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) Struktur definiert wird.</span><span class="sxs-lookup"><span data-stu-id="a6caf-141">The macros are a NULL-terminated array of macros; where each macro is defined by using a [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) struct.</span></span>

<span data-ttu-id="a6caf-142">Ändern Sie den Kompilierungs Effekt-Befehl, um einen Zeiger auf die Makros zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="a6caf-142">Modify the compile effect call to take a pointer to the macros.</span></span>


```
D3DX11CompileFromFile( str, Shader_Macros, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );    
```



## <a name="hlsl-shader-flags"></a><span data-ttu-id="a6caf-143">HLSL-shaderflags</span><span class="sxs-lookup"><span data-stu-id="a6caf-143">HLSL Shader Flags</span></span>

<span data-ttu-id="a6caf-144">Shaderflags geben Shader-Einschränkungen für den HLSL-Compiler an.</span><span class="sxs-lookup"><span data-stu-id="a6caf-144">Shader flags specify shader constraints to the HLSL compiler.</span></span> <span data-ttu-id="a6caf-145">Diese Flags wirken sich auf den vom Shader-Compiler generierten Code auf folgende Weise aus:</span><span class="sxs-lookup"><span data-stu-id="a6caf-145">These flags affect the code generated by the shader compiler in the following ways:</span></span>

-   <span data-ttu-id="a6caf-146">Optimieren Sie die Codegröße.</span><span class="sxs-lookup"><span data-stu-id="a6caf-146">Optimize the code size.</span></span>
-   <span data-ttu-id="a6caf-147">Einschließlich der Debuginformationen, die die Fluss Steuerung verhindern.</span><span class="sxs-lookup"><span data-stu-id="a6caf-147">Including debug information, which prevents flow control.</span></span>
-   <span data-ttu-id="a6caf-148">Wirkt sich auf das Kompilierungs Ziel und darauf aus, ob ein Shader auf älterer Hardware ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a6caf-148">Affects the compile target and whether a shader can run on legacy hardware.</span></span>

<span data-ttu-id="a6caf-149">Diese Flags können logisch kombiniert werden, wenn Sie nicht zwei widersprüchliche Merkmale angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="a6caf-149">These flags can be logically combined if you have not specified two conflicting characteristics.</span></span> <span data-ttu-id="a6caf-150">Eine Auflistung der Flags finden Sie unter [d3d10 \_ Shader Konstanten](/windows/desktop/direct3d10/d3d10-shader).</span><span class="sxs-lookup"><span data-stu-id="a6caf-150">For a listing of the flags see [D3D10\_SHADER Constants](/windows/desktop/direct3d10/d3d10-shader).</span></span>

## <a name="fx-flags"></a><span data-ttu-id="a6caf-151">FX-Flags</span><span class="sxs-lookup"><span data-stu-id="a6caf-151">FX Flags</span></span>

<span data-ttu-id="a6caf-152">Verwenden Sie diese Flags bei der Erstellung eines Effekts, um entweder das Kompilierungs Verhalten oder das Lauf Zeit Effekt Verhalten zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a6caf-152">Use these flags when you create an effect to define either compilation behavior or runtime effect behavior.</span></span> <span data-ttu-id="a6caf-153">Eine Auflistung der Flags finden Sie unter [d3d10 \_ Effect Konstanten](/windows/desktop/direct3d10/d3d10-effect).</span><span class="sxs-lookup"><span data-stu-id="a6caf-153">For a listing of the flags see [D3D10\_EFFECT Constants](/windows/desktop/direct3d10/d3d10-effect).</span></span>

## <a name="checking-errors"></a><span data-ttu-id="a6caf-154">Überprüfen von Fehlern</span><span class="sxs-lookup"><span data-stu-id="a6caf-154">Checking Errors</span></span>

<span data-ttu-id="a6caf-155">Wenn während der Kompilierung ein Fehler auftritt, gibt die API eine Schnittstelle zurück, die die Fehler vom Effekt Compiler enthält.</span><span class="sxs-lookup"><span data-stu-id="a6caf-155">If during compilation an error occurs, the API returns an interface that contains the errors from the effect compiler.</span></span> <span data-ttu-id="a6caf-156">Diese Schnittstelle wird als [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a6caf-156">This interface is called [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)).</span></span> <span data-ttu-id="a6caf-157">Er ist nicht direkt lesbar. Wenn Sie jedoch einen Zeiger auf den Puffer zurückgeben, der die Daten enthält (eine Zeichenfolge), können Sie alle Kompilierungsfehler sehen.</span><span class="sxs-lookup"><span data-stu-id="a6caf-157">It is not directly readable; however, by returning a pointer to the buffer that contains the data (which is a string), you can see any compilation errors.</span></span>

<span data-ttu-id="a6caf-158">Dieses Beispiel enthält einen Fehler in basichlsl. FX, die erste Variablen Deklaration wird zweimal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6caf-158">This example contains an error in the BasicHLSL.fx, the first variable declaration occurs twice.</span></span>


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



<span data-ttu-id="a6caf-159">Dieser Fehler bewirkt, dass der Compiler den folgenden Fehler zurückgibt, wie im folgenden Screenshot der Überwachungsfenster in Microsoft Visual Studio gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6caf-159">This error causes the compiler to return the following error, as shown in the following screen shot of the Watch window in Microsoft Visual Studio.</span></span>

![Screenshot des Fensters "Visual Studio-Überwachung" mit dem Fehler "0x01997sb8"](images/effect-compile-errors-2.jpg)

<span data-ttu-id="a6caf-161">Da der Compiler den Fehler in einem LPVOID-Zeiger zurückgibt, wandeln Sie ihn in eine Zeichenfolge in der Überwachungsfenster um.</span><span class="sxs-lookup"><span data-stu-id="a6caf-161">Because the compiler returns the error in a LPVOID pointer, cast it to a character string in the Watch window.</span></span>

<span data-ttu-id="a6caf-162">Hier ist der Code angegeben, der den Fehler von der fehlgeschlagenen Kompilierung zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a6caf-162">Here is the code that returns the error from the failed compile.</span></span>


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3DBlob*   l_pBlob_Effect = NULL;
ID3DBlob*   l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );      

LPVOID l_pError = NULL;
if( pErrorBlob )
{
    l_pError = pErrorBlob->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a><span data-ttu-id="a6caf-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6caf-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6caf-164">Rendern eines Effekts (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="a6caf-164">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 