---
description: Legen Sie den Bereich eines Arrays fest, das an das Gerät übergeben werden soll.
ms.assetid: 43f1c258-770c-4756-9033-e5667b379fe6
title: ID3DXBaseEffect::SetArrayRange-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetArrayRange
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1cf4f51bfca29f1aa46238197818bb10bc4d0fe811218e5cedc59c24deb2446f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987630"
---
# <a name="id3dxbaseeffectsetarrayrange-method"></a>ID3DXBaseEffect::SetArrayRange-Methode

Legen Sie den Bereich eines Arrays fest, das an das Gerät übergeben werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetArrayRange(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Start,
  [in] UINT       Stop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hParameter* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Siehe [Handles (Direct3D 9).](handles.md)

</dd> <dt>

*Starten* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Starten sie den Index.

</dd> <dt>

*Beenden* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Index beenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
