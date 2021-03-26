---
title: ID3DX11EffectPass getpixelshaderdesc-Methode (D3dx11effect. h)
description: Eine Pixel-shaderbeschreibung erhalten.
ms.assetid: 5772f197-7ac5-4492-9a41-eedb1a8b22c9
keywords:
- Getpixelshaderdesc-Methode Direct3D 11
- Getpixelshaderdesc-Methode Direct3D 11, ID3DX11EffectPass-Schnittstelle
- ID3DX11EffectPass-Schnittstelle Direct3D 11, getpixelshaderdesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetPixelShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c04479a58eed0aa94616f0ffc092f17d52d9af4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982246"
---
# <a name="id3dx11effectpassgetpixelshaderdesc-method"></a>ID3DX11EffectPass:: getpixelshaderdesc-Methode

Eine Pixel-shaderbeschreibung erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPixelShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDE SC* 
</dt> <dd>

Typ: **[ **Bibliothek d3dx11 \_ Pass- \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)\***

Ein Zeiger auf eine Pixel-Shader-Beschreibung (siehe [**Bibliothek d3dx11 \_ Pass \_ Shader \_**](d3dx11-pass-shader-desc.md)Debug).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.

## <a name="remarks"></a>Bemerkungen

Ein Effekt Durchlauf kann renderzustandszuweisungen und shaderobjektzuweisungen enthalten.

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

 

 





