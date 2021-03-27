---
title: Spezialisierte Schnittstellen (Direct3D 11)
description: ID3DX11EffectVariable verfügt über eine Reihe von Methoden, mit denen die Schnittstelle in den speziellen Typ der benötigten Schnittstelle umgewandelt wird.
ms.assetid: 20892af0-7d4a-4a89-b8d7-4ef225400697
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9f8adb5a5bb184473ff5679df99f0b71557fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712071"
---
# <a name="specializing-interfaces-direct3d-11"></a><span data-ttu-id="d26b0-103">Spezialisierte Schnittstellen (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="d26b0-103">Specializing Interfaces (Direct3D 11)</span></span>

<span data-ttu-id="d26b0-104">[**ID3DX11EffectVariable**](id3dx11effectvariable.md) verfügt über eine Reihe von Methoden, mit denen die Schnittstelle in den speziellen Typ der benötigten Schnittstelle umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="d26b0-104">[**ID3DX11EffectVariable**](id3dx11effectvariable.md) has a number of methods for casting the interface into the particular type of interface you need.</span></span> <span data-ttu-id="d26b0-105">Die Methoden haben die Form *astype* und enthalten eine Methode für jeden Typ von Effekt Variable (z. b. asblend, asconstantbuffer usw.).</span><span class="sxs-lookup"><span data-stu-id="d26b0-105">The methods are of the form *AsType* and include a method for each type of effect variable (such as AsBlend, AsConstantBuffer etc..)</span></span>

<span data-ttu-id="d26b0-106">Nehmen Sie beispielsweise an, Sie haben einen Effekt mit zwei globalen Variablen: Time und eine Welt Transformation.</span><span class="sxs-lookup"><span data-stu-id="d26b0-106">For example, suppose you have an effect with two global variables: time and a world transform.</span></span>


```
float    g_fTime;
float4x4 g_mWorld;
```



<span data-ttu-id="d26b0-107">Es folgt ein Beispiel, das diese Variablen abruft:</span><span class="sxs-lookup"><span data-stu-id="d26b0-107">Here is an example that gets these variables:</span></span>


```
ID3DX11EffectVariable* g_pVariable;
ID3DX11EffectMatrixVariable* g_pmWorld;
ID3DX11EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect11->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pVariable = g_pEffect11->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



<span data-ttu-id="d26b0-108">Durch die Spezialisierung der Schnittstellen können Sie den Code auf einen einzelnen-Befehl reduzieren.</span><span class="sxs-lookup"><span data-stu-id="d26b0-108">By specializing the interfaces, you could reduce the code to a single call.</span></span>


```
g_pmWorld = (g_pEffect11->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect11->GetVariableByName("g_fTime"))->AsScalar();
```



<span data-ttu-id="d26b0-109">Schnittstellen, die von [**ID3DX11EffectVariable**](id3dx11effectvariable.md) erben, verfügen auch über diese Methoden, aber Sie wurden so entworfen, dass Sie ungültige Objekte zurückgeben. nur Aufrufe von **ID3DX11EffectVariable** geben gültige Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="d26b0-109">Interfaces that inherit from [**ID3DX11EffectVariable**](id3dx11effectvariable.md) also have these methods, but they have been designed to return invalid objects; only calls from **ID3DX11EffectVariable** return valid objects.</span></span> <span data-ttu-id="d26b0-110">Anwendungen können das zurückgegebene Objekt testen, um festzustellen, ob es gültig ist, indem [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d26b0-110">Applications can test the returned object to see if it is valid by calling [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d26b0-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d26b0-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d26b0-112">Effekte (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="d26b0-112">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




