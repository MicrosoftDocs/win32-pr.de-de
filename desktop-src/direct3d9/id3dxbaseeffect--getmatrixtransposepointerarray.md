---
description: Ruft ein Array von Zeigern auf transponierte Matrizen ab.
ms.assetid: b859ff2f-cf62-4619-b8be-b940fa0513b3
title: ID3DXBaseEffect::GetMatrixTransposePointerArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTransposePointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 42014ed5a829f6dc0d45d7fe0dbcc96f52e945d47ae02b8effd217329e92bda8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118830"
---
# <a name="id3dxbaseeffectgetmatrixtransposepointerarray-method"></a>ID3DXBaseEffect::GetMatrixTransposePointerArray-Methode

Ruft ein Array von Zeigern auf transponierte Matrizen ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMatrixTransposePointerArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX **ppMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hParameter* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Siehe [Handles (Direct3D 9).](handles.md)

</dd> <dt>

*ppMatrix* \[ out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\*\***

Array von Zeigern auf transponierte Matrizen. Siehe [**D3DXMATRIX**](d3dxmatrix.md).

</dd> <dt>

*Anzahl* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Matrizen im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Eine transponierte Matrix enthält Spalten-Hauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.

Wenn die Zielmatrizen größer als die Quellmatrizen sind, werden nur die linken oberen Komponenten jeder Zielmatrix gefüllt, und die verbleibenden Zielmatrixkomponenten werden auf 0 (null) festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetMatrixTransposeArray**](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
