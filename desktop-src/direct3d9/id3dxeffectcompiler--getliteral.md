---
description: Ruft einen Literalstatus eines Parameters ab. Ein Literalparameter hat einen Wert, der sich während der Lebensdauer eines Effekts nicht ändert.
ms.assetid: 417abbee-5193-462e-b0d1-b4928ad0a041
title: ID3DXEffectCompiler::GetLiteral-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.GetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d5c4fcb9b4eb3ee102d4e0676985945cfa227aa35cbd939c8dcd5b8d51da4826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493940"
---
# <a name="id3dxeffectcompilergetliteral-method"></a>ID3DXEffectCompiler::GetLiteral-Methode

Ruft einen Literalstatus eines Parameters ab. Ein Literalparameter hat einen Wert, der sich während der Lebensdauer eines Effekts nicht ändert.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLiteral(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pLiteral
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hParameter* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für einen Parameter. Siehe [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pLiteral* \[ out\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)\***

Gibt True zurück, wenn der Parameter ein Literal ist, andernfalls FALSE.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Diese Methode ändert nur, ob der Parameter ein Literal ist oder nicht. Um den Wert eines Parameters zu ändern, verwenden Sie eine Methode wie [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) oder [**ID3DXBaseEffect::SetValue.**](id3dxbaseeffect--setvalue.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[Verwendungen und Literale (Direct3D 9)](usages-and-literals.md)
</dt> <dt>

[**ID3DXEffectCompiler::SetLiteral**](id3dxeffectcompiler--setliteral.md)
</dt> </dl>

 

 
