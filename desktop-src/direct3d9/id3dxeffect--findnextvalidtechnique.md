---
description: Sucht nach der nächsten gültigen Technik, beginnend bei der Technik nach der angegebenen Technik.
ms.assetid: 0d2f3f80-90fd-495d-acb8-075f50e9a974
title: ID3DXEffect::FindNextValidTechnique-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.FindNextValidTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f65a08d1f1ec8a1f7710272d2a1c48e936f211b3bcdee8b84652b9a7196f39e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118700"
---
# <a name="id3dxeffectfindnextvalidtechnique-method"></a>ID3DXEffect::FindNextValidTechnique-Methode

Sucht nach der nächsten gültigen Technik, beginnend bei der Technik nach der angegebenen Technik.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindNextValidTechnique(
  [in]  D3DXHANDLE hTechnique,
  [out] D3DXHANDLE *pTechnique
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hTechnique* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für eine Technik. Siehe [Handles (Direct3D 9).](handles.md) Geben **Sie NULL** für diesen Parameter an, um das erste gültige Verfahren zu finden.

</dd> <dt>

*pTechnique* \[ out\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***

Zeiger auf einen Bezeichner für die nächste Technik. **NULL** wird zurückgegeben, wenn dies die letzte Technik ist. Siehe [Handles (Direct3D 9).](handles.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**D3DXTECHNIQUE \_ DESC**](d3dxtechnique-desc.md)
</dt> <dt>

[**ID3DXEffect::ValidateTechnique**](id3dxeffect--validatetechnique.md)
</dt> </dl>

 

 




