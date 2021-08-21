---
title: ID3DX11EffectShaderVariable GetGeometryShader-Methode (D3dx11effect.h)
description: Abrufen eines Geometrie-Shaders.
ms.assetid: 395d5c92-a941-4fbf-9bb9-b43634c1810b
keywords:
- GetGeometryShader-Methode Direct3D 11
- GetGeometryShader-Methode Direct3D 11 , ID3DX11EffectShaderVariable-Schnittstelle
- ID3DX11EffectShaderVariable-Schnittstelle Direct3D 11 , GetGeometryShader-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetGeometryShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77bd190566fbc4e699e087b0203c2f42b697bb1ab0f5dd30d7ec4659367ebd63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565910"
---
# <a name="id3dx11effectshadervariablegetgeometryshader-method"></a>ID3DX11EffectShaderVariable::GetGeometryShader-Methode

Abrufen eines Geometrie-Shaders.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetGeometryShader(
   UINT                 ShaderIndex,
   ID3D11GeometryShader **ppGS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Ein nullbasierter Index.

</dd> <dt>

*ppGS* 
</dt> <dd>

Typ: **[ **ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)\*\***

Ein Zeiger auf einen [**ID3D11GeometryShader-Zeiger,**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader) der bei der Rückgabe auf den geometry-Shader festgelegt wird.

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

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

