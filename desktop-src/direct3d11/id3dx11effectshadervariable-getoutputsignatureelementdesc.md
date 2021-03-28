---
title: ID3DX11EffectShaderVariable GetOutputSignatureElementDesc-Methode (D3dx11effect. h)
description: Hier erhalten Sie eine Beschreibung der Ausgabe Signatur.
ms.assetid: 05f43a57-18fa-4be7-814e-ffbe53837cab
keywords:
- GetOutputSignatureElementDesc-Methode Direct3D 11
- GetOutputSignatureElementDesc-Methode Direct3D 11, ID3DX11EffectShaderVariable-Schnittstelle
- ID3DX11EffectShaderVariable-Schnittstelle Direct3D 11, GetOutputSignatureElementDesc-Methode
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
ms.openlocfilehash: 29545754be560a3a7710adf23963566a324d8a3f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996163"
---
# <a name="id3dx11effectshadervariablegetoutputsignatureelementdesc-method"></a>ID3DX11EffectShaderVariable:: GetOutputSignatureElementDesc-Methode

Hier erhalten Sie eine Beschreibung der Ausgabe Signatur.

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

*Shaderindex* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Ein NULL basierter shaderindex.

</dd> <dt>

*Element* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Ein NULL basierter Element Index.

</dd> <dt>

*PDE SC* 
</dt> <dd>

Type: **[ **D3D11 \_ Signature \_ Parameter \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***

Ein Zeiger auf eine Parameter Beschreibung (siehe [**D3D11 \_ Signature \_ Parameter \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.

## <a name="remarks"></a>Bemerkungen

Ein Effekt enthält einen oder mehrere Shader. jeder Shader hat eine Eingabe-und Ausgabe Signatur. Jede Signatur enthält ein oder mehrere-Elemente (oder-Parameter). Der Shader-Index identifiziert den Shader, und der Element Index identifiziert das Element (oder den Parameter) in der shadersignatur.

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

 

