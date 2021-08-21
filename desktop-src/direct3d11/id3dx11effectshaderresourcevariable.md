---
title: ID3DX11EffectShaderResourceVariable-Schnittstelle (D3dx11effect.h)
description: Eine Shader-Ressourcenschnittstelle greift auf eine Shaderressource zu.
ms.assetid: 936a3439-1f7d-4fea-b124-1d6ead528250
keywords:
- ID3DX11EffectShaderResourceVariable-Schnittstelle Direct3D 11
- ID3DX11EffectShaderResourceVariable-Schnittstelle Direct3D 11 , beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1cdfce3ce5fe907de5b0149f2280d8b1e34a8761c56cf9e83e316ea253d7366
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533286"
---
# <a name="id3dx11effectshaderresourcevariable-interface"></a>ID3DX11EffectShaderResourceVariable-Schnittstelle

Eine Shader-Ressourcenschnittstelle greift auf eine Shaderressource zu.

## <a name="members"></a>Member

Die **ID3DX11EffectShaderResourceVariable-Schnittstelle** erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectShaderResourceVariable** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectShaderResourceVariable-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                           | Beschreibung                                  |
|:---------------------------------------------------------------------------------|:---------------------------------------------|
| [**GetResource**](id3dx11effectshaderresourcevariable-getresource.md)           | Abrufen einer Shaderressource.<br/>            |
| [**GetResourceArray**](id3dx11effectshaderresourcevariable-getresourcearray.md) | Abrufen eines Arrays von Shaderressourcen.<br/> |
| [**SetResource**](id3dx11effectshaderresourcevariable-setresource.md)           | Legen Sie eine Shaderressource fest.<br/>            |
| [**SetResourceArray**](id3dx11effectshaderresourcevariable-setresourcearray.md) | Legen Sie ein Array von Shaderressourcen fest.<br/> |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effekte 11 Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





