---
title: ID3DX11EffectVariable asscalar-Methode (D3dx11effect. h)
description: Eine skalare Variable erhalten.
ms.assetid: 5cc02fb3-351a-4309-9145-1ed7d759a650
keywords:
- Asscalar-Methode Direct3D 11
- Asscalar-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable Interface Direct3D 11, asscalar-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsScalar
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e455250ae99075af449793d634fd6b3c2fafc4b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762390"
---
# <a name="id3dx11effectvariableasscalar-method"></a>ID3DX11EffectVariable:: asscalar-Methode

Eine skalare Variable erhalten.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectScalarVariable* AsScalar();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)\***

Ein Zeiger auf eine skalare Variable. Siehe [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md).

## <a name="remarks"></a>Bemerkungen

Asscalar gibt eine Version der Effekt Variablen zurück, die auf eine skalare Variable spezialisiert wurde. Ähnlich wie bei einer Umwandlung gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effekt Variable keine skalaren Daten enthält.

Anwendungen können das zurückgegebene Objekt auf Gültigkeit testen, indem Sie [**IsValid**](id3dx11effectvariable-isvalid.md)aufrufen.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





