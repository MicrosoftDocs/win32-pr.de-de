---
title: ID3DX11EffectPass GetVertexShaderDesc-Methode (D3dx11effect.h)
description: Abrufen einer Vertex-Shaderbeschreibung.
ms.assetid: 7e02a438-2ff4-4e32-bc16-d112aafa57cb
keywords:
- GetVertexShaderDesc-Methode Direct3D 11
- GetVertexShaderDesc-Methode Direct3D 11 , ID3DX11EffectPass-Schnittstelle
- ID3DX11EffectPass-Schnittstelle Direct3D 11 , GetVertexShaderDesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetVertexShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7942fc1f8202065ac904223693c70b4dc8ea70bf3421158a08bad253acc67567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045968"
---
# <a name="id3dx11effectpassgetvertexshaderdesc-method"></a>ID3DX11EffectPass::GetVertexShaderDesc-Methode

Abrufen einer Vertex-Shaderbeschreibung.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVertexShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDesc* 
</dt> <dd>

Typ: **[ **D3DX11 \_ PASS \_ SHADER \_ DESC**](d3dx11-pass-shader-desc.md)\***

Ein Zeiger auf eine Vertex-Shaderbeschreibung (siehe [**D3DX11 \_ PASS \_ SHADER \_ DESC**](d3dx11-pass-shader-desc.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Ein Effektdurchlauf kann Renderzustandszuweisungen und Shaderobjektzuweisungen enthalten.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





