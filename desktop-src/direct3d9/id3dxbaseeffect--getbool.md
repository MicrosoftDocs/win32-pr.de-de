---
description: Ruft einen booleschen Wert ab.
ms.assetid: 9d61efcd-f267-4c45-b685-d363588796f7
title: 'ID3DXBaseEffect:: getBool-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: 0476c62733379a7e92aca55c3cdc2c31a3526de2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367493"
---
# <a name="id3dxbaseeffectgetbool-method"></a>ID3DXBaseEffect:: getBool-Methode

Ruft einen booleschen Wert ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBool(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pb
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hparameter* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*PB* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)\***

Gibt einen booleschen Wert zurück.

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

[**SetBool**](id3dxbaseeffect--setbool.md)
</dt> </dl>

 

 
