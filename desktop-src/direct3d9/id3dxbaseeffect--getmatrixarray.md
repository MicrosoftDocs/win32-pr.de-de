---
description: Ruft ein Array von nicht übersetzten Matrizen ab.
ms.assetid: 37b08f55-22f1-4b60-8cd4-566a77e7dbd6
title: ID3DXBaseEffect::GetMatrixArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6d94820200cfc4cdc90c0a67562ac84efd57cd5cacb8e2a0ff37fcb91454db33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987790"
---
# <a name="id3dxbaseeffectgetmatrixarray-method"></a>ID3DXBaseEffect::GetMatrixArray-Methode

Ruft ein Array von nicht übersetzten Matrizen ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMatrixArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
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

*pMatrix* \[ out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Gibt ein Array von nicht übersetzten Matrizen zurück. Siehe [**D3DXMATRIX**](d3dxmatrix.md).

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

Eine nicht übersetzte Matrix enthält Zeilen-Hauptdaten. Das heißt, jeder Vektor ist in einer Zeile enthalten.

Wenn die Zielmatrizen größer als die Quellmatrizen sind, werden nur die linken oberen Komponenten jeder Zielmatrix gefüllt, und die verbleibenden Zielmatrixkomponenten werden auf 0 (null) festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetMatrixArray**](id3dxbaseeffect--setmatrixarray.md)
</dt> </dl>

 

 
