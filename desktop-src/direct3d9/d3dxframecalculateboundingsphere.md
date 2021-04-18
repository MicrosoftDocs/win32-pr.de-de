---
description: Berechnet die umgebende Kugel aller Netze in der Frame Hierarchie.
ms.assetid: 8c3f5a9e-73ff-4d83-8f85-a3fc2a9a53f7
title: D3DXFrameCalculateBoundingSphere-Funktion (D3dx9anim. h)
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
ms.openlocfilehash: f10043d2c897bf6ab24c442b8e134f31221c498e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371913"
---
# <a name="d3dxframecalculateboundingsphere-function"></a>D3DXFrameCalculateBoundingSphere-Funktion

Berechnet die umgebende Kugel aller Netze in der Frame Hierarchie.

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

*pframeroot* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXFRAME**](d3dxframe.md) \***

Zeiger auf den Stamm Knoten.

</dd> <dt>

*pobjectcenter* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXVECTOR3**](d3dxvector3.md)**

Gibt den Mittelpunkt der umgebenden Kugel zurück.

</dd> <dt>

*pobjectradius* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Gibt den Radius der umgebenden Kugel zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Animations Funktionen](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
