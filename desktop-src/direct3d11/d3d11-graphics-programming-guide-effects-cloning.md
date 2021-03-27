---
title: Klonen eines Effekts
description: Das Klonen eines Effekts erzeugt eine zweite, fast identische Kopie des Effekts.
ms.assetid: e3870363-5ee8-4fdc-a489-cdaeef8c9c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68607d3cc9f00a346fcfa65c255f3caa51dea384
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711705"
---
# <a name="cloning-an-effect"></a><span data-ttu-id="9d5c5-103">Klonen eines Effekts</span><span class="sxs-lookup"><span data-stu-id="9d5c5-103">Cloning an Effect</span></span>

<span data-ttu-id="9d5c5-104">Das Klonen eines Effekts erzeugt eine zweite, fast identische Kopie des Effekts.</span><span class="sxs-lookup"><span data-stu-id="9d5c5-104">Cloning an effect creates a second, almost identical copy of the effect.</span></span> <span data-ttu-id="9d5c5-105">Im folgenden einzelnen Qualifizierer finden Sie eine Erläuterung, warum dies nicht exakt ist.</span><span class="sxs-lookup"><span data-stu-id="9d5c5-105">See the following single qualifier for an explanation of why it is not exact.</span></span> <span data-ttu-id="9d5c5-106">Eine zweite Kopie eines Effekts ist nützlich, wenn Sie das Effekten-Framework für mehrere Threads verwenden möchten, da die Effekt Laufzeit nicht Thread sicher ist, um eine hohe Leistung aufrechtzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="9d5c5-106">A second copy of an effect is useful when one wants to use the effects framework on multiple threads, since the effect runtime is not thread safe to maintain high performance.</span></span>

<span data-ttu-id="9d5c5-107">Da Geräte Kontexte auch nicht Thread sicher sind, sollten verschiedene Threads verschiedene Geräte Kontexte an die ID3DX11EffectPass:: Apply-Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="9d5c5-107">Since device contexts are also non-thread-safe, different threads should pass different device contexts to the ID3DX11EffectPass::Apply method.</span></span>

<span data-ttu-id="9d5c5-108">Ein Effekt kann mit der folgenden Syntax geklont werden:</span><span class="sxs-lookup"><span data-stu-id="9d5c5-108">An effect can be cloned with the following syntax:</span></span>


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



<span data-ttu-id="9d5c5-109">Im obigen Beispiel wird die geklonte Kopie denselben Zustand wie der ursprüngliche Effekt Kapseln, unabhängig davon, in welchem Zustand sich der ursprüngliche Effekt befindet.</span><span class="sxs-lookup"><span data-stu-id="9d5c5-109">In the above example, the cloned copy will encapsulate the same state as the original effect, regardless of what state the original effect is in.</span></span> <span data-ttu-id="9d5c5-110">Dies gilt insbesondere für:</span><span class="sxs-lookup"><span data-stu-id="9d5c5-110">In particular:</span></span>

1.  <span data-ttu-id="9d5c5-111">Wenn "Peer-ffect" optimiert ist, wird der pgeklonte Effekt optimiert.</span><span class="sxs-lookup"><span data-stu-id="9d5c5-111">If pEffect is optimized, pCloned Effect is optimized</span></span>
2.  <span data-ttu-id="9d5c5-112">Wenn für "Peer-ffect" einige vom Benutzer verwaltete Variablen vorhanden sind, haben die pgeklonten Effekte dieselben Benutzer verwalteten Variablen (siehe die Beschreibung unten).</span><span class="sxs-lookup"><span data-stu-id="9d5c5-112">If pEffect has some user-managed variables, pCloned Effect will have the same user-managed variables (see the single description below)</span></span>
3.  <span data-ttu-id="9d5c5-113">Alle ausstehenden Variablen Aktualisierungen (bis zum Update des Gerätestatus "Apply") in "pclonede ffect" stehen aus.</span><span class="sxs-lookup"><span data-stu-id="9d5c5-113">Any pending variable updates (until an Apply call updates device state) in pEffect will be pending in pClonedEffect</span></span>

