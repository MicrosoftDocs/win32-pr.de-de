---
title: ID3DX11EffectShaderVariable GetPatchConstantSignatureElementDesc-Methode (D3dx11effect.h)
description: Hier finden Sie eine Beschreibung der Patchkonst konstanten Signatur.
ms.assetid: 72a86cf6-ace2-4306-ac5c-37d888c087f7
keywords:
- GetPatchConstantSignatureElementDesc-Methode Direct3D 11
- GetPatchConstantSignatureElementDesc-Methode Direct3D 11, ID3DX11EffectShaderVariable-Schnittstelle
- ID3DX11EffectShaderVariable-Schnittstelle Direct3D 11 , GetPatchConstantSignatureElementDesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPatchConstantSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85adc4a022c0f897a2e228aab670ccae60de0ec256e5f88e033991b137863fe1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565870"
---
# <a name="id3dx11effectshadervariablegetpatchconstantsignatureelementdesc-method"></a>ID3DX11EffectShaderVariable::GetPatchConstantSignatureElementDesc-Methode

Hier finden Sie eine Beschreibung der Patchkonst konstanten Signatur.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPatchConstantSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Ein nullbasierter Shaderindex.

</dd> <dt>

*Element* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Ein nullbasierter Elementindex.

</dd> <dt>

*pDesc* 
</dt> <dd>

Typ: **[ **D3D11 \_ SIGNATURE \_ PARAMETER \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***

Ein Zeiger auf eine Parameterbeschreibung (siehe [**D3D11 \_ SIGNATURE \_ PARAMETER \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

