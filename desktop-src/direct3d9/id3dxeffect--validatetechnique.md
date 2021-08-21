---
description: Überprüfen sie eine Technik.
ms.assetid: d69eaafa-da4d-4599-86fb-83d72e1664cc
title: ID3DXEffect::ValidateTechnique-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ValidateTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4ba3f6422c373c63a9b147ded8f288f642dcd880805cbd1d8b638b3f0e7f8f8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951700"
---
# <a name="id3dxeffectvalidatetechnique-method"></a>ID3DXEffect::ValidateTechnique-Methode

Überprüfen sie eine Technik.

## <a name="syntax"></a>Syntax


```C++
HRESULT ValidateTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hTechnique* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Siehe [Handles (Direct3D 9)](handles.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DERR \_ CONFLICTINGRENDERSTATE, D3DERR \_ CONFLICTINGTEXTUREFILTER, D3DERR \_ DEVICELOST, D3DERR \_ DRIVERINTERNALERROR, D3DERR \_ TOOMANYOPERATIONS, D3DERR \_ UNSUPPORTEDALP DLLG, D3DERR \_ UNSUPPORTEDALPHAOPERATION, D3DERR \_ UNSUPPORTEDCOLORARG, D3DERR \_ UNSUPPORTEDCOLOROPERATION, D3DERR \_ UNSUPPORTEDFACTORVALUE, D3DERR \_ UNSUPPORTEDTEXTUREFILTER UND D3DERR \_ WRONGTEXTUREFORMAT.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::SetTechnique**](id3dxeffect--settechnique.md)
</dt> </dl>

 

 