<span data-ttu-id="9d5c5-114">Die folgenden Direct3D 11-Geräte Objekte sind unveränderlich oder werden nie durch das Effects-Framework aktualisiert, sodass der geklonte Effekt auf die gleichen Objekte wie der ursprüngliche Effekt zeigt:</span><span class="sxs-lookup"><span data-stu-id="9d5c5-114">The following Direct3D 11 device objects are immutable or never updated by the effects framework, so the cloned effect will point to the same objects as the original effect:</span></span>

1.  <span data-ttu-id="9d5c5-115">State Block-Objekte (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)</span><span class="sxs-lookup"><span data-stu-id="9d5c5-115">State block objects (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)</span></span>
2.  <span data-ttu-id="9d5c5-116">Shader</span><span class="sxs-lookup"><span data-stu-id="9d5c5-116">Shaders</span></span>
3.  <span data-ttu-id="9d5c5-117">Klassen Instanzen</span><span class="sxs-lookup"><span data-stu-id="9d5c5-117">Class instances</span></span>
4.  <span data-ttu-id="9d5c5-118">Texturen (ohne Textur Puffer)</span><span class="sxs-lookup"><span data-stu-id="9d5c5-118">Textures (not including texture buffers)</span></span>
5.  <span data-ttu-id="9d5c5-119">Ungeordnete Zugriffs Sichten</span><span class="sxs-lookup"><span data-stu-id="9d5c5-119">Unordered access views</span></span>

<span data-ttu-id="9d5c5-120">Die folgenden Direct3D 11-Geräte Objekte sind unveränderlich und werden von der Effekt Laufzeit geändert (es sei denn, vom Benutzer verwaltet oder Single in einem geklonten Effekt). neue Kopien dieser Objekte werden erstellt, wenn Sie nicht einzeln sind:</span><span class="sxs-lookup"><span data-stu-id="9d5c5-120">The following Direct3D 11 device objects are both immutable and modified by the effect runtime (unless user-managed or single in a cloned effect); new copies of these objects are created when non-single:</span></span>

1.  <span data-ttu-id="9d5c5-121">Konstantenpuffer</span><span class="sxs-lookup"><span data-stu-id="9d5c5-121">Constant buffers</span></span>
2.  <span data-ttu-id="9d5c5-122">Textur Puffer</span><span class="sxs-lookup"><span data-stu-id="9d5c5-122">Texture Buffers</span></span>

## <a name="single-constant-buffers-and-texture-buffers"></a><span data-ttu-id="9d5c5-123">Einzelne Konstante Puffer und Textur Puffer</span><span class="sxs-lookup"><span data-stu-id="9d5c5-123">Single Constant Buffers and Texture Buffers</span></span>

<span data-ttu-id="9d5c5-124">Beachten Sie, dass sich diese Erörterung auf Konstante Puffer und Texturen bezieht</span><span class="sxs-lookup"><span data-stu-id="9d5c5-124">Note that this discussion applies to both constant buffers and textures, but constant buffers are assumed for ease of reading.</span></span>

<span data-ttu-id="9d5c5-125">In Fällen, in denen ein konstanter Puffer nur von einem Thread aktualisiert wird, werden diese Daten von einem Gerätezustand, der durch geklonte Effekte festgelegt wurde, verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d5c5-125">There may be cases where a constant buffer is only updated by one thread, but device state set by cloned effects will use this data.</span></span> <span data-ttu-id="9d5c5-126">Der Haupteffekt kann z. b. die Welt aktualisieren und Matrizen anzeigen, auf die von Shadern in geklonten Effekten verwiesen wird, die nicht die Welt-und Ansichts Matrizen ändern.</span><span class="sxs-lookup"><span data-stu-id="9d5c5-126">For example, the main effect may update the world and view matrices which are referenced from shaders in cloned effects which do not change the world and view matrices.</span></span> <span data-ttu-id="9d5c5-127">In diesen Fällen müssen die geklonten Effekte auf den aktuellen Konstanten Puffer verweisen, anstatt einen neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9d5c5-127">In these cases, the cloned effects need to reference the current constant buffer instead of recreating one.</span></span>

