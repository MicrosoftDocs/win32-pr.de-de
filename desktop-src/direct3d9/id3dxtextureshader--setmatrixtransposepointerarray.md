---
description: Legt ein Array von Zeigern auf umgesetzte Matrizen fest.
ms.assetid: 2b9f1efe-b2ea-416b-a370-202db57b1925
title: 'ID3DXTextureShader:: setmatrixtransposepointerarray-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: cd7c81dcb0fd9b9354c2536a91abaebfe8e4315b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365099"
---
# <a name="id3dxtextureshadersetmatrixtransposepointerarray-method"></a>ID3DXTextureShader:: setmatrixtransposepointerarray-Methode

Legt ein Array von Zeigern auf umgesetzte Matrizen fest.

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

*hconstant* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für das Array von Matrix Konstanten. Siehe [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*ppmatrix* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \* \***

Array von Zeigern auf umgesetzte Matrizen. Siehe [**D3DXMATRIX**](d3dxmatrix.md).

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

Eine umgesetzte Matrix enthält Spalten Hauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
