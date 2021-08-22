---
description: Beenden Sie die Erfassung von Änderungen am Auswirkungsparameterzustand.
ms.assetid: b6ca2917-2df0-4f3a-9ee3-23e9d2501ff4
title: ID3DXEffect::EndParameterBlock-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b1d68aa1bd716ee106a5d1588a7a7060adb851185115e97d2f5f2a5d7f857c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494230"
---
# <a name="id3dxeffectendparameterblock-method"></a>ID3DXEffect::EndParameterBlock-Methode

Beenden Sie die Erfassung von Änderungen am Auswirkungsparameterzustand.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE EndParameterBlock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt ein Handle für den Parameterzustandsblock zurück.

## <a name="remarks"></a>Hinweise

Alle Effektparameter, die den Zustand ändern (nach dem Aufruf von BeginParameterBlock und vor dem Aufruf von EndParameterBlock), werden in einem Effect-Parameterzustandsblock gespeichert. Verwenden Sie ApplyParameterBlock, um diesen Block von Zustandsänderungen auf das Effektsystem anzuwenden. Sobald Sie mit einem Zustandsblock fertig sind, verwenden Sie DeleteParameterBlock, um den Arbeitsspeicher frei zu geben.

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

[**ID3DXEffect::ApplyParameterBlock**](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[**ID3DXEffect::D eleteParameterBlock**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