<span data-ttu-id="9d5c5-128">Es gibt zwei Möglichkeiten, dieses gewünschte Ergebnis zu erzielen:</span><span class="sxs-lookup"><span data-stu-id="9d5c5-128">There are two ways to achieve this desired result:</span></span>

1.  <span data-ttu-id="9d5c5-129">Verwenden Sie ID3DX11EffectConstantBuffer:: setconstantbuffer für den geklonten Effekt, damit er vom Benutzer verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="9d5c5-129">Use ID3DX11EffectConstantBuffer::SetConstantBuffer on the cloned effect to make it user-managed</span></span>
2.  <span data-ttu-id="9d5c5-130">Markieren Sie den konstanten Puffer im HLSL-Code als "Single", und erzwingen Sie, dass die Auswirkung der Laufzeit nach dem Klonen vom Benutzer verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="9d5c5-130">Mark the constant buffer as "single" in the HLSL code, forcing the effect runtime to treat is as user-managed after cloning</span></span>

<span data-ttu-id="9d5c5-131">Es gibt zwei Unterschiede zwischen den beiden oben genannten Methoden.</span><span class="sxs-lookup"><span data-stu-id="9d5c5-131">There are two differences between the two methods above.</span></span> <span data-ttu-id="9d5c5-132">Zuerst wird in Methode 1 ein neuer ID3D11Buffer erstellt, und der Benutzer wird vor dem Aufruf von setconstantbuffer aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9d5c5-132">First, in method 1, a new ID3D11Buffer will be created and user before SetConstantBuffer is called.</span></span> <span data-ttu-id="9d5c5-133">Nach dem Aufrufen von undosetconstantbuffer im geklonten Effekt verweist die Variable in der Methode 1Auf den neu erstellten Puffer (die Auswirkungen werden bei Apply aktualisiert), während die Variable in der Methode 2 weiterhin auf den ursprünglichen Puffer zeigt (nicht bei der Übersetzung aktualisiert).</span><span class="sxs-lookup"><span data-stu-id="9d5c5-133">Also, after calling UndoSetConstantBuffer in the cloned effect, the variable in method 1will point to the newly-created buffer (which effects will update on Apply) while the variable in method 2 will continue to point to the original buffer (not updating it on Apply).</span></span>

<span data-ttu-id="9d5c5-134">Sehen Sie sich das folgende Beispiel in HLSL an:</span><span class="sxs-lookup"><span data-stu-id="9d5c5-134">See the following example in HLSL:</span></span>


```
cbuffer ObjectData
{
    float4 Position;
};
single cbuffer ViewData
{
    float4x4 ViewMatrix;
};
```



<span data-ttu-id="9d5c5-135">Beim Klonen wird durch den geklonten Effekt ein neuer ID3D11Buffer für ObjectData erstellt, und der Inhalt wird bei Apply ausgefüllt, aber auf den ursprünglichen ID3D11Buffer für ViewData verwiesen.</span><span class="sxs-lookup"><span data-stu-id="9d5c5-135">While cloning, the cloned effect will create a new ID3D11Buffer for ObjectData, and fill its contents on Apply, but reference the original ID3D11Buffer for ViewData.</span></span> <span data-ttu-id="9d5c5-136">Der einzelne Qualifizierer kann beim Klon Vorgang ignoriert werden, indem das \_ Flag "Bibliothek d3dx11 Effect \_ Clone \_ Force \_ nonsingle" festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="9d5c5-136">The single qualifier can be ignored in the cloning process by setting the D3DX11\_EFFECT\_CLONE\_FORCE\_NONSINGLE flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d5c5-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9d5c5-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d5c5-138">Effekte (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="9d5c5-138">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




