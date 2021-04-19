---
description: Legt ein Array von nicht übersetzten Matrizen fest.
ms.assetid: 27f230bd-9aee-4673-aa70-5ecda541b1be
title: 'ID3DXTextureShader:: setmatrixarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b0545d48e16698f44cc48ad467f9454ac94db030
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363975"
---
# <a name="id3dxtextureshadersetmatrixarray-method"></a>ID3DXTextureShader:: setmatrixarray-Methode

Legt ein Array von nicht übersetzten Matrizen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMatrixArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hconstant* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für das Array konstanter Matrizen. Siehe [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pmatrix* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Array von nicht übersetzten Matrizen. Siehe [**D3DXMATRIX**](d3dxmatrix.md).

</dd> <dt>

*Anzahl* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl von Matrizen im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

Eine nicht übersetzte Matrix enthält Zeilen Hauptdaten; Das heißt, jeder Vektor ist in einer Zeile enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
