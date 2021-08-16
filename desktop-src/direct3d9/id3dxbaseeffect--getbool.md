---
description: Ruft einen BOOL-Wert ab.
ms.assetid: 9d61efcd-f267-4c45-b685-d363588796f7
title: ID3DXBaseEffect::GetBool-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetBool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 13fa69c8fd20798f683003bd561193a4079ba48c291248f7d4ce6fe1d0fc5fe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522319"
---
# <a name="id3dxbaseeffectgetbool-method"></a>ID3DXBaseEffect::GetBool-Methode

Ruft einen BOOL-Wert ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBool(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pb
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hParameter* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Siehe [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pb* \[ out\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)\***

Gibt einen booleschen Wert zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetBool**](id3dxbaseeffect--setbool.md)
</dt> </dl>

 

 
