---
title: ID3DX11EffectPass GetPixelShaderDesc-Methode (D3dx11effect.h)
description: Hier erhalten Sie eine Pixel-Shader-Beschreibung.
ms.assetid: 5772f197-7ac5-4492-9a41-eedb1a8b22c9
keywords:
- GetPixelShaderDesc-Methode Direct3D 11
- GetPixelShaderDesc-Methode Direct3D 11, ID3DX11EffectPass-Schnittstelle
- ID3DX11EffectPass-Schnittstelle Direct3D 11 , GetPixelShaderDesc-Methode
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
ms.openlocfilehash: 3684192d7fd70207a06eb5f4d6196c4414cd4c2b2fc45073230ea5912385c3b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535008"
---
# <a name="id3dx11effectpassgetpixelshaderdesc-method"></a>ID3DX11EffectPass::GetPixelShaderDesc-Methode

Hier erhalten Sie eine Pixel-Shader-Beschreibung.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPixelShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDesc* 
</dt> <dd>

Typ: **[ **D3DX11 \_ PASS \_ SHADER \_ DESC**](d3dx11-pass-shader-desc.md)\***

Ein Zeiger auf eine Pixel-Shader-Beschreibung (siehe [**D3DX11 \_ PASS \_ SHADER \_ DESC**](d3dx11-pass-shader-desc.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Ein Effektpass kann Renderzustandszuweisungen und Shaderobjektzuweisungen enthalten.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





