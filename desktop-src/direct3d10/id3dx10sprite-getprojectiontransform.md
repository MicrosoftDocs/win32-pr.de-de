---
description: Holen Sie sich die Sprite-Projektions Matrix, die auf alle Sprites angewendet wird.
ms.assetid: aee65a9f-27f9-42d9-98eb-ae90fc18c7f5
title: 'ID3DX10Sprite:: getprojectiontransform-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eefd526fbe32158505db1edc73b9bbf527ad99be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762381"
---
# <a name="id3dx10spritegetprojectiontransform-method"></a>ID3DX10Sprite:: getprojectiontransform-Methode

Holen Sie sich die Sprite-Projektions Matrix, die auf alle Sprites angewendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProjectionTransform(
  [out] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pprojectiontransform* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf ein [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) -Wert, der auf die Projektions Matrix des Sprite festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
