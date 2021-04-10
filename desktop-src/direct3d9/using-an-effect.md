---
description: Auf dieser Seite erfahren Sie, wie Sie einen Effekt generieren und verwenden.
ms.assetid: d9fdafed-5958-4995-a1b5-8881feca1291
title: Verwenden eines Effekts (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1170fde625e5eee5e9665f0759d302b5f5450a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125575"
---
# <a name="using-an-effect-direct3d-9"></a><span data-ttu-id="3ed06-103">Verwenden eines Effekts (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3ed06-103">Using an Effect (Direct3D 9)</span></span>

<span data-ttu-id="3ed06-104">Auf dieser Seite erfahren Sie, wie Sie einen Effekt generieren und verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-104">This page will show you how to generate and use an effect.</span></span> <span data-ttu-id="3ed06-105">Die behandelten Themen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3ed06-105">The topics covered include how to:</span></span>

-   [<span data-ttu-id="3ed06-106">Erstellen eines Effekts</span><span class="sxs-lookup"><span data-stu-id="3ed06-106">Create an Effect</span></span>](#create-an-effect)
-   [<span data-ttu-id="3ed06-107">Einen Effekt Rendering</span><span class="sxs-lookup"><span data-stu-id="3ed06-107">Render an Effect</span></span>](#render-an-effect)
-   [<span data-ttu-id="3ed06-108">Verwenden der Semantik zum Suchen von Effekt Parametern</span><span class="sxs-lookup"><span data-stu-id="3ed06-108">Use Semantics to Find Effect Parameters</span></span>](#use-semantics-to-find-effect-parameters)
-   [<span data-ttu-id="3ed06-109">Verwenden von Handles zum effizienten erhalten und Festlegen von Parametern</span><span class="sxs-lookup"><span data-stu-id="3ed06-109">Use Handles to Get and Set Parameters Efficiently</span></span>](#use-handles-to-get-and-set-parameters-efficiently)
-   [<span data-ttu-id="3ed06-110">Hinzufügen von Parameter Informationen mit Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="3ed06-110">Add Parameter Information with Annotations</span></span>](#add-parameter-information-with-annotations)
-   [<span data-ttu-id="3ed06-111">Parameter für Freigabe Effekte</span><span class="sxs-lookup"><span data-stu-id="3ed06-111">Share Effect Parameters</span></span>](#share-effect-parameters)
-   [<span data-ttu-id="3ed06-112">Einen Effekt Offline kompilieren</span><span class="sxs-lookup"><span data-stu-id="3ed06-112">Compile an Effect Offline</span></span>](#compile-an-effect-offline)
-   [<span data-ttu-id="3ed06-113">Verbessern der Leistung durch preshaders</span><span class="sxs-lookup"><span data-stu-id="3ed06-113">Improve Performance with Preshaders</span></span>](#improve-performance-with-preshaders)
-   [<span data-ttu-id="3ed06-114">Verwenden von Parameter Blöcken zum Verwalten von Effekt Parametern</span><span class="sxs-lookup"><span data-stu-id="3ed06-114">Use Parameter Blocks to Manage Effect Parameters</span></span>](#use-parameter-blocks-to-manage-effect-parameters)

## <a name="create-an-effect"></a><span data-ttu-id="3ed06-115">Erstellen eines Effekts</span><span class="sxs-lookup"><span data-stu-id="3ed06-115">Create an Effect</span></span>

<span data-ttu-id="3ed06-116">Hier ist ein Beispiel für das Erstellen eines Effekts, der aus dem [basichlsl-Beispiel](../directx-sdk--august-2009-.md)stammt.</span><span class="sxs-lookup"><span data-stu-id="3ed06-116">Here is an example of creating an effect taken from the [BasicHLSL Sample](../directx-sdk--august-2009-.md).</span></span> <span data-ttu-id="3ed06-117">Der Effekt Erstellungs Code zum Erstellen eines debugshaders ist von **onkreatedevice**:</span><span class="sxs-lookup"><span data-stu-id="3ed06-117">The effect creation code for creating a debug shader is from **OnCreateDevice**:</span></span>


```
ID3DXEffect* g_pEffect = NULL;
DWORD dwShaderFlags = 0;

    dwShaderFlags |= D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_NO_PRESHADER;

    // Read the D3DX effect file
    WCHAR str[MAX_PATH];
    DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL.fx" );

    D3DXCreateEffectFromFile( 
        pd3dDevice, 
        str, 
        NULL, // CONST D3DXMACRO* pDefines,
        NULL, // LPD3DXINCLUDE pInclude,
        dwShaderFlags, 
        NULL, // LPD3DXEFFECTPOOL pPool,
        &g_pEffect, 
        NULL );
```



<span data-ttu-id="3ed06-118">Diese Funktion übernimmt die folgenden Argumente:</span><span class="sxs-lookup"><span data-stu-id="3ed06-118">This function takes these arguments:</span></span>

-   <span data-ttu-id="3ed06-119">Das Gerät.</span><span class="sxs-lookup"><span data-stu-id="3ed06-119">The device.</span></span>
-   <span data-ttu-id="3ed06-120">Der Dateiname der Effekt Datei.</span><span class="sxs-lookup"><span data-stu-id="3ed06-120">The file name of the effect file.</span></span>
-   <span data-ttu-id="3ed06-121">Ein Zeiger auf eine mit NULL endende Liste von \# definiert, die beim Durchführen des Shaders verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ed06-121">A pointer to a NULL-terminated list of \#defines, to be used while parsing the shader.</span></span>
-   <span data-ttu-id="3ed06-122">Ein optionaler Zeiger auf einen Benutzer geschriebenen include-Handler.</span><span class="sxs-lookup"><span data-stu-id="3ed06-122">An optional pointer to a user-written include handler.</span></span> <span data-ttu-id="3ed06-123">Der-Handler wird vom Prozessor aufgerufen, wenn er eine include auflösen muss \# .</span><span class="sxs-lookup"><span data-stu-id="3ed06-123">The handler is called by the processor whenever it needs to resolve a \#include.</span></span>
-   <span data-ttu-id="3ed06-124">Ein Shader-kompilierungsflag, das die compilerhinweise darüber gibt, wie der Shader verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ed06-124">A shader compile flag that gives the compiler hints about how the shader will be used.</span></span> <span data-ttu-id="3ed06-125">Die Optionen lauten:</span><span class="sxs-lookup"><span data-stu-id="3ed06-125">The options include:</span></span>
    -   <span data-ttu-id="3ed06-126">Die Validierung wird übersprungen, wenn bekannte gute Shader kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-126">Skipping validation, if known good shaders are being compiled.</span></span>
    -   <span data-ttu-id="3ed06-127">Die Optimierung wird übersprungen (manchmal verwendet, wenn Optimierungen das Debuggen erschweren).</span><span class="sxs-lookup"><span data-stu-id="3ed06-127">Skipping optimization (sometimes used when optimizations make debugging harder).</span></span>
    -   <span data-ttu-id="3ed06-128">Anfordern von Debuginformationen, die in den Shader eingeschlossen werden sollen, damit Sie gedebuggt werden können.</span><span class="sxs-lookup"><span data-stu-id="3ed06-128">Requesting debug information to be included in the shader so it can be debugged.</span></span>
-   <span data-ttu-id="3ed06-129">Der Effekt Pool.</span><span class="sxs-lookup"><span data-stu-id="3ed06-129">The effect pool.</span></span> <span data-ttu-id="3ed06-130">Wenn mehr als ein Effekt denselben Speicherpool Zeiger verwendet, werden die globalen Variablen in den Effekten gemeinsam genutzt.</span><span class="sxs-lookup"><span data-stu-id="3ed06-130">If more than one effect uses the same memory pool pointer, the global variables in the effects are shared with each other.</span></span> <span data-ttu-id="3ed06-131">Wenn Sie keine Auswirkung-Variablen freigeben müssen, kann der Speicherpool auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-131">If there is no need to share effect variables, the memory pool can be set to **NULL**.</span></span>
-   <span data-ttu-id="3ed06-132">Ein Zeiger auf den neuen Effekt.</span><span class="sxs-lookup"><span data-stu-id="3ed06-132">A pointer to the new effect.</span></span>
-   <span data-ttu-id="3ed06-133">Ein Zeiger auf einen Puffer, an den Validierungs Fehler gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3ed06-133">A pointer to a buffer to which validation errors can be sent.</span></span> <span data-ttu-id="3ed06-134">In diesem Beispiel wurde der-Parameter auf **null** festgelegt und nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3ed06-134">In this example, the parameter was set to **NULL** and not used.</span></span>

> [!Note]  
> <span data-ttu-id="3ed06-135">Ab dem SDK vom Dezember 2006 ist der DirectX 10 HLSL-Compiler nun der Standard Compiler in DirectX 9 und DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="3ed06-135">Beginning with the December 2006 SDK, the DirectX 10 HLSL compiler is now the default compiler in both DirectX 9 and DirectX 10.</span></span> <span data-ttu-id="3ed06-136">Ausführliche Informationen finden Sie unter [Effect-Compiler-Tool](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="3ed06-136">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

 

## <a name="render-an-effect"></a><span data-ttu-id="3ed06-137">Einen Effekt Rendering</span><span class="sxs-lookup"><span data-stu-id="3ed06-137">Render an Effect</span></span>

<span data-ttu-id="3ed06-138">Die Abfolge der Aufrufe zum Anwenden des Wirkungs Zustands auf ein Gerät lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3ed06-138">The sequence of calls for applying effect state to a device is:</span></span>

-   <span data-ttu-id="3ed06-139">[**ID3DXEffect:: begin**](id3dxeffect--begin.md) legt die aktive Technik fest.</span><span class="sxs-lookup"><span data-stu-id="3ed06-139">[**ID3DXEffect::Begin**](id3dxeffect--begin.md) sets the active technique.</span></span>
-   <span data-ttu-id="3ed06-140">[**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md) legt den aktiven Durchlauf fest.</span><span class="sxs-lookup"><span data-stu-id="3ed06-140">[**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) sets the active pass.</span></span>
-   <span data-ttu-id="3ed06-141">[**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) aktualisiert Änderungen an beliebigen Set-aufrufen im Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="3ed06-141">[**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) updates changes to any set calls in the pass.</span></span> <span data-ttu-id="3ed06-142">Dies sollte vor einem Draw-Aufruf aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-142">This should be called before any draw call.</span></span>
-   <span data-ttu-id="3ed06-143">[**ID3DXEffect:: endpass**](id3dxeffect--endpass.md) beendet einen Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="3ed06-143">[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) ends a pass.</span></span>
-   <span data-ttu-id="3ed06-144">[**ID3DXEffect:: End**](id3dxeffect--end.md) beendet die aktive Technik.</span><span class="sxs-lookup"><span data-stu-id="3ed06-144">[**ID3DXEffect::End**](id3dxeffect--end.md) ends the active technique.</span></span>

<span data-ttu-id="3ed06-145">Der Effekt-Rendering-Code ist auch einfacher als der entsprechende Rendering-Code.</span><span class="sxs-lookup"><span data-stu-id="3ed06-145">Effect render code is also simpler than the corresponding render code without an effect.</span></span> <span data-ttu-id="3ed06-146">Hier ist der Rendering-Code mit einem Effekt:</span><span class="sxs-lookup"><span data-stu-id="3ed06-146">Here's the render code with an effect:</span></span>


```
// Apply the technique contained in the effect 
g_pEffect->Begin(&cPasses, 0);

for (iPass = 0; iPass < cPasses; iPass++)
{
    g_pEffect->BeginPass(iPass);

    // Only call CommitChanges if any state changes have happened
    // after BeginPass is called
    g_pEffect->CommitChanges();

    // Render the mesh with the applied technique
    g_pMesh->DrawSubset(0);

    g_pEffect->EndPass();
}
g_pEffect->End();
```



<span data-ttu-id="3ed06-147">Die Renderschleife besteht darin, den Effekt abzufragen, um zu sehen, wie viele Pass Sie enthält, und dann alle Durchgänge für eine Technik abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3ed06-147">The render loop consists of querying the effect to see how many passes it contains, and then calling all the passes for a technique.</span></span> <span data-ttu-id="3ed06-148">Die Renderschleife kann erweitert werden, um mehrere Techniken aufzurufen, die jeweils mehrere Durchgänge haben.</span><span class="sxs-lookup"><span data-stu-id="3ed06-148">The render loop could be expanded to call multiple techniques, each with multiple passes.</span></span>

## <a name="use-semantics-to-find-effect-parameters"></a><span data-ttu-id="3ed06-149">Verwenden der Semantik zum Suchen von Effekt Parametern</span><span class="sxs-lookup"><span data-stu-id="3ed06-149">Use Semantics to Find Effect Parameters</span></span>

<span data-ttu-id="3ed06-150">Eine Semantik ist ein Bezeichner, der an einen Effektparameter angefügt wird, um einer Anwendung das Suchen nach dem Parameter zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3ed06-150">A semantic is an identifier that is attached to an effect parameter to allow an application to search for the parameter.</span></span> <span data-ttu-id="3ed06-151">Ein Parameter kann höchstens über eine Semantik verfügen.</span><span class="sxs-lookup"><span data-stu-id="3ed06-151">A parameter can have at most one semantic.</span></span> <span data-ttu-id="3ed06-152">Die Semantik befindet sich nach einem Doppelpunkt (:) nach dem Parameternamen.</span><span class="sxs-lookup"><span data-stu-id="3ed06-152">The semantic is located following a colon (:) after the parameter name.</span></span> <span data-ttu-id="3ed06-153">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3ed06-153">For instance:</span></span>


```
float4x4 matWorldViewProj : WORLDVIEWPROJ;
```



<span data-ttu-id="3ed06-154">Wenn Sie die globale Variable Auswirkung ohne Verwendung einer Semantik deklariert haben, sieht Sie stattdessen wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="3ed06-154">If you declared the effect global variable without using a semantic, it would look like this instead:</span></span>


```
float4x4 matWorldViewProj;
```



<span data-ttu-id="3ed06-155">Die Effect-Schnittstelle kann eine Semantik verwenden, um ein Handle für einen bestimmten Effektparameter zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3ed06-155">The effect interface can use a semantic to get a handle to a particular effect parameter.</span></span> <span data-ttu-id="3ed06-156">Im folgenden Beispiel wird das Handle der Matrix zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="3ed06-156">For instance, the following returns the handle of the matrix:</span></span>


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



<span data-ttu-id="3ed06-157">Zusätzlich zum Durchsuchen des semantischen namens verfügt die Effect-Schnittstelle über viele andere Methoden, um nach Parametern zu suchen.</span><span class="sxs-lookup"><span data-stu-id="3ed06-157">In addition to searching by semantic name, the effect interface has many other methods to search for parameters.</span></span>

## <a name="use-handles-to-get-and-set-parameters-efficiently"></a><span data-ttu-id="3ed06-158">Verwenden von Handles zum effizienten erhalten und Festlegen von Parametern</span><span class="sxs-lookup"><span data-stu-id="3ed06-158">Use Handles to Get and Set Parameters Efficiently</span></span>

<span data-ttu-id="3ed06-159">Handles bieten eine effiziente Möglichkeit zum Verweisen auf wirkungsparameter, Techniken, Pass-und Anmerkungen mit einem Effekt.</span><span class="sxs-lookup"><span data-stu-id="3ed06-159">Handles provide an efficient means for referencing effect parameters, techniques, passes, and annotations with an effect.</span></span> <span data-ttu-id="3ed06-160">Handles (die vom Typ D3DXHANDLE sind) sind Zeichen folgen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="3ed06-160">Handles (which are of type D3DXHANDLE) are string pointers.</span></span> <span data-ttu-id="3ed06-161">Die Handles, die an Funktionen wie getparameterxxx oder getannotationxxx übermittelt werden, können in einer von drei Formen vorliegen:</span><span class="sxs-lookup"><span data-stu-id="3ed06-161">The handles that are passed into functions such as GetParameterxxx or GetAnnotationxxx can be in one of three forms:</span></span>

-   <span data-ttu-id="3ed06-162">Ein Handle, das von einer Funktion wie getparameterxxx zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3ed06-162">A handle returned by a function such as GetParameterxxx.</span></span>
-   <span data-ttu-id="3ed06-163">Eine Zeichenfolge, die den Namen des Parameters, der Technik, der Übergabe oder der Anmerkung enthält.</span><span class="sxs-lookup"><span data-stu-id="3ed06-163">A string containing the name of the parameter, technique, pass, or annotation.</span></span>
-   <span data-ttu-id="3ed06-164">Ein Handle, das auf **null** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3ed06-164">A handle set to **NULL**.</span></span>

<span data-ttu-id="3ed06-165">In diesem Beispiel wird ein Handle für den Parameter zurückgegeben, dem die "worldviewproj"-Semantik angefügt ist:</span><span class="sxs-lookup"><span data-stu-id="3ed06-165">This example returns a handle to the parameter that has the WORLDVIEWPROJ semantic attached to it:</span></span>


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



## <a name="add-parameter-information-with-annotations"></a><span data-ttu-id="3ed06-166">Hinzufügen von Parameter Informationen mit Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="3ed06-166">Add Parameter Information with Annotations</span></span>

<span data-ttu-id="3ed06-167">Anmerkungen sind benutzerspezifische Daten, die an beliebige Techniken, Pass oder Parameter angefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="3ed06-167">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="3ed06-168">Eine Anmerkung ist eine flexible Möglichkeit zum Hinzufügen von Informationen zu einzelnen Parametern.</span><span class="sxs-lookup"><span data-stu-id="3ed06-168">An annotation is a flexible way to add information to individual parameters.</span></span> <span data-ttu-id="3ed06-169">Die Informationen können gelesen und auf jede Weise verwendet werden, die die Anwendung auswählt.</span><span class="sxs-lookup"><span data-stu-id="3ed06-169">The information can be read back and used any way the application chooses.</span></span> <span data-ttu-id="3ed06-170">Eine Anmerkung kann einen beliebigen Datentyp aufweisen und kann dynamisch hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-170">An annotation can be of any data type and can be added dynamically.</span></span> <span data-ttu-id="3ed06-171">Annotation-Deklarationen werden durch spitzen Klammern getrennt.</span><span class="sxs-lookup"><span data-stu-id="3ed06-171">Annotation declarations are delimited by angle brackets.</span></span> <span data-ttu-id="3ed06-172">Eine Anmerkung enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3ed06-172">An annotation contains:</span></span>

-   <span data-ttu-id="3ed06-173">Ein-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="3ed06-173">A data type.</span></span>
-   <span data-ttu-id="3ed06-174">Ein Variablenname.</span><span class="sxs-lookup"><span data-stu-id="3ed06-174">A variable name.</span></span>
-   <span data-ttu-id="3ed06-175">Ein Gleichheitszeichen (=).</span><span class="sxs-lookup"><span data-stu-id="3ed06-175">An equals sign (=).</span></span>
-   <span data-ttu-id="3ed06-176">Der Datenwert.</span><span class="sxs-lookup"><span data-stu-id="3ed06-176">The data value.</span></span>
-   <span data-ttu-id="3ed06-177">Ein Semikolon mit Endpunkten (;).</span><span class="sxs-lookup"><span data-stu-id="3ed06-177">A ending semicolon (;).</span></span>

<span data-ttu-id="3ed06-178">Beispielsweise enthalten beide vorherigen Beispiele in diesem Dokument diese Anmerkung:</span><span class="sxs-lookup"><span data-stu-id="3ed06-178">For instance, both of the previous examples in this paper contain this annotation:</span></span>


```
texture Tex0 < string name = "tiger.bmp"; >;
```



<span data-ttu-id="3ed06-179">Die-Anmerkung wird an das Textur Objekt angefügt und gibt die Textur Datei an, die zum Initialisieren des Textur Objekts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ed06-179">The annotation is attached to the texture object and specifies the texture file that should be used to initialize the texture object.</span></span> <span data-ttu-id="3ed06-180">Die-Anmerkung initialisiert nicht das Textur Objekt, sondern lediglich ein Teil der Benutzerinformationen, die an die Variable angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="3ed06-180">The annotation does not initialize the texture object, it is simply a piece of user information that is attached to the variable.</span></span> <span data-ttu-id="3ed06-181">Eine Anwendung kann die-Anmerkung entweder mit [**ID3DXBaseEffect:: GetAnnotation**](id3dxbaseeffect--getannotation.md) oder [**ID3DXBaseEffect:: getannotationbyname**](id3dxbaseeffect--getannotationbyname.md) lesen, um die Zeichenfolge zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="3ed06-181">An application can read the annotation with either [**ID3DXBaseEffect::GetAnnotation**](id3dxbaseeffect--getannotation.md) or [**ID3DXBaseEffect::GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) to return the string.</span></span> <span data-ttu-id="3ed06-182">Anmerkungen können auch von der Anwendung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-182">Annotations can also be added by the application.</span></span>

<span data-ttu-id="3ed06-183">Jede Anmerkung:</span><span class="sxs-lookup"><span data-stu-id="3ed06-183">Each annotation:</span></span>

-   <span data-ttu-id="3ed06-184">Muss entweder numerisch oder Zeichen folgen sein.</span><span class="sxs-lookup"><span data-stu-id="3ed06-184">Must be either numeric or strings.</span></span>
-   <span data-ttu-id="3ed06-185">Muss immer mit einem Standardwert initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-185">Must always be initialized with a default value.</span></span>
-   <span data-ttu-id="3ed06-186">Kann [Techniken und übergebenen (Direct3D 9)](techniques-and-passes.md) und [Effektparameter](/previous-versions/windows/desktop/ee417539(v=vs.85))der obersten Ebene zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-186">Can be associated with [Techniques and Passes (Direct3D 9)](techniques-and-passes.md) and top-level [Effect Parameters](/previous-versions/windows/desktop/ee417539(v=vs.85)).</span></span>
-   <span data-ttu-id="3ed06-187">Kann mit [**ID3DXEffect**](id3dxeffect.md) oder [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)geschrieben und daraus gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-187">Can be written to and read from with either [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>
-   <span data-ttu-id="3ed06-188">Kann mit [**ID3DXEffect**](id3dxeffect.md)hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-188">Can be added with [**ID3DXEffect**](id3dxeffect.md).</span></span>
-   <span data-ttu-id="3ed06-189">Innerhalb des Effekts kann nicht auf Sie verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-189">Cannot be referenced inside the effect.</span></span>
-   <span data-ttu-id="3ed06-190">Unter Semantik oder untergeordnete Anmerkungen sind nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="3ed06-190">Cannot have sub-semantics or sub-annotations.</span></span>

## <a name="share-effect-parameters"></a><span data-ttu-id="3ed06-191">Parameter für Freigabe Effekte</span><span class="sxs-lookup"><span data-stu-id="3ed06-191">Share Effect Parameters</span></span>

<span data-ttu-id="3ed06-192">Effektparameter sind alle nicht statischen Variablen, die in einem Effekt deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-192">Effect parameters are all the non-static variables declared in an effect.</span></span> <span data-ttu-id="3ed06-193">Dies kann globale Variablen und Anmerkungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="3ed06-193">This can include global variables and annotations.</span></span> <span data-ttu-id="3ed06-194">Effektparameter können von verschiedenen Effekten gemeinsam genutzt werden, indem Parameter mit dem "Shared"-Schlüsselwort deklariert und dann der Effekt mit einem Effekt Pool erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3ed06-194">Effect parameters can be shared between different effects by declaring parameters with the "shared" keyword and then creating the effect with an effect pool.</span></span>

<span data-ttu-id="3ed06-195">Ein Effekt Pool enthält Parameter für gemeinsame Effekte.</span><span class="sxs-lookup"><span data-stu-id="3ed06-195">An effect pool contains shared effect parameters.</span></span> <span data-ttu-id="3ed06-196">Der Pool wird durch Aufrufen von [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md)erstellt, wodurch eine [**ID3DXEffectPool**](id3dxeffectpool.md) -Schnittstelle zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3ed06-196">The pool is created by calling [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), which returns an [**ID3DXEffectPool**](id3dxeffectpool.md) interface.</span></span> <span data-ttu-id="3ed06-197">Die-Schnittstelle kann bei der Erstellung eines Effekts als Eingabe für jede der D3DXCreateEffectxxx-Funktionen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-197">The interface can be supplied as an input to any of the D3DXCreateEffectxxx functions when an effect is created.</span></span> <span data-ttu-id="3ed06-198">Damit ein Parameter von mehreren Effekten gemeinsam genutzt werden kann, muss der Parameter in den einzelnen gemeinsamen Effekten denselben Namen, denselben Typ und dieselbe Semantik aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3ed06-198">For a parameter to be shared across multiple effects, the parameter must have the same name, type, and semantic in each of the shared effects.</span></span>


```
ID3DXEffectPool* g_pEffectPool = NULL;   // Effect pool for sharing parameters

    D3DXCreateEffectPool( &g_pEffectPool );
```



<span data-ttu-id="3ed06-199">Die Auswirkungen von Freigabe Parametern müssen das gleiche Gerät verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-199">Effects that share parameters must use the same device.</span></span> <span data-ttu-id="3ed06-200">Dies wird erzwungen, um zu verhindern, dass Geräte abhängige Parameter (z. b. Shader oder Texturen) auf verschiedenen Geräten gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-200">This is enforced to prevent the sharing of device-dependent parameters (such as shaders or textures) across different devices.</span></span> <span data-ttu-id="3ed06-201">Parameter werden aus dem Pool gelöscht, wenn die Auswirkungen, die die freigegebenen Parameter enthalten, freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-201">Parameters are deleted from the pool whenever the effects that contain the shared parameters are released.</span></span> <span data-ttu-id="3ed06-202">Wenn Freigabe Parameter nicht erforderlich sind, geben Sie bei der Erstellung eines Effekts **null** für den Effekt Pool an.</span><span class="sxs-lookup"><span data-stu-id="3ed06-202">If sharing parameters is not necessary, supply **NULL** for the effect pool when an effect is created.</span></span>

<span data-ttu-id="3ed06-203">Geklonte Effekte verwenden denselben Effekt Pool wie der Effekt, von dem Sie geklont werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-203">Cloned effects use the same effect pool as the effect from which they are cloned.</span></span> <span data-ttu-id="3ed06-204">Das Klonen eines Effekts führt zu einer exakten Kopie eines Effekts, einschließlich globaler Variablen, Techniken, Durchläufen und Anmerkungen.</span><span class="sxs-lookup"><span data-stu-id="3ed06-204">Cloning an effect makes an exact copy of an effect, including global variables, techniques, passes, and annotations.</span></span>

## <a name="compile-an-effect-offline"></a><span data-ttu-id="3ed06-205">Einen Effekt Offline kompilieren</span><span class="sxs-lookup"><span data-stu-id="3ed06-205">Compile an Effect Offline</span></span>

<span data-ttu-id="3ed06-206">Sie können einen Effekt zur Laufzeit mit [**D3DXCreateEffect**](d3dxcreateeffect.md)kompilieren, oder Sie können einen Effekt Offline kompilieren, indem Sie das Befehlszeilen-Compilertool fxc.exe verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-206">You can compile an effect at run time with [**D3DXCreateEffect**](d3dxcreateeffect.md), or you can compile an effect offline using the command-line compiler tool fxc.exe.</span></span> <span data-ttu-id="3ed06-207">Der Effekt im [compiledebug-Beispiel](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) enthält einen Vertex-Shader, einen Pixel-Shader und eine Technik:</span><span class="sxs-lookup"><span data-stu-id="3ed06-207">The effect in the [CompiledEffect Sample](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) contains a vertex shader, a pixel shader, and one technique:</span></span>


```
// File: CompiledEffect.fx

// Global variables
float4 g_MaterialAmbientColor;    // Material's ambient color
...

// Texture samplers
sampler RenderTargetSampler = 
   ...

// Type: Vertex shader                                      
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0 )
{
   ...
};
// Type: Pixel shader
PS_OUTPUT RenderScenePS( VS_OUTPUT In ) 
{ 
   ...
}

// Type: Technique                                     
technique RenderScene
{
    pass P0
    {          
        ZENABLE = true;
        VertexShader = compile vs_1_1 RenderSceneVS();
        PixelShader  = compile ps_1_1 RenderScenePS();
    }
}
```



<span data-ttu-id="3ed06-208">Wenn Sie den Shader für vs 1 1 mit dem [Effekt-Compilertool](../direct3dtools/fxc.md) kompilieren, werden \_ die folgenden assemblyshaderanweisungen \_ generiert:</span><span class="sxs-lookup"><span data-stu-id="3ed06-208">Using [Effect-Compiler Tool](../direct3dtools/fxc.md) to compile the shader for vs\_1\_1 generated the following assembly shader instructions:</span></span>


```
//
// Generated by Microsoft (R) D3DX9 Shader Compiler 4.09.02.1188
//
//   fxc /T vs_1_1 /E RenderSceneVS /Fc CompiledEffect.txt CompiledEffect.fx
//
//
// Parameters:
//
//   float4 g_LightAmbient;
//   float4 g_LightDiffuse;
//   float3 g_LightDir;
//   float4 g_MaterialAmbientColor;
//   float4 g_MaterialDiffuseColor;
//   float g_fTime;
//   float4x4 g_mWorld;
//   float4x4 g_mWorldViewProjection;
//
//
// Registers:
//
//   Name                   Reg   Size
//   ---------------------- ----- ----
//   g_mWorldViewProjection c0       4
//   g_mWorld               c4       3
//   g_MaterialAmbientColor c7       1
//   g_MaterialDiffuseColor c8       1
//   g_LightDir             c9       1
//   g_LightAmbient         c10      1
//   g_LightDiffuse         c11      1
//   g_fTime                c12      1
//
//
// Default values:
//
//   g_LightDir
//     c9   = { 0.57735, 0.57735, 0.57735, 0 };
//
//   g_LightAmbient
//     c10  = { 1, 1, 1, 1 };
//
//   g_LightDiffuse
//     c11  = { 1, 1, 1, 1 };
//

    vs_1_1
    def c13, 0.159154937, 0.25, 6.28318548, -3.14159274
    def c14, -2.52398507e-007, 2.47609005e-005, -0.00138883968, 0.0416666418
    def c15, -0.5, 1, 0.5, 0
    dcl_position v0
    dcl_normal v1
    dcl_texcoord v2
    mov r0.w, c12.x
    mad r0.w, r0.w, c13.x, c13.y
    expp r3.y, r0.w
    mov r0.w, r3.y
    mad r0.w, r0.w, c13.z, c13.w
    mul r0.w, r0.w, r0.w
    mad r1.w, r0.w, c14.x, c14.y
    mad r1.w, r0.w, r1.w, c14.z
    mad r1.w, r0.w, r1.w, c14.w
    mad r1.w, r0.w, r1.w, c15.x
    mad r0.w, r0.w, r1.w, c15.y
    mul r0.w, r0.w, v0.x
    mul r0.x, r0.w, c15.z
    dp3 r1.x, v1, c4
    dp3 r1.y, v1, c5
    dp3 r1.z, v1, c6
    mov r0.yzw, c15.w
    dp3 r2.x, r1, r1
    add r0, r0, v0
    rsq r1.w, r2.x
    dp4 oPos.x, r0, c0
    mul r1.xyz, r1, r1.w
    dp4 oPos.y, r0, c1
    dp3 r1.x, r1, c9
    dp4 oPos.z, r0, c2
    max r1.w, r1.x, c15.w
    mov r1.xyz, c8
    mul r1.xyz, r1, c11
    mov r2.xyz, c7
    mul r2.xyz, r2, c10
    dp4 oPos.w, r0, c3
    mad oD0.xyz, r1, r1.w, r2
    mov oD0.w, c15.y
    mov oT0.xy, v2

// approximately 34 instruction slots used
```



## <a name="improve-performance-with-preshaders"></a><span data-ttu-id="3ed06-209">Verbessern der Leistung durch preshaders</span><span class="sxs-lookup"><span data-stu-id="3ed06-209">Improve Performance with Preshaders</span></span>

<span data-ttu-id="3ed06-210">Ein preshader ist eine Technik zum Erhöhen der shadereffizienz, indem Konstante shaderausdrücke vorab berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-210">A preshader is a technique for increasing shader efficiency by pre-calculating constant shader expressions.</span></span> <span data-ttu-id="3ed06-211">Der Effekt Compiler ruft die Shader-Berechnungen automatisch aus dem Text eines Shaders ab und führt Sie auf der CPU aus, bevor der Shader ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ed06-211">The effect compiler automatically pulls out shader computations from the body of a shader and executes them on the CPU prior to the shader running.</span></span> <span data-ttu-id="3ed06-212">Folglich arbeiten präshader nur mit Effekten.</span><span class="sxs-lookup"><span data-stu-id="3ed06-212">Consequently, preshaders only work with effects.</span></span> <span data-ttu-id="3ed06-213">Diese beiden Ausdrücke können beispielsweise außerhalb des Shaders ausgewertet werden, bevor Sie ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-213">For instance, these two expressions can be evaluated outside of the shader before it runs.</span></span>


```
mul(World,mul(View, Projection));
sin(time)
```



<span data-ttu-id="3ed06-214">Shader-Berechnungen, die verschoben werden können, sind die, die einheitlichen Parametern zugeordnet sind. Das heißt, dass die Berechnungen für jeden Scheitelpunkt oder Pixel nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-214">Shader computations that can be moved are those associated with uniform parameters; that is, the computations do not change for each vertex or pixel.</span></span> <span data-ttu-id="3ed06-215">Wenn Sie Effekte verwenden, generiert und führt der Effekt Compiler automatisch einen preshader für Sie aus. Es sind keine Flags zum Aktivieren vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-215">If you are using effects, the effect compiler automatically generates and runs a preshader for you; there are no flags to enable.</span></span> <span data-ttu-id="3ed06-216">Preshaders können die Anzahl der Anweisungen pro Shader verringern und auch die Anzahl der Konstanten Registrierungen verringern, die ein Shader beansprucht.</span><span class="sxs-lookup"><span data-stu-id="3ed06-216">Preshaders can reduce the number of instructions per shader and can also reduce the number of constant registers a shader consumes.</span></span>

<span data-ttu-id="3ed06-217">Stellen Sie sich den Effekt Compiler als eine Art von multiprozessorcompiler vor, da er Shader-Code für zwei Arten von Prozessoren kompiliert: eine CPU und eine GPU.</span><span class="sxs-lookup"><span data-stu-id="3ed06-217">Think of the effect compiler as a sort of multi-processor compiler because it compiles shader code for two types of processors: a CPU and a GPU.</span></span> <span data-ttu-id="3ed06-218">Außerdem ist der Effekt Compiler so konzipiert, dass Code von der GPU in die CPU verschoben und somit die shaderleistung verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="3ed06-218">In addition, the effect compiler is designed to move code from the GPU to the CPU and therefore improve shader performance.</span></span> <span data-ttu-id="3ed06-219">Dies ist sehr ähnlich, wenn ein statischer Ausdruck aus einer Schleife abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3ed06-219">This is very similar to pulling a static expression out of a loop.</span></span> <span data-ttu-id="3ed06-220">Ein Shader, der die Position aus dem Raum in den Projektions Bereich umwandelt und Texturkoordinaten in HLSL wie folgt aussehen würde:</span><span class="sxs-lookup"><span data-stu-id="3ed06-220">A shader that transforms position from world space to projection space, and copies texture coordinates would look like this in HLSL:</span></span>


```
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
float4x4 g_mWorldInverse;           // Inverse World matrix
float3 g_LightDir;                  // Light direction in world space
float4 g_LightDiffuse;              // Diffuse color of the light

struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0)
{
    VS_OUTPUT Output;
    
    // Transform the position from object space to projection space
    Output.Position = mul(vPos, g_mWorldViewProjection);

    // Transform the light from world space to object space    
    float3 vLightObjectSpace = normalize(mul(g_LightDir, (float3x3)g_mWorldInverse)); 

    // N dot L lighting
    Output.Diffuse = max(0,dot(vNormal, vLightObjectSpace));
    
    // Copy the texture coordinate
    Output.TextureUV = vTexCoord0; 
    
    return Output;    
}
technique RenderVS
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS();
    }
}
```



<span data-ttu-id="3ed06-221">Wenn Sie den Shader für vs 1 1 mit dem [Effekt-Compilertool](../direct3dtools/fxc.md) kompilieren, werden \_ die folgenden Assemblyanweisungen \_ generiert:</span><span class="sxs-lookup"><span data-stu-id="3ed06-221">Using [Effect-Compiler Tool](../direct3dtools/fxc.md) to compile the shader for vs\_1\_1 generates the following assembly instructions:</span></span>


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //   g_mWorldInverse        c4       3
            //   g_LightDir             c7       1
            //
            
                vs_1_1
                def c8, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                mov r1.xyz, c7
                dp3 r0.x, r1, c4
                dp3 r0.y, r1, c5
                dp3 r0.z, r1, c6
                dp4 oPos.x, v0, c0
                dp3 r1.x, r0, r0
                dp4 oPos.y, v0, c1
                rsq r0.w, r1.x
                dp4 oPos.z, v0, c2
                mul r0.xyz, r0, r0.w
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, r0
                max oD0, r0.x, c8.x
                mov oT0.xy, v2
            
            // approximately 14 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



<span data-ttu-id="3ed06-222">Dies verbraucht ungefähr 14 Slots und beansprucht 9 Konstante Register.</span><span class="sxs-lookup"><span data-stu-id="3ed06-222">This uses up approximately 14 slots and consumes 9 constant registers.</span></span> <span data-ttu-id="3ed06-223">Bei einem preshader verschiebt der Compiler die statischen Ausdrücke aus dem Shader und in den preshader.</span><span class="sxs-lookup"><span data-stu-id="3ed06-223">With a preshader, the compiler moves the static expressions out of the shader and into the preshader.</span></span> <span data-ttu-id="3ed06-224">Derselbe Shader würde wie folgt mit einem preshader aussehen:</span><span class="sxs-lookup"><span data-stu-id="3ed06-224">The same shader would look like this with a preshader:</span></span>


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //
            //
            // Registers:
            //
            //   Name            Reg   Size
            //   --------------- ----- ----
            //   g_mWorldInverse c0       3
            //   g_LightDir      c3       1
            //
            
                preshader
                dot r0.x, c3.xyz, c0.xyz
                dot r0.y, c3.xyz, c1.xyz
                dot r0.z, c3.xyz, c2.xyz
                dot r1.w, r0.xyz, r0.xyz
                rsq r0.w, r1.w
                mul c4.xyz, r0.w, r0.xyz
            
            // approximately 6 instructions used
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //
            
                vs_1_1
                def c5, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                dp4 oPos.x, v0, c0
                dp4 oPos.y, v0, c1
                dp4 oPos.z, v0, c2
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, c4
                max oD0, r0.x, c5.x
                mov oT0.xy, v2
            
            // approximately 7 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



<span data-ttu-id="3ed06-225">Ein Effekt führt einen preshader direkt vor dem Ausführen eines Shaders aus.</span><span class="sxs-lookup"><span data-stu-id="3ed06-225">An effect executes a preshader just before executing a shader.</span></span> <span data-ttu-id="3ed06-226">Das Ergebnis ist die gleiche Funktionalität mit erhöhter shaderleistung, da die Anzahl der Anweisungen, die ausgeführt werden müssen (für jeden Scheitelpunkt oder jedes Pixel, abhängig vom Typ des Shader), reduziert wurde.</span><span class="sxs-lookup"><span data-stu-id="3ed06-226">The result is the same functionality with increased shader performance because the number of instructions that need to be executed (for each vertex or pixel depending on the type of shader) has been reduced.</span></span> <span data-ttu-id="3ed06-227">Außerdem werden weniger Konstante Register vom Shader beansprucht, weil die statischen Ausdrücke in den preshader verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-227">In addition, fewer constant registers are consumed by the shader as a result of the static expressions being moved to the preshader.</span></span> <span data-ttu-id="3ed06-228">Dies bedeutet, dass Shader, die zuvor durch die Anzahl der benötigten Konstanten registriert wurden, jetzt kompiliert werden können, da Sie weniger Konstante Register benötigen.</span><span class="sxs-lookup"><span data-stu-id="3ed06-228">This means that shaders previously limited by the number of constant registers they required may now compile because they require fewer constant registers.</span></span> <span data-ttu-id="3ed06-229">Es empfiehlt sich, eine Leistungsverbesserung von 5 Prozent und 20 Prozent zu erwarten.</span><span class="sxs-lookup"><span data-stu-id="3ed06-229">It is reasonable to expect a 5 percent and a 20 percent performance improvement from preshaders.</span></span>

<span data-ttu-id="3ed06-230">Beachten Sie, dass sich die Eingabe Konstanten von den Ausgabe Konstanten in einem preshader unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="3ed06-230">Keep in mind that the input constants are different from the output constants in a preshader.</span></span> <span data-ttu-id="3ed06-231">Die Ausgabe C1 ist nicht mit der Eingabe C1-Register identisch.</span><span class="sxs-lookup"><span data-stu-id="3ed06-231">The output c1 is not the same as the input c1 register.</span></span> <span data-ttu-id="3ed06-232">Das Schreiben in ein konstantes Register in einem preshader schreibt tatsächlich in den eingabeslot (konstant) des Shader.</span><span class="sxs-lookup"><span data-stu-id="3ed06-232">Writing to a constant register in a preshader actually writes into the corresponding shader's input (constant) slot.</span></span>


```
// BaseDelta c0 1
// Refinements c1 1
preshader
mul c1.x, c0.x, (-2)
add c0.x, c0.x, c0.x
cmp c5.x, c1.x, (1), (0)
```



<span data-ttu-id="3ed06-233">Die obige CMP-Anweisung liest den preshader C1-Wert, während die mul-Anweisung in die Hardware-Shader-Register schreibt, die vom Vertexshader verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3ed06-233">The cmp instruction above will read the preshader c1 value, while the mul instruction will write to the hardware shader registers to be used by the vertex shader.</span></span>

## <a name="use-parameter-blocks-to-manage-effect-parameters"></a><span data-ttu-id="3ed06-234">Verwenden von Parameter Blöcken zum Verwalten von Effekt Parametern</span><span class="sxs-lookup"><span data-stu-id="3ed06-234">Use Parameter Blocks to Manage Effect Parameters</span></span>

<span data-ttu-id="3ed06-235">Parameter Blöcke sind Blöcke der Auswirkung des Zustands.</span><span class="sxs-lookup"><span data-stu-id="3ed06-235">Parameter blocks are blocks of effect state changes.</span></span> <span data-ttu-id="3ed06-236">Ein Parameter Block kann Zustandsänderungen aufzeichnen, sodass Sie später mit einem einzigen-Befehl angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3ed06-236">A parameter block can record state changes, so that they can be applied later on with a single call.</span></span> <span data-ttu-id="3ed06-237">Erstellen Sie einen Parameter Block durch Aufrufen von [**ID3DXEffect:: beginparameterblock**](id3dxeffect--beginparameterblock.md):</span><span class="sxs-lookup"><span data-stu-id="3ed06-237">Create a parameter block by calling [**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md):</span></span>


```
    m_pEffect->SetTechnique( "RenderScene" );

    m_pEffect->BeginParameterBlock();
    D3DXVECTOR4 v4( Diffuse.r, Diffuse.g, Diffuse.b, Diffuse.a );
    m_pEffect->SetVector( "g_vDiffuse", &v4 );
    m_pEffect->SetFloat( "g_fReflectivity", fReflectivity );
    m_pEffect->SetFloat( "g_fAnimSpeed", fAnimSpeed );
    m_pEffect->SetFloat( "g_fSizeMul", fSize );
    m_hParameters = m_pEffect->EndParameterBlock();
```



<span data-ttu-id="3ed06-238">Der Parameter Block speichert vier von den API-aufrufen angewendete Änderungen.</span><span class="sxs-lookup"><span data-stu-id="3ed06-238">The parameter block saves four changes applied by the API calls.</span></span> <span data-ttu-id="3ed06-239">Durch Aufrufen von [**ID3DXEffect:: beginparameterblock**](id3dxeffect--beginparameterblock.md) wird die Aufzeichnung der Zustandsänderungen gestartet.</span><span class="sxs-lookup"><span data-stu-id="3ed06-239">Calling [**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md) starts recording the state changes.</span></span> <span data-ttu-id="3ed06-240">[**ID3DXEffect:: endparameterblock**](id3dxeffect--endparameterblock.md) beendet das Hinzufügen der Änderungen zum Parameter Block und gibt ein Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="3ed06-240">[**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md) stops adding the changes to the parameter block and returns a handle.</span></span> <span data-ttu-id="3ed06-241">Das Handle wird beim Aufrufen von [**ID3DXEffect:: applyparameterblock**](id3dxeffect--applyparameterblock.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="3ed06-241">The handle will be used when calling [**ID3DXEffect::ApplyParameterBlock**](id3dxeffect--applyparameterblock.md).</span></span>

<span data-ttu-id="3ed06-242">Im [effectparam-Beispiel](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx)wird der Parameter Block in der Rendering-Sequenz angewendet:</span><span class="sxs-lookup"><span data-stu-id="3ed06-242">In the [EffectParam Sample](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx), the parameter block is applied in the render sequence:</span></span>


```
CObj g_aObj[NUM_OBJS];       // Object instances

    if( SUCCEEDED( pd3dDevice->BeginScene() ) )
    {
        // Set the shared parameters using the first mesh's effect.

        // Render the mesh objects
        for( int i = 0; i < NUM_OBJS; ++i )
        {
            ID3DXEffect *pEffect = g_aObj[i].m_pEffect;

            // Apply the parameters
            pEffect->ApplyParameterBlock( g_aObj[i].m_hParameters );

            ...

            pEffect->Begin( &cPasses, 0 );
            for( iPass = 0; iPass < cPasses; iPass++ )
            {
              ...
            }
            pEffect->End();
        }

        ...
        pd3dDevice->EndScene();
    }
```



<span data-ttu-id="3ed06-243">Der Parameter Block legt den Wert aller vier Zustandsänderungen fest, kurz bevor [**ID3DXEffect:: begin**](id3dxeffect--begin.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3ed06-243">The parameter block sets the value of all four of the state changes just before [**ID3DXEffect::Begin**](id3dxeffect--begin.md) is called.</span></span> <span data-ttu-id="3ed06-244">Parameter Blöcke sind eine praktische Möglichkeit, mehrere Zustandsänderungen mit einem einzigen API-Befehl festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3ed06-244">Parameter blocks are a handy way to set multiple state changes with a single API call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ed06-245">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3ed06-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ed06-246">Effekte</span><span class="sxs-lookup"><span data-stu-id="3ed06-246">Effects</span></span>](effects.md)
</dt> </dl>

 

 
