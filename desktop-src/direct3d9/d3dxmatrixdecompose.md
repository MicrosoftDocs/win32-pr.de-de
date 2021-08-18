---
description: 'D3DXMatrixDecompose-Funktion (D3dx9math.h): Unterbricht eine allgemeine 3D-Transformationsmatrix in ihre skalaren, drehlichen und übersetzungsbasierten Komponenten.'
ms.assetid: 73d3c248-1254-444e-9fd8-4f144424ddb7
title: D3DXMatrixDecompose-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDecompose
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffb6ce07713b4f66f4a85a678b5b28b589f8ae797c5a7b5c578ed136bbb9e3f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460390"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a>D3DXMatrixDecompose-Funktion (D3dx9math.h)

Unterteilen einer allgemeinen 3D-Transformationsmatrix in ihre skalaren, rotierten und übersetzungsübergreifenden Komponenten.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXMatrixDecompose(
  _Inout_       D3DXVECTOR3    *pOutScale,
  _Inout_       D3DXQUATERNION *pOutRotation,
  _Inout_       D3DXVECTOR3    *pOutTranslation,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOutScale* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf die Ausgabe [**D3DXVECTOR3,**](d3dxvector3.md) die Skalierungsfaktoren enthält, die entlang der x-, y- und z-Achsen angewendet werden.

</dd> <dt>

*pOutRotation* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die die Drehung beschreibt.

</dd> <dt>

*pOutTranslation* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf den [**D3DXVECTOR3-Vektor,**](d3dxvector3.md) der die Übersetzung beschreibt.

</dd> <dt>

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine [**D3DXMATRIX-Eingabematrix,**](d3dxmatrix.md) die zersetzt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




