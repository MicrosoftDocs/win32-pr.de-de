---
title: ID3DX11EffectShaderVariable GetComputeShader-Methode (D3dx11effect.h)
description: Abrufen eines Compute-Shaders.
ms.assetid: 16a48be1-4e73-4206-837f-615f8d624086
keywords:
- GetComputeShader-Methode Direct3D 11
- GetComputeShader-Methode Direct3D 11 , ID3DX11EffectShaderVariable-Schnittstelle
- ID3DX11EffectShaderVariable-Schnittstelle Direct3D 11, GetComputeShader-Methode
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
ms.openlocfilehash: 27a256c143a7232494e34c2b6c36255f1360cf15225c212d0d7c1be6678d3b7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565900"
---
# <a name="id3dx11effectshadervariablegetcomputeshader-method"></a>ID3DX11EffectShaderVariable::GetComputeShader-Methode

Abrufen eines Compute-Shaders.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetComputeShader(
   UINT                ShaderIndex,
   ID3D11ComputeShader **ppPS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Index des Compute-Shaders.

</dd> <dt>

*Öpp* 
</dt> <dd>

Typ: **[ **ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader)\*\***

Zeiger auf einen [**ID3D11ComputeShader-Zeiger,**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader) der bei der Rückgabe auf den Computeshader festgelegt wird.

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

 

