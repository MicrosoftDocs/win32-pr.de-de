---
description: Legt balyzentrierte Texelkoordinaten fest.
ms.assetid: 6c7c74aa-71a3-45aa-9b18-6409fbd63bda
title: ID3DXTextureGutterHelper::SetBaryMap-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6a82a28308b3236d81159a555219f2a459dd7d9738f1d42f22148af343da5f0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893230"
---
# <a name="id3dxtexturegutterhelpersetbarymap-method"></a>ID3DXTextureGutterHelper::SetBaryMap-Methode

Legt balyzentrierte Texelkoordinaten fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetBaryMap(
  [in] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pBaryData* \[ In\]
</dt> <dd>

Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Zeiger auf eine [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) die die ersten beiden baryzentrierten Koordinaten der einzelnen Texel enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Hinweise

Die dritte baryzentrierte Koordinate wird angegeben durch:


```
1 - ( pBaryData.x + pBaryData.y )
```



Die baryzentrierten Koordinaten, die in diese Methode eingegeben werden, sind nur für gültige Texel (keine Klasse 0) gültig. [**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) gibt werte, die nicht null sind, für gültige Texel zurück.

Baryzentrierte Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkt des Dreiecks. Eine detailliertere Beschreibung der baryzentrierten Koordinaten finden Sie unter [Beschreibung der baryzentrierten Koordinaten von Mathworld.](http://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




