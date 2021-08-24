---
description: 'ID3DXBaseEffect::SetMatrix-Methode: Legt eine nicht transponierte Matrix fest.'
ms.assetid: 90329460-756e-4b3e-9ff3-be9dc556eb9f
title: ID3DXBaseEffect::SetMatrix-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 77aad0573aed5e7dcb37ea82052b535badf8ee77d438393ad8d45e4963b79609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749010"
---
# <a name="id3dxbaseeffectsetmatrix-method"></a>ID3DXBaseEffect::SetMatrix-Methode

Legt eine nicht transponierte Matrix fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hParameter* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Siehe [Handles (Direct3D 9).](handles.md)

</dd> <dt>

*pMatrix* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine nicht übersetzte Matrix. Siehe [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Eine nicht transponierte Matrix enthält Zeilen-Hauptdaten. Anders ausgedrückt: Jeder Vektor ist in einer Zeile enthalten.

Wenn die Zielmatrix kleiner als die Quellmatrix ist, werden die zusätzlichen Komponenten der Quellmatrix ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetMatrix**](id3dxbaseeffect--getmatrix.md)
</dt> </dl>

 

 




