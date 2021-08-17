---
description: Berechnet die umschließende Kugel aller Gitternetze in der Rahmenhierarchie.
ms.assetid: 8c3f5a9e-73ff-4d83-8f85-a3fc2a9a53f7
title: D3DXFrameCalculateBoundingSphere-Funktion (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameCalculateBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a8a4706fcbd421072e2b82cd9e228fe24c35651c17ce4ab0f48e05b946946fb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123216"
---
# <a name="d3dxframecalculateboundingsphere-function"></a>D3DXFrameCalculateBoundingSphere-Funktion

Berechnet die umschließende Kugel aller Gitternetze in der Rahmenhierarchie.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXFrameCalculateBoundingSphere(
  _In_  const D3DXFRAME     *pFrameRoot,
  _Out_       LPD3DXVECTOR3 pObjectCenter,
  _Out_       FLOAT         *pObjectRadius
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFrameRoot* \[ In\]
</dt> <dd>

Typ: **const [**D3DXFRAME**](d3dxframe.md) \***

Zeiger auf den Stammknoten.

</dd> <dt>

*pObjectCenter* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXVECTOR3**](d3dxvector3.md)**

Gibt die Mitte der umgebenden Kugel zurück.

</dd> <dt>

*pObjectRadius* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Gibt den Radius der umgebenden Kugel zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Animationsfunktionen](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
