---
description: Ruft die Texturkoordinaten (u, v) der einzelnen Texel ab.
ms.assetid: 7d8eecf8-6344-4a48-8338-b92ebb0ab2ef
title: ID3DXTextureGutterHelper::GetTexelMap-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 321f5075bdfde3a5a3d707089867356b3f702230dd81d2a1c29b513a8cf8e1ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800373"
---
# <a name="id3dxtexturegutterhelpergettexelmap-method"></a>ID3DXTextureGutterHelper::GetTexelMap-Methode

Ruft die Texturkoordinaten (u, v) der einzelnen Texel ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTexelMap(
  [out] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTexelData* \[ out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Zeiger auf die Position in Pixel-Texturkoordinaten (u, v), an der sich die einzelnen Texel befinden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Hinweise

Für Die Texturkoordinaten der Klassen 2 und [**4**](id3dxtexturegutterhelper.md)entsprechen die zurückgegebenen Texturkoordinaten (u, v) dem nächstgelegenen Punkt am nächsten Dreieck.

Die Anwendung muss pTexelData zuordnen und verwalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




