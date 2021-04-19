---
description: Überprüfen Sie eine Technik.
ms.assetid: d69eaafa-da4d-4599-86fb-83d72e1664cc
title: 'ID3DXEffect:: validatetechnique-Methode (D3DX9Effect. h)'
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
ms.openlocfilehash: b48ffa8707a3f78e76555d57225c11f89160fdd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370413"
---
# <a name="id3dxeffectvalidatetechnique-method"></a>ID3DXEffect:: validatetechnique-Methode

Überprüfen Sie eine Technik.

## <a name="syntax"></a>Syntax


```C++
HRESULT ValidateTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*htechnik* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DERR \_ conflictingrenderstate, D3DERR \_ conflictingtexturefilter, D3DERR \_ DeviceLost, D3DERR \_ driverinternalerror, D3DERR \_ toomanyoperations, D3DERR \_ unsupportedalphaarg, D3DERR \_ unsupportedalphaoperation, D3DERR \_ unsupportedcolorarg, D3DERR \_ unsupportedcoloroperation, D3DERR \_ unsupportedfactor Value, D3DERR \_ unsupportedtexturefilter und D3DERR \_ fehlertextureformat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect:: settechnique**](id3dxeffect--settechnique.md)
</dt> </dl>

 

 




