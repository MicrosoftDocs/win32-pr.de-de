---
title: ID3DX11EffectVariable asshaderresource-Methode (D3dx11effect. h)
description: Eine Shader-Resource-Variable erhalten.
ms.assetid: 02db94eb-980a-4677-af89-3006aef6faca
keywords:
- Asshaderresource-Methode Direct3D 11
- Asshaderresource-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11, asshaderresource-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsShaderResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3af6236d25e8a2c652f5a551bf7199f3a78d8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996314"
---
# <a name="id3dx11effectvariableasshaderresource-method"></a>ID3DX11EffectVariable:: asshaderresource-Methode

Eine Shader-Resource-Variable erhalten.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectShaderResourceVariable* AsShaderResource();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)\***

Ein Zeiger auf eine Shader-Resource-Variable. Siehe [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md).

## <a name="remarks"></a>Bemerkungen

Asshaderresource gibt eine Version der Effekt Variablen zurück, die auf eine Shader-Resource-Variable spezialisiert wurde. Ähnlich wie bei einer Umwandlung gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effekt Variable keine Shader-Ressourcen Daten enthält.

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

 

 





