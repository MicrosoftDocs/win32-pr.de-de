---
description: Bestimmt, ob ein Parameter von der Technik verwendet wird.
ms.assetid: ac50c0d3-93d9-4477-a854-d0b53df28c90
title: ID3DXEffect::IsParameterUsed-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.IsParameterUsed
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 80b0e69ec4f46541840d5b381cd25d056b25240a00a9ae84b0aaf46a79295ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296001"
---
# <a name="id3dxeffectisparameterused-method"></a>ID3DXEffect::IsParameterUsed-Methode

Bestimmt, ob ein Parameter von der Technik verwendet wird.

## <a name="syntax"></a>Syntax


```C++
BOOL IsParameterUsed(
  [in] D3DXHANDLE hParameter,
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hParameter* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für den Parameter. Siehe [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*hTechnique* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für die Technik. Siehe [Handles (Direct3D 9)](handles.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Gibt **TRUE** zurück, wenn der Parameter verwendet wird, und **FALSE,** wenn der Parameter nicht verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
