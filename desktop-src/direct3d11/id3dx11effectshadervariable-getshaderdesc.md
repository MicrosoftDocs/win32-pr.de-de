---
title: ID3DX11EffectShaderVariable GetShaderDesc-Methode (D3dx11effect.h)
description: Abrufen einer Shaderbeschreibung.
ms.assetid: 7dd667d3-c500-4486-b279-a165befe8733
keywords:
- GetShaderDesc-Methode Direct3D 11
- GetShaderDesc-Methode Direct3D 11 , ID3DX11EffectShaderVariable-Schnittstelle
- ID3DX11EffectShaderVariable-Schnittstelle Direct3D 11 , GetShaderDesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f78e3a41fbd7f1063abdbd8c782119f62e141b7fa5a160106cf85be274435fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676850"
---
# <a name="id3dx11effectshadervariablegetshaderdesc-method"></a>ID3DX11EffectShaderVariable::GetShaderDesc-Methode

Abrufen einer Shaderbeschreibung.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetShaderDesc(
   UINT                      ShaderIndex,
   D3DX11_EFFECT_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Ein nullbasierter Index.

</dd> <dt>

*pDesc* 
</dt> <dd>

Typ: **[ **D3DX11 \_ EFFECT \_ SHADER \_ DESC**](d3dx11-effect-shader-desc.md)\***

Ein Zeiger auf eine Shaderbeschreibung (siehe [**D3DX11 \_ EFFECT \_ SHADER \_ DESC**](d3dx11-effect-shader-desc.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

