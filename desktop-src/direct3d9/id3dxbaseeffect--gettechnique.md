---
description: Ruft das Handle einer Technik ab.
ms.assetid: da139706-734b-4d5e-896d-52f045942218
title: ID3DXBaseEffect::GetTechnique-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6d193e08bf40ac67ba46218e9ce3e11b510d7014239a09b1c1b0000be5ec9420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987740"
---
# <a name="id3dxbaseeffectgettechnique-method"></a>ID3DXBaseEffect::GetTechnique-Methode

Ruft das Handle einer Technik ab.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetTechnique(
  [in] UINT Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Technikindex.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt das Handle der angegebenen Technik oder **NULL** zurück, wenn der Index ungültig war. Siehe [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
