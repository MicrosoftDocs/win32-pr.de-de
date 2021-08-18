---
description: Legt die aktive Technik fest.
ms.assetid: 18f19773-a9f8-47f9-9334-acc95e0f0eb7
title: ID3DXEffect::SetTechnique-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7b10190df7c4527535a35c2c352933ec652452d51804e23b8aad338e6ca40522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987544"
---
# <a name="id3dxeffectsettechnique-method"></a>ID3DXEffect::SetTechnique-Methode

Legt die aktive Technik fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hTechnique* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiges Handle für die Technik. Siehe [Handles (Direct3D 9)](handles.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




