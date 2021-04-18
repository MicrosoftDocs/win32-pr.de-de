---
description: Gibt die Länge einer Quaternion zurück.
ms.assetid: daa835c2-2370-4427-a4ca-eddfb43d5c67
title: D3DXQuaternionLength-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f54136e7e34ba05442f98b25438dd03b7b5f211
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394213"
---
# <a name="d3dxquaternionlength-function"></a>D3DXQuaternionLength-Funktion

Gibt die Länge einer Quaternion zurück.

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXQuaternionLength(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PQ* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***

Ein Zeiger auf die Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **float**](../winprog/windows-data-types.md)**

Die Länge der Quaternion.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionLengthSq**](d3dxquaternionlengthsq.md)
</dt> </dl>

 

 
