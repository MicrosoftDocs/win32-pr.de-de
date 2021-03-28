---
title: ID3DX11EffectShaderVariable getvertexshader-Methode (D3dx11effect. h)
description: Einen Vertex-Shader erhalten.
ms.assetid: 31a250ae-154b-43ce-97e3-6480f23dc4e2
keywords:
- Getvertexshader-Methode Direct3D 11
- Getvertexshader-Methode Direct3D 11, ID3DX11EffectShaderVariable-Schnittstelle
- ID3DX11EffectShaderVariable-Schnittstelle Direct3D 11, getvertexshader-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetVertexShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7977da5fc36a0c339069526db723e2c479b49d55
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531022"
---
# <a name="id3dx11effectshadervariablegetvertexshader-method"></a>ID3DX11EffectShaderVariable:: getvertexshader-Methode

Einen Vertex-Shader erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVertexShader(
   UINT               ShaderIndex,
   ID3D11VertexShader **ppVS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Shaderindex* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Ein NULL basierter Index.

</dd> <dt>

*PPVs* 
</dt> <dd>

Typ: **[ **ID3D11VertexShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11vertexshader)\*\***

Ein Zeiger auf einen [**ID3D11VertexShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11vertexshader) -Zeiger, der bei der Rückgabe auf den Scheitelpunkt-Shader festgelegt wird.

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

 

