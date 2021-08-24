---
description: Ruft eine nicht transposed Matrix ab.
ms.assetid: d507c82c-b1a5-4e83-8921-5d45f52faba0
title: ID3DXBaseEffect::GetMatrix-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f7733f37ae5db4bfdaf504f5e0925b89cea7a8f2e54f4546feb4141fddd246ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118860"
---
# <a name="id3dxbaseeffectgetmatrix-method"></a>ID3DXBaseEffect::GetMatrix-Methode

Ruft eine nicht transposed Matrix ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMatrix(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hParameter* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Siehe [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pMatrix* \[ out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Gibt eine nicht transposed Matrix zurück. Siehe [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Eine nicht transposed Matrix enthält Zeilen-Hauptdaten. Das heißt, jeder Vektor ist in einer Zeile enthalten.

Wenn die Zielmatrix größer als die Quellmatrix ist, werden nur die linken oberen Komponenten der Zielmatrix gefüllt, und die übrigen Komponenten werden auf 0 (null) festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetMatrix**](id3dxbaseeffect--setmatrix.md)
</dt> </dl>

 

 




