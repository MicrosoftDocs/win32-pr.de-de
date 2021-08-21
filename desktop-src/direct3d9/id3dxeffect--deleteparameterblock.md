---
description: Löscht einen Parameterblock.
ms.assetid: 5502dabc-1703-481b-a69d-f6bd8fd01d20
title: ID3DXEffect::D eleteParameterBlock-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.DeleteParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a53d97bc077f830bdf73f5a184e253a8537626cbba575b2a5b9e74247ea48702
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494240"
---
# <a name="id3dxeffectdeleteparameterblock-method"></a>ID3DXEffect::D eleteParameterBlock-Methode

Löscht einen Parameterblock.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

 *hParameterBlock* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Ein Handle für den Parameterblock. Dies ist das handle, das von [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md)zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Parameterblöcke sind Blöcke mit Auswirkungszuständen. Verwenden Sie einen Parameterblock, um Zustandsänderungen aufzuzeichnen, damit sie später mit einem einzelnen API-Aufruf angewendet werden können. Wenn Sie den Parameterblock nicht mehr benötigen, löschen Sie den Parameterblock, um die Speicherauslastung zu reduzieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md)
</dt> </dl>

 

 




