---
title: ID3DX11EffectVariable AsShaderResource-Methode (D3dx11effect.h)
description: Abrufen einer Shader-Ressourcenvariablen.
ms.assetid: 02db94eb-980a-4677-af89-3006aef6faca
keywords:
- AsShaderResource-Methode Direct3D 11
- AsShaderResource-Methode Direct3D 11 , ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11 , AsShaderResource-Methode
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
ms.openlocfilehash: 0ef87874c005f12d3e49962ee438f516df3631c12ff17fc4db27e0a82fe1a654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531383"
---
# <a name="id3dx11effectvariableasshaderresource-method"></a>ID3DX11EffectVariable::AsShaderResource-Methode

Abrufen einer Shader-Ressourcenvariablen.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectShaderResourceVariable* AsShaderResource();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)\***

Ein Zeiger auf eine Shader-Ressourcenvariable. Siehe [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md).

## <a name="remarks"></a>Hinweise

AsShaderResource gibt eine Version der Effect-Variablen zurück, die auf eine Shader-Ressourcenvariable spezialisiert wurde. Ähnlich wie bei einer Umwandlung gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effect-Variable keine Shaderressourcendaten enthält.

Anwendungen können das zurückgegebene Objekt auf Gültigkeit testen, indem [**sie IsValid**](id3dx11effectvariable-isvalid.md)aufrufen.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





