---
description: Gibt das Quadrat der Länge eines 3D-Vektors zurück.
ms.assetid: 25dc50cc-542b-4989-a858-9b37603393a0
title: D3DXVec3LengthSq-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3LengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bb7d17d4f1bc06d68a73a2cff9288d159381387
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355843"
---
# <a name="d3dxvec3lengthsq-function"></a>D3DXVec3LengthSq-Funktion

Gibt das Quadrat der Länge eines 3D-Vektors zurück.

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXVec3LengthSq(
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PV* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Ein Zeiger auf die Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **float**](../winprog/windows-data-types.md)**

Die Quadrat Länge des Vektors.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Length**](d3dxvec3length.md)
</dt> </dl>

 

 
