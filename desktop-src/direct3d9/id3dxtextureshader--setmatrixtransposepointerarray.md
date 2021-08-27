---
description: 'ID3DXTextureShader::SetMatrixTransposePointerArray-Methode: Legt ein Array von Zeigern auf transponierte Matrizen fest.'
ms.assetid: 2b9f1efe-b2ea-416b-a370-202db57b1925
title: ID3DXTextureShader::SetMatrixTransposePointerArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5bbfee8dd7366bbfb3b17aa83708f5d54f3a8b460b2dfab4a7cdc587b3d40d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800220"
---
# <a name="id3dxtextureshadersetmatrixtransposepointerarray-method"></a>ID3DXTextureShader::SetMatrixTransposePointerArray-Methode

Legt ein Array von Zeigern auf transponierte Matrizen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hConstant* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für das Array von Matrixkonstanten. Siehe [D3DXHANDLE](d3dxfx.md).

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

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Eine transponierte Matrix enthält Spaltenhauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
