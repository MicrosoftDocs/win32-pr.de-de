---
description: Erstellt eine Identitätsmatrix.
ms.assetid: 0dd6d4fb-284c-4d01-9a85-63aa08e71723
title: D3DXMatrixIdentity-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10dffa12a379754006ca65d1239be96632a68b93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961550"
---
# <a name="d3dxmatrixidentity-function"></a>D3DXMatrixIdentity-Funktion

Erstellt eine Identitätsmatrix.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixIdentity(
  _Inout_ D3DXMATRIX *pOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Identitätsmatrix ist.

## <a name="remarks"></a>Bemerkungen

Die Identitätsmatrix ist eine Matrix, in der alle Koeffizienten 0 (null) sind, mit Ausnahme der \[ 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4, 4 Koeffizienten \] , die auf 1 festgelegt sind. Die Identitätsmatrix ist ein besonderes, da Sie bei der Anwendung auf Vertices nicht geändert wird. Die Identitätsmatrix dient als Ausgangspunkt für Matrizen, die Scheitelpunkt Werte ändern, um Drehungen, Übersetzungen und andere Transformationen zu erstellen, die durch eine 4-X4-Matrix dargestellt werden können.

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixIdentity** -Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixIsIdentity**](d3dxmatrixisidentity.md)
</dt> </dl>

 

 




