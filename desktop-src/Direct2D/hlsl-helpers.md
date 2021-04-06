---
title: HLSL-Hilfsprogramme
description: Zur Unterstützung von Autoren beim Schreiben von Verknüpf bares-Pixel-Shadern definiert d2d1effecthelpers. hlsli einen Satz von HLSL-Spracherweiterungen in Form von Hilfsmethoden und-Makros.
ms.assetid: 5D0BB99E-7C77-4D45-82E6-F038E4B752A4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8f43447c16d93ef9e1839ac319c761b975222a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947482"
---
# <a name="hlsl-helpers"></a><span data-ttu-id="ff176-103">HLSL-Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="ff176-103">HLSL Helpers</span></span>

<span data-ttu-id="ff176-104">Zur Unterstützung von Autoren beim Schreiben von Verknüpf bares-Pixel-Shadern definiert d2d1effecthelpers. hlsli einen Satz von HLSL-Spracherweiterungen in Form von Hilfsmethoden und-Makros.</span><span class="sxs-lookup"><span data-stu-id="ff176-104">To assist effect authors in writing linkable pixel shaders, d2d1effecthelpers.hlsli defines a set of HLSL language extensions in the form of helper methods and macros.</span></span>

<span data-ttu-id="ff176-105">Fügen Sie der HLSL-Datei eine include-Anweisung hinzu, um d2d1effecthelpers. hlsli dem Projekt hinzuzufügen \# .</span><span class="sxs-lookup"><span data-stu-id="ff176-105">To add d2d1effecthelpers.hlsli to your project, add an \#include statement in the HLSL file.</span></span> <span data-ttu-id="ff176-106">d2d1effecthelpers. hlsli befindet sich am gleichen Speicherort wie andere Direct2D-Header, z. b. d2d1. h; Sie können auf die Eigenschaften Seite der HLSL-Datei verweisen, indem Sie das Makro $ (windowssdk \_ INCLUDEPATH) der zusätzlichen include-Verzeichnisse-Eigenschaft hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ff176-106">d2d1effecthelpers.hlsli is located in the same location as other Direct2D headers such as d2d1.h; it can be referenced from the HLSL file's property page by adding the macro $(WindowsSDK\_IncludePath) to the Additional Include Directories property.</span></span> <span data-ttu-id="ff176-107">Beachten Sie, dass die \# include-Anweisung vorhanden sein muss, nachdem alle Präprozessordirektiven wie D2D \_ input \_ count definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="ff176-107">Note that the \#include statement must come after any preprocessor directives such D2D\_INPUT\_COUNT have been defined.</span></span>

``` syntax
#include <d2d1effecthelpers.hlsli>
```

<span data-ttu-id="ff176-108">Direct2D bietet keine Unterstützung für das Verknüpfen von COMPUTE-oder Vertex-Shadern.</span><span class="sxs-lookup"><span data-stu-id="ff176-108">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="ff176-109">Wenn Ihre Wirkung jedoch sowohl einen Vertex-Shader als auch einen PixelShader verwendet, kann die Ausgabe des Pixelshaders weiterhin verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="ff176-109">However, if your effect uses both a vertex shader and pixel shader, the output of the pixel shader can still be linked.</span></span>

## <a name="preprocessor-directives"></a><span data-ttu-id="ff176-110">Präprozessoranweisungen</span><span class="sxs-lookup"><span data-stu-id="ff176-110">Preprocessor Directives</span></span>

<span data-ttu-id="ff176-111">Präprozessordirektiven sind erforderlich, um Informationen über den Effekt zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="ff176-111">Preprocessor directives are required to communicate information about the effect.</span></span> <span data-ttu-id="ff176-112">Dies schließt die Anzahl der Eingaben und den Samplings der einzelnen Eingaben ein.</span><span class="sxs-lookup"><span data-stu-id="ff176-112">This includes the number of inputs and sampling type of each input.</span></span> <span data-ttu-id="ff176-113">Die folgenden Werte sollten ggf. im Effekt-Shader-Code oberhalb des relevanten Shader-Einstiegs Punkts definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ff176-113">The following values should be defined in the effect shader code above the relevant shader entry point when applicable.</span></span>

