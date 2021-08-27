---
title: ID3DX11EffectShaderVariable GetOutputSignatureElementDesc-Methode (D3dx11effect.h)
description: Hier erhalten Sie eine Ausgabesignaturbeschreibung.
ms.assetid: 05f43a57-18fa-4be7-814e-ffbe53837cab
keywords:
- GetOutputSignatureElementDesc-Methode Direct3D 11
- GetOutputSignatureElementDesc-Methode Direct3D 11, ID3DX11EffectShaderVariable-Schnittstelle
- ID3DX11EffectShaderVariable-Schnittstelle Direct3D 11 , GetOutputSignatureElementDesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetOutputSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af968b25a00e32b489a520e9d4a3e870329af910caa8ac1bf45ac49a7ea6132
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533266"
---
# <a name="id3dx11effectshadervariablegetoutputsignatureelementdesc-method"></a>ID3DX11EffectShaderVariable::GetOutputSignatureElementDesc-Methode

Hier erhalten Sie eine Ausgabesignaturbeschreibung.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetOutputSignatureElementDesc(
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

Ein Effekt enthält mindestens einen Shader. jeder Shader verfügt über eine Eingabe- und Ausgabesignatur. jede Signatur enthält ein oder mehrere Elemente (oder Parameter). Der Shaderindex identifiziert den Shader, und der Elementindex identifiziert das Element (oder den Parameter) in der Shadersignatur.

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

 

