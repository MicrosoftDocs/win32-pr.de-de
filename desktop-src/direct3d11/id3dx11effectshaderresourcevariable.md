---
title: ID3DX11EffectShaderResourceVariable-Schnittstelle (D3dx11effect. h)
description: Eine Shader-Resource-Schnittstelle greift auf eine Shaderressource zu.
ms.assetid: 936a3439-1f7d-4fea-b124-1d6ead528250
keywords:
- ID3DX11EffectShaderResourceVariable-Schnittstelle Direct3D 11
- ID3DX11EffectShaderResourceVariable Interface Direct3D 11, beschrieben
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
ms.openlocfilehash: 7abfc2bf29bf3ea5333bf9e7da6630a62c5747aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996298"
---
# <a name="id3dx11effectshaderresourcevariable-interface"></a>ID3DX11EffectShaderResourceVariable-Schnittstelle

Eine Shader-Resource-Schnittstelle greift auf eine Shaderressource zu.

## <a name="members"></a>Member

Die **ID3DX11EffectShaderResourceVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectShaderResourceVariable** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectShaderResourceVariable** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                           | BESCHREIBUNG                                  |
|:---------------------------------------------------------------------------------|:---------------------------------------------|
| [**GetResource**](id3dx11effectshaderresourcevariable-getresource.md)           | Eine Shaderressource erhalten.<br/>            |
| [**Getresourcearray**](id3dx11effectshaderresourcevariable-getresourcearray.md) | Ein Array von Shaderressourcen erhalten.<br/> |
| [**Ziel Quelle**](id3dx11effectshaderresourcevariable-setresource.md)           | Legen Sie eine Shaderressource fest.<br/>            |
| [**"Tartresourcearray"**](id3dx11effectshaderresourcevariable-setresourcearray.md) | Legen Sie ein Array von Shaderressourcen fest.<br/> |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effekte 11-Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





