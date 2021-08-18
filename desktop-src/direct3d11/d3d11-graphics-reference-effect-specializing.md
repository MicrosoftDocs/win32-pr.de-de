---
title: Spezielle Schnittstellen (Direct3D 11)
description: ID3DX11EffectVariable verfügt über eine Reihe von Methoden zum Umwandeln der Schnittstelle in den gewünschten Schnittstellentyp.
ms.assetid: 20892af0-7d4a-4a89-b8d7-4ef225400697
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e4cff9c74f7a4b4034578b7ddeec2c388f0f953534393ac27778c31ed3856c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126074"
---
# <a name="specializing-interfaces-direct3d-11"></a>Spezielle Schnittstellen (Direct3D 11)

[**ID3DX11EffectVariable**](id3dx11effectvariable.md) verfügt über eine Reihe von Methoden zum Umwandeln der Schnittstelle in den gewünschten Schnittstellentyp. Die Methoden haben das Format *AsType* und enthalten eine Methode für jeden Typ von Effektvariablen (z. B. AsBlend, AsConstantBuffer usw.).

Angenommen, Sie haben einen Effekt mit zwei globalen Variablen: Zeit und eine Welttransformation.


```
float    g_fTime;
float4x4 g_mWorld;
```



Im Folgenden finden Sie ein Beispiel, das diese Variablen erhält:


```
ID3DX11EffectVariable* g_pVariable;
ID3DX11EffectMatrixVariable* g_pmWorld;
ID3DX11EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect11->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pVariable = g_pEffect11->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



Durch die Spezialisierung der Schnittstellen können Sie den Code auf einen einzigen Aufruf reduzieren.


```
g_pmWorld = (g_pEffect11->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect11->GetVariableByName("g_fTime"))->AsScalar();
```



Schnittstellen, die von [**ID3DX11EffectVariable**](id3dx11effectvariable.md) erben, verfügen ebenfalls über diese Methoden, wurden jedoch so entworfen, dass sie ungültige Objekte zurückgeben. nur Aufrufe von **ID3DX11EffectVariable** geben gültige Objekte zurück. Anwendungen können das zurückgegebene Objekt testen, um zu überprüfen, ob es gültig ist, indem [**sie ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md)aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




