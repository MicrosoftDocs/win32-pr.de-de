---
description: Ruft balyzentrierte Texelkoordinaten ab.
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: ID3DXTextureGutterHelper::GetBaryMap-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4183bf9bfa5065595073b8534e978367c3ec16bf76245d639da81292641afa81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729199"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a>ID3DXTextureGutterHelper::GetBaryMap-Methode

Ruft balyzentrierte Texelkoordinaten ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBaryMap(
  [in, out] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pBaryData* \[ in, out\]
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



Baryzentrierte Koordinaten werden immer in Bezug auf das von [**ID3DXTextureGutterHelper::GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md)zurückgegebene Dreieck angegeben.

Die von dieser Methode zurückgegebenen baryzentrierten Koordinaten sind nur für gültige Texel (nicht der Klasse 0) gültig. [**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) gibt Werte ungleich 0 (null) für gültige Texel zurück.

[**Texel der**](id3dxtexturegutterhelper.md) Klasse 2 werden dem nächstgelegenen Punkt im Dreieck im Texelbereich zugeordnet.

Die Anwendung muss pBaryData zuordnen und verwalten.

Baryzentrierte Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkt des Dreiecks. Eine detailliertere Beschreibung der baryzentrierten Koordinaten finden Sie unter [Beschreibung der baryzentrierten Koordinaten von Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




