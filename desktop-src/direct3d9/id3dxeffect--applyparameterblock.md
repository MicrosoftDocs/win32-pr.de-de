---
description: Wenden Sie die Werte in einem Zustandsblock auf den systemstatus der aktuellen Auswirkung an.
ms.assetid: f228e2a2-64fa-4354-9f49-42d1d3b12d50
title: ID3DXEffect::ApplyParameterBlock-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ApplyParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8f5a382823da73df68ec0c32e120c0e94a2a7deba86e6aac4afe01e4e46acd7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951800"
---
# <a name="id3dxeffectapplyparameterblock-method"></a>ID3DXEffect::ApplyParameterBlock-Methode

Wenden Sie die Werte in einem Zustandsblock auf den systemstatus der aktuellen Auswirkung an.

## <a name="syntax"></a>Syntax


```C++
HRESULT ApplyParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

 *hParameterBlock* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Ein Handle für den Parameterblock. Dies ist das handle, das von [**ID3DXEffect::EndParameterBlock zurückgegeben wird.**](id3dxeffect--endparameterblock.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Capture effect-Parameterzustandsänderungen in einem Parameterblock durch Aufrufen von BeginParameterBlock; Beenden Sie die Erfassung von Zustandsänderungen, indem Sie EndParameterBlock aufrufen. Diese Zustandsänderungen umfassen alle Änderungen von Effektparametern, die innerhalb einer Technik auftreten (einschließlich der Änderungen außerhalb eines Durchgangs). Wenn Sie mit dem Parameterblock fertig sind, rufen Sie DeleteParameterBlock auf, um Arbeitsspeicher wiederhergestellt zu haben.

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
</dt> <dt>

[**ID3DXEffect::D eleteParameterBlock**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




