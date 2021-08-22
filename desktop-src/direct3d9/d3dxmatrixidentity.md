---
description: Erstellt eine Identitätsmatrix.
ms.assetid: 0dd6d4fb-284c-4d01-9a85-63aa08e71723
title: D3DXMatrixIdentity-Funktion (D3dx9math.h)
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
ms.openlocfilehash: ce7d891eb446372b749c7085a37e80241c52f1cf862a61b3fc9edeb544776b2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044897"
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

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Identitätsmatrix ist.

## <a name="remarks"></a>Hinweise

Die Identitätsmatrix ist eine Matrix, in der alle Koeffizienten 0 sind, mit Ausnahme der \[ \] Koeffizienten \[ 1,1 2,2 \] \[ 3,3 \] \[ 4,4, \] die auf 1 festgelegt sind. Die Identitätsmatrix ist besonders, da sie unverändert bleibt, wenn sie auf Scheitelpunkte angewendet wird. Die Identitätsmatrix wird als Ausgangspunkt für Matrizen verwendet, die Scheitelpunktwerte ändern, um Drehungen, Übersetzungen und andere Transformationen zu erstellen, die durch eine 4 x4-Matrix dargestellt werden können.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixIdentity-Funktion** als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixIsIdentity**](d3dxmatrixisidentity.md)
</dt> </dl>

 

 




