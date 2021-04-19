---
description: Legt ein Array von ganzen Zahlen fest.
ms.assetid: 4491bffd-ce5e-4f84-ac11-0314a1b16d63
title: 'ID3DXBaseEffect:: tartintarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetIntArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f76ff0d7f4bcc68d7cce85f3d02f2bc207a5f4b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367342"
---
# <a name="id3dxbaseeffectsetintarray-method"></a>ID3DXBaseEffect:: tartintarray-Methode

Legt ein Array von ganzen Zahlen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hParameter,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hparameter* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*PN* \[ in\]
</dt> <dd>

Typ: Konstante **[**int**](../winprog/windows-data-types.md) \***

Array von ganzen Zahlen.

</dd> <dt>

*Anzahl* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl von ganzen Zahlen im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**Getintarray**](id3dxbaseeffect--getintarray.md)
</dt> </dl>

 

 
