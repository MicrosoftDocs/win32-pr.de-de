---
description: Ruft ein Array der übersetzten Matrizen ab.
ms.assetid: fbfcb2e4-82ca-4f79-923e-35749c5b9586
title: 'ID3DXBaseEffect:: getmatrixtransposearray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTransposeArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c5f3709a31067b82e9752a9e97db6f3a2a323a19
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762357"
---
# <a name="id3dxbaseeffectgetmatrixtransposearray-method"></a>ID3DXBaseEffect:: getmatrixtransposearray-Methode

Ruft ein Array der übersetzten Matrizen ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMatrixTransposeArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hparameter* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pmatrix* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Gibt ein Array der übersetzten Matrizen zurück. Siehe [**D3DXMATRIX**](d3dxmatrix.md).

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

Wenn die Ziel Matrizen größer als die Quell Matrizen sind, werden nur die linken oberen Komponenten der einzelnen Ziel Matrix gefüllt, und die restlichen Ziel Matrixkomponenten werden auf 0 (null) festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**Setmatrixtransposearray**](id3dxbaseeffect--setmatrixtransposearray.md)
</dt> </dl>

 

 
