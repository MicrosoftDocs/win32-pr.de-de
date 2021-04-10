---
description: Beendet die Erfassung von Effekt-Parameter Zustandsänderungen.
ms.assetid: b6ca2917-2df0-4f3a-9ee3-23e9d2501ff4
title: 'ID3DXEffect:: endparameterblock-Methode (D3DX9Effect. h)'
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
ms.openlocfilehash: 3359e3b923d05e003ffbda18791e497d18ba627e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961622"
---
# <a name="id3dxeffectendparameterblock-method"></a>ID3DXEffect:: endparameterblock-Methode

Beendet die Erfassung von Effekt-Parameter Zustandsänderungen.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE EndParameterBlock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt ein Handle für den Parameter Status Block zurück.

## <a name="remarks"></a>Bemerkungen

Alle Effektparameter, die den Zustand ändern (nach dem Aufrufen von beginparameterblock und vor dem Aufrufen von endparameterblock), werden in einem Effektparameter-Zustands Block gespeichert. Verwenden Sie applyparameterblock, um diesen Block von Zustandsänderungen auf das Effektsystem anzuwenden. Wenn Sie mit einem Zustands Block fertig sind, verwenden Sie deleteparameterblock, um den Arbeitsspeicher freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect:: beginparameterblock**](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[**ID3DXEffect:: applyparameterblock**](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[**ID3DXEffect::D eleteparameterblock**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




