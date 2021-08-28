---
description: 'ID3DXBaseEffect::SetMatrixTransposePointerArray-Methode: Legt ein Array von Zeigern auf transponierte Matrizen fest.'
ms.assetid: 11a21077-eeee-4d52-ac16-41444e3eca4f
title: ID3DXBaseEffect::SetMatrixTransposePointerArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9a1ed9fa363209cf861d3f11a3c71075cc9558bc7af42f90990bcba383dff6a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790650"
---
# <a name="id3dxbaseeffectsetmatrixtransposepointerarray-method"></a>ID3DXBaseEffect::SetMatrixTransposePointerArray-Methode

Legt ein Array von Zeigern auf transponierte Matrizen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hParameter* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Siehe [Handles (Direct3D 9).](handles.md)

</dd> <dt>

*ppMatrix* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***

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

Wenn die Zielmatrizen kleiner als die Quellmatrizen sind, werden die zusätzlichen Komponenten der Quellmatrizen ignoriert.

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

 

 
