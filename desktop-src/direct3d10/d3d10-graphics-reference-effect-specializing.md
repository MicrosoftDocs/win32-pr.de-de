---
description: Die ID3D10EffectVariable-Schnittstelle verfügt über eine Reihe von Methoden, mit denen die Schnittstelle in den speziellen Typ der benötigten Schnittstelle umgewandelt wird.
ms.assetid: c0842a1d-b78c-44b2-89c7-452d54efe403
title: Spezialisierte Schnittstellen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ce8bc29ae16ada650da7283beb1dd858948cae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342603"
---
# <a name="specializing-interfaces-direct3d-10"></a><span data-ttu-id="51dee-103">Spezialisierte Schnittstellen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="51dee-103">Specializing Interfaces (Direct3D 10)</span></span>

<span data-ttu-id="51dee-104">Die [**ID3D10EffectVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) verfügt über eine Reihe von Methoden, mit denen die Schnittstelle in den speziellen Typ der benötigten Schnittstelle umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="51dee-104">[**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) has a number of methods for casting the interface into the particular type of interface you need.</span></span> <span data-ttu-id="51dee-105">Die Methoden weisen die Form als *Typ* auf und enthalten eine Methode für jeden Typ von Effekt Variable (z. b. asblend, asconstantbuffer usw.).</span><span class="sxs-lookup"><span data-stu-id="51dee-105">The methods are of the form As *Type* and include a method for each type of effect variable (such as AsBlend, AsConstantBuffer etc..)</span></span>

<span data-ttu-id="51dee-106">Nehmen Sie beispielsweise an, Sie haben einen Effekt mit zwei globalen Variablen: Time und eine Welt Transformation.</span><span class="sxs-lookup"><span data-stu-id="51dee-106">For example, suppose you have an effect with two global variables: time and a world transform.</span></span>


```
float    g_fTime;
float4x4 g_mWorld;
```



<span data-ttu-id="51dee-107">Im folgenden finden Sie ein Beispiel (aus [SimpleSample10 Sample](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)), das diese Variablen abruft:</span><span class="sxs-lookup"><span data-stu-id="51dee-107">Here is an example (from [SimpleSample10 Sample](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) that gets these variables:</span></span>


```
ID3D10EffectVariable* g_pVariable;
ID3D10EffectMatrixVariable* g_pmWorld;
ID3D10EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect10->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pfTime = g_pEffect10->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



<span data-ttu-id="51dee-108">Durch die Spezialisierung der Schnittstellen können Sie den Code auf einen einzelnen-Befehl reduzieren.</span><span class="sxs-lookup"><span data-stu-id="51dee-108">By specializing the interfaces, you could reduce the code to a single call.</span></span>


```
g_pmWorld = (g_pEffect10->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect10->GetVariableByName("g_fTime"))->AsScalar();
```



<span data-ttu-id="51dee-109">Schnittstellen, die von der [**ID3D10EffectVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) erben, verfügen auch über diese Methoden, aber Sie wurden so entworfen, dass Sie ungültige Objekte nur Aufrufe der **ID3D10EffectVariable-Schnittstelle** geben gültige Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="51dee-109">Interfaces that inherit from [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) also have these methods, but they have been designed to return invalid objects; only calls from **ID3D10EffectVariable Interface** return valid objects.</span></span> <span data-ttu-id="51dee-110">Anwendungen können das zurückgegebene Objekt testen, um festzustellen, ob es gültig ist, indem [**ID3D10EffectVariable:: IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="51dee-110">Applications can test the returned object to see if it is valid by calling [**ID3D10EffectVariable::IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).</span></span>

## <a name="related-topics"></a><span data-ttu-id="51dee-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51dee-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51dee-112">Effekte</span><span class="sxs-lookup"><span data-stu-id="51dee-112">Effects</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



