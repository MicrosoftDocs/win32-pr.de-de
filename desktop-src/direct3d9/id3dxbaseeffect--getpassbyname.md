---
description: Ruft das Handle eines Durchlaufs ab, indem nach seinem Namen gesucht wird.
ms.assetid: 24d043a2-5c87-4a59-80d4-0c81bd7a0b3e
title: ID3DXBaseEffect::GetPassByName-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5837d2b69c793f788c4c89f648402e7924bc2f3af9a92bbbe596c133efe10d1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987760"
---
# <a name="id3dxbaseeffectgetpassbyname-method"></a>ID3DXBaseEffect::GetPassByName-Methode

Ruft das Handle eines Durchlaufs ab, indem nach seinem Namen gesucht wird.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetPassByName(
  [in] D3DXHANDLE hTechnique,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hTechnique* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle der übergeordneten Technik. Siehe [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeichenfolge, die den Passnamen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt das Handle des ersten Durchlaufs innerhalb der angegebenen Technik mit dem angegebenen Namen zurück, oder **NULL,** wenn der Name nicht gefunden wurde. Siehe [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
