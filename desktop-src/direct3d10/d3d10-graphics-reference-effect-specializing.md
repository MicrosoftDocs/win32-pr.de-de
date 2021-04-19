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
# <a name="specializing-interfaces-direct3d-10"></a>Spezialisierte Schnittstellen (Direct3D 10)

Die [**ID3D10EffectVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) verfügt über eine Reihe von Methoden, mit denen die Schnittstelle in den speziellen Typ der benötigten Schnittstelle umgewandelt wird. Die Methoden weisen die Form als *Typ* auf und enthalten eine Methode für jeden Typ von Effekt Variable (z. b. asblend, asconstantbuffer usw.).

Nehmen Sie beispielsweise an, Sie haben einen Effekt mit zwei globalen Variablen: Time und eine Welt Transformation.


```
float    g_fTime;
float4x4 g_mWorld;
```



Im folgenden finden Sie ein Beispiel (aus [SimpleSample10 Sample](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)), das diese Variablen abruft:


```
ID3D10EffectVariable* g_pVariable;
ID3D10EffectMatrixVariable* g_pmWorld;
ID3D10EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect10->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pfTime = g_pEffect10->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



Durch die Spezialisierung der Schnittstellen können Sie den Code auf einen einzelnen-Befehl reduzieren.


```
g_pmWorld = (g_pEffect10->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect10->GetVariableByName("g_fTime"))->AsScalar();
```



Schnittstellen, die von der [**ID3D10EffectVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) erben, verfügen auch über diese Methoden, aber Sie wurden so entworfen, dass Sie ungültige Objekte nur Aufrufe der **ID3D10EffectVariable-Schnittstelle** geben gültige Objekte zurück. Anwendungen können das zurückgegebene Objekt testen, um festzustellen, ob es gültig ist, indem [**ID3D10EffectVariable:: IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid)aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