-   <span data-ttu-id="ff176-114">`D2D_INPUT_COUNT <N>` : Deklariert die Anzahl der Textur Eingaben für den Effekt.</span><span class="sxs-lookup"><span data-stu-id="ff176-114">`D2D_INPUT_COUNT <N>` : Declares the number of texture inputs to the effect.</span></span> <span data-ttu-id="ff176-115">Wenn der Effekt eine Variable Anzahl von Eingaben hat, muss dieser Wert ordnungsgemäß auf jeden Shader-Einstiegspunkt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ff176-115">If the effect has a variable number of inputs, this value must be scoped appropriately to each shader entry point.</span></span> <span data-ttu-id="ff176-116">Die Definition dieses Werts ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="ff176-116">Defining this value is mandatory.</span></span>
-   <span data-ttu-id="ff176-117">`D2D_INPUT<N>_SIMPLE` : Deklariert die n-te Eingabe für die Verwendung der einfachen Stichprobenentnahme.</span><span class="sxs-lookup"><span data-stu-id="ff176-117">`D2D_INPUT<N>_SIMPLE` : Declares the Nth input to use simple sampling.</span></span> <span data-ttu-id="ff176-118">Wenn Sie nicht definiert ist, wird die n-te Eingabe standardmäßig auf Complex festgelegt</span><span class="sxs-lookup"><span data-stu-id="ff176-118">If not defined, the Nth input defaults to complex.</span></span> <span data-ttu-id="ff176-119">Die Definition dieses Werts ist optional.</span><span class="sxs-lookup"><span data-stu-id="ff176-119">Defining this value is optional.</span></span>
-   <span data-ttu-id="ff176-120">`D2D_INPUT<N>_COMPLEX` : Deklariert die n-te Eingabe für die Verwendung komplexer Stichproben.</span><span class="sxs-lookup"><span data-stu-id="ff176-120">`D2D_INPUT<N>_COMPLEX` : Declares the Nth input to use complex sampling.</span></span> <span data-ttu-id="ff176-121">Wenn Sie nicht definiert ist, wird die n-te Eingabe standardmäßig auf Complex festgelegt</span><span class="sxs-lookup"><span data-stu-id="ff176-121">If not defined, the Nth input defaults to complex.</span></span> <span data-ttu-id="ff176-122">Die Definition dieses Werts ist optional.</span><span class="sxs-lookup"><span data-stu-id="ff176-122">Defining this value is optional.</span></span>
-   <span data-ttu-id="ff176-123">`D2D_REQUIRES_SCENE_POSITION` : Gibt an, dass die shaderfunktion Hilfsmethoden aufruft, die den Positionswert der Szene verwenden (nämlich die [D2DGetScenePosition](d2dgetsceneposition.md) Helper-Funktion).</span><span class="sxs-lookup"><span data-stu-id="ff176-123">`D2D_REQUIRES_SCENE_POSITION` : Indicates that the shader function calls helper methods that use the scene position value (namely, the [D2DGetScenePosition](d2dgetsceneposition.md) helper function).</span></span> <span data-ttu-id="ff176-124">Dieser Parameter sollte nur bei Bedarf eingeschlossen werden, da dieser Parameter nur von einer Funktion pro verknüpftem Shader verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ff176-124">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span> <span data-ttu-id="ff176-125">Die Definition dieses Werts ist optional.</span><span class="sxs-lookup"><span data-stu-id="ff176-125">Defining this value is optional.</span></span>
-   <span data-ttu-id="ff176-126">`D2D_CUSTOM_ENTRY` : Gibt an, dass die pixelshaderfunktion die Ausgabe eines benutzerdefinierten Vertex-Shaders verarbeitet und somit seine Eingabeparameter deklariert.</span><span class="sxs-lookup"><span data-stu-id="ff176-126">`D2D_CUSTOM_ENTRY` : Indicates that the pixel shader function consumes the output of a custom vertex shader, and thus will declare its input parameters.</span></span> <span data-ttu-id="ff176-127">Alle benutzerdefinierten Vertex-shadereingaben verwenden eine komplexe Stichprobenentnahme und können die Ausgabe einer anderen shaderfunktion nicht verwenden (d. h., Sie sind nur nach dem ablaufbar).</span><span class="sxs-lookup"><span data-stu-id="ff176-127">All custom vertex shader inputs use complex sampling, and cannot consume the output of another shader function (i.e. they are only post-linkable).</span></span> <span data-ttu-id="ff176-128">Die Definition dieses Werts ist optional.</span><span class="sxs-lookup"><span data-stu-id="ff176-128">Defining this value is optional.</span></span>

<span data-ttu-id="ff176-129">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ff176-129">For example:</span></span>

``` syntax
#define D2D_INPUT_COUNT 3
#define D2D_INPUT0_SIMPLE
#define D2D_INPUT1_SIMPLE
#define D2D_INPUT2_COMPLEX
#include <d2d1effecthelpers.hlsli>
          
```

## <a name="helper-functions"></a><span data-ttu-id="ff176-130">Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ff176-130">Helper Functions</span></span>

<span data-ttu-id="ff176-131">Hilfsfunktionen werden als Ersatz für einige systeminterne HLSL-Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff176-131">Helper functions are used as a replacement for some native HLSL intrinsic functions.</span></span> <span data-ttu-id="ff176-132">Zur Kompilierzeit werden diese Hilfsfunktionen von Direct2D in der entsprechenden Version neu definiert, abhängig vom Typ der Kompilierungs Methode (Full Shader oder Export Function).</span><span class="sxs-lookup"><span data-stu-id="ff176-132">At compile time, these helper functions are redefined by Direct2D into the appropriate version depending on the compilation target type (full shader or export function).</span></span>

<span data-ttu-id="ff176-133">Die Hilfsfunktionen:</span><span class="sxs-lookup"><span data-stu-id="ff176-133">The helper functions:</span></span>

<dl>

[<span data-ttu-id="ff176-134">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="ff176-134">D2DGetInput</span></span>](d2dgetinput.md)  
[<span data-ttu-id="ff176-135">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="ff176-135">D2DSampleInput</span></span>](d2dsampleinput.md)  
[<span data-ttu-id="ff176-136">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="ff176-136">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
[<span data-ttu-id="ff176-137">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="ff176-137">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
[<span data-ttu-id="ff176-138">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="ff176-138">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
[<span data-ttu-id="ff176-139">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="ff176-139">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
[<span data-ttu-id="ff176-140">D2D \_ PS- \_ Eintrag</span><span class="sxs-lookup"><span data-stu-id="ff176-140">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="ff176-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ff176-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff176-142">Effektshader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="ff176-142">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> </dl>

 

 




