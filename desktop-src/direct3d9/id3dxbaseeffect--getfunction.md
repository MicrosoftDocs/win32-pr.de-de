---
description: Ruft das Handle einer Funktion ab.
ms.assetid: 97c82c28-4402-4605-8247-44d6f38bfa20
title: ID3DXBaseEffect::GetFunction-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunction
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ff3627c27ce6fa4eac0e166276a94dd5f4c1dd62bc4f8b38ccdd52c365a332fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094167"
---
# <a name="id3dxbaseeffectgetfunction-method"></a>ID3DXBaseEffect::GetFunction-Methode

Ruft das Handle einer Funktion ab.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetFunction(
  [in] UINT Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Funktionsindex.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt das Handle der angegebenen Funktion oder **NULL** zurück, wenn der Index ungültig war. Siehe [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
