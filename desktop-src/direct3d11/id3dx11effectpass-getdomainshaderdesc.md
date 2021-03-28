---
title: ID3DX11EffectPass getdomainshaderdesc-Methode (D3dx11effect. h)
description: Eine Domänen-Shader-Beschreibung erhalten.
ms.assetid: 02109930-0922-46b8-9381-bb75abd0c4a0
keywords:
- Getdomainshaderdesc-Methode Direct3D 11
- Getdomainshaderdesc-Methode Direct3D 11, ID3DX11EffectPass-Schnittstelle
- ID3DX11EffectPass-Schnittstelle Direct3D 11, getdomainshaderdesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDomainShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2157134d97332fc9c76267f5e0db49d2c40e96a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982432"
---
# <a name="id3dx11effectpassgetdomainshaderdesc-method"></a>ID3DX11EffectPass:: getdomainshaderdesc-Methode

Eine Domänen-Shader-Beschreibung erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDomainShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDE SC* 
</dt> <dd>

Typ: **[ **Bibliothek d3dx11 \_ Pass- \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)\***

Ein Zeiger auf eine Domänen-Shader-Beschreibung (siehe [**Bibliothek d3dx11 \_ Pass \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)).

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

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





