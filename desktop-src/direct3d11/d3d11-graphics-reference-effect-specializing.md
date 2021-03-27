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
# <a name="specializing-interfaces-direct3d-11"></a>Spezialisierte Schnittstellen (Direct3D 11)

[**ID3DX11EffectVariable**](id3dx11effectvariable.md) verfügt über eine Reihe von Methoden, mit denen die Schnittstelle in den speziellen Typ der benötigten Schnittstelle umgewandelt wird. Die Methoden haben die Form *astype* und enthalten eine Methode für jeden Typ von Effekt Variable (z. b. asblend, asconstantbuffer usw.).

Nehmen Sie beispielsweise an, Sie haben einen Effekt mit zwei globalen Variablen: Time und eine Welt Transformation.


```
float    g_fTime;
float4x4 g_mWorld;
```



Es folgt ein Beispiel, das diese Variablen abruft:


```
ID3DX11EffectVariable* g_pVariable;
ID3DX11EffectMatrixVariable* g_pmWorld;
ID3DX11EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect11->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pVariable = g_pEffect11->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



Durch die Spezialisierung der Schnittstellen können Sie den Code auf einen einzelnen-Befehl reduzieren.


```
g_pmWorld = (g_pEffect11->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect11->GetVariableByName("g_fTime"))->AsScalar();
```



Schnittstellen, die von [**ID3DX11EffectVariable**](id3dx11effectvariable.md) erben, verfügen auch über diese Methoden, aber Sie wurden so entworfen, dass Sie ungültige Objekte zurückgeben. nur Aufrufe von **ID3DX11EffectVariable** geben gültige Objekte zurück. Anwendungen können das zurückgegebene Objekt testen, um festzustellen, ob es gültig ist, indem [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md)aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




