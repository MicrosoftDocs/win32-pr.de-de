---
title: ID3DX11EffectShaderVariable getcomputeshader-Methode (D3dx11effect. h)
description: Einen Compute-Shader erhalten.
ms.assetid: 16a48be1-4e73-4206-837f-615f8d624086
keywords:
- Getcomputeshader-Methode Direct3D 11
- Getcomputeshader-Methode Direct3D 11, ID3DX11EffectShaderVariable-Schnittstelle
- ID3DX11EffectShaderVariable-Schnittstelle Direct3D 11, getcomputeshader-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetComputeShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9312a7d603370d53c0721574623733c9e75da8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219720"
---
# <a name="id3dx11effectshadervariablegetcomputeshader-method"></a>ID3DX11EffectShaderVariable:: getcomputeshader-Methode

Einen Compute-Shader erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetComputeShader(
   UINT                ShaderIndex,
   ID3D11ComputeShader **ppPS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Shaderindex* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Der Index des Compute-Shaders.

</dd> <dt>

*PPPs* 
</dt> <dd>

Typ: **[ **ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader)\*\***

Zeiger auf einen [**ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader) -Zeiger, der bei der Rückgabe auf den Compute-Shader festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.

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

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

