---
description: 'D3DXMatrixDecompose-Funktion (D3DX10Math.h): Unterteilt eine allgemeine 3D-Transformationsmatrix in ihre Skalar-, Drehungs- und Übersetzungskomponenten.'
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: D3DXMatrixDecompose-Funktion (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: be91b4b8ef6b0a18dc7691eb230ae755db31173ab8e42ab8ef0fb105d23630c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498140"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a>D3DXMatrixDecompose-Funktion (D3DX10Math.h)

Unterteilt eine allgemeine 3D-Transformationsmatrix in ihre Skalar-, Drehungs- und Übersetzungskomponenten.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOutScale* \[ In\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Zeiger auf die [**D3DXVECTOR3-Ausgabe,**](d3d10-d3dxvector3.md) die Skalierungsfaktoren enthält, die auf die x-, y- und z-Achse angewendet werden.

</dd> <dt>

*pOutRotation* \[ In\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf [**D3DXQUATERNION,**](d3d10-d3dxquaternion.md) der die Drehung beschreibt.

</dd> <dt>

*pOutTranslation* \[ In\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Zeiger auf den D3DXVECTOR3-Vektor, der die Übersetzung beschreibt.

</dd> <dt>

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf eine zu zerlegende [**D3DXMATRIX-Eingabematrix.**](d3d10-d3dxmatrix.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
