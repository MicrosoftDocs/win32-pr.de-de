---
title: ID3DX11EffectShaderResourceVariable SetResource-Methode (D3dx11effect.h)
description: Legen Sie eine Shaderressource fest.
ms.assetid: f85c33ff-dc00-4421-939c-74f9317faadc
keywords:
- SetResource-Methode Direct3D 11
- SetResource-Methode Direct3D 11 , ID3DX11EffectShaderResourceVariable-Schnittstelle
- ID3DX11EffectShaderResourceVariable-Schnittstelle Direct3D 11 , SetResource-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.SetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf0db2db1886298633ba70fa9af6ce1d475b5c511487b35e65d20373f8282f3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533438"
---
# <a name="id3dx11effectshaderresourcevariablesetresource-method"></a>ID3DX11EffectShaderResourceVariable::SetResource-Methode

Legen Sie eine Shaderressource fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetResource(
   ID3D11ShaderResourceView *pResource
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pResource* 
</dt> <dd>

Typ: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***

Die Adresse eines Zeigers auf eine shader-resource-view-Schnittstelle. Siehe [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

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

[ID3DX11EffectShaderResourceVariable](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

 





