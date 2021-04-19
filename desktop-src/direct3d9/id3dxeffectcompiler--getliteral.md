---
description: Ruft den literalstatus eines Parameters ab. Ein literalparameter weist einen Wert auf, der sich während der Lebensdauer eines Effekts nicht ändert.
ms.assetid: 417abbee-5193-462e-b0d1-b4928ad0a041
title: 'ID3DXEffectCompiler:: getliteralmethode (D3DX9Shader. h)'
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
ms.openlocfilehash: c16e3798ab66a34e12812a3560572c45b9206b30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364352"
---
# <a name="id3dxeffectcompilergetliteral-method"></a>ID3DXEffectCompiler:: getliteralmethode

Ruft den literalstatus eines Parameters ab. Ein literalparameter weist einen Wert auf, der sich während der Lebensdauer eines Effekts nicht ändert.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLiteral(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pLiteral
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hparameter* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für einen Parameter. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pliteral* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)\***

Gibt true zurück, wenn der-Parameter ein Literalwert ist, andernfalls false.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

Diese Methoden ändern nur, ob der Parameter ein Literalwert ist oder nicht. Um den Wert eines Parameters zu ändern, verwenden Sie eine Methode wie [**ID3DXBaseEffect:: SetBool**](id3dxbaseeffect--setbool.md) oder [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[Verwendungen und Literale (Direct3D 9)](usages-and-literals.md)
</dt> <dt>

[**ID3DXEffectCompiler:: setliteral**](id3dxeffectcompiler--setliteral.md)
</dt> </dl>

 

 
