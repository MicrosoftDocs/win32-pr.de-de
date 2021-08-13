---
title: ID3DX11EffectShaderResourceVariable SetResourceArray-Methode (D3dx11effect.h)
description: Legen Sie ein Array von Shaderressourcen fest.
ms.assetid: b9597878-01af-42f3-9cc6-2ce1af4f08f6
keywords:
- SetResourceArray-Methode Direct3D 11
- SetResourceArray-Methode Direct3D 11, ID3DX11EffectShaderResourceVariable-Schnittstelle
- ID3DX11EffectShaderResourceVariable-Schnittstelle Direct3D 11 , SetResourceArray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.SetResourceArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e20a7e24a2ea129c9a72d440dc2cb634bc8ae79a55b8ba47be1bffe6b75e85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408160"
---
# <a name="id3dx11effectshaderresourcevariablesetresourcearray-method"></a>ID3DX11EffectShaderResourceVariable::SetResourceArray-Methode

Legen Sie ein Array von Shaderressourcen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetResourceArray(
   ID3D11ShaderResourceView **ppResources,
   UINT                     Offset,
   UINT                     Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppResources* 
</dt> <dd>

Typ: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***

Die Adresse eines Arrays von Shader-Ressourcenansichtsschnittstellen. Siehe [**ID3D11ShaderResourceView.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)

</dd> <dt>

*Offset* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der nullbasierte Arrayindex, um die erste Schnittstelle zu erhalten.

</dd> <dt>

*Count* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Elemente im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectShaderResourceVariable](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

