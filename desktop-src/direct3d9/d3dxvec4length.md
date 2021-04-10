---
description: Gibt die Länge eines 4D-Vektors zurück.
ms.assetid: cb332160-3e3d-41b9-bfb0-e3b743d2eafd
title: D3DXVec4Length-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ea16c6406c217f5e5d76af68a5da3a0c8bd17b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961774"
---
# <a name="d3dxvec4length-function"></a>D3DXVec4Length-Funktion

Gibt die Länge eines 4D-Vektors zurück.

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXVec4Length(
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PV* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Ein Zeiger auf die Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **float**](../winprog/windows-data-types.md)**

Die Länge des Vektors.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec4LengthSq**](d3dxvec4lengthsq.md)
</dt> </dl>

 

 
