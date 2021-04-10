---
description: Starten Sie die Erfassung von Zustandsänderungen in einem Parameter Block.
ms.assetid: cdf6f572-1a21-4c1d-a113-13b48bacd060
title: 'ID3DXEffect:: beginparameterblock-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 60a43304c8e0e3d64ac6469c1c075c57b5411e3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050866"
---
# <a name="id3dxeffectbeginparameterblock-method"></a>ID3DXEffect:: beginparameterblock-Methode

Starten Sie die Erfassung von Zustandsänderungen in einem Parameter Block.

## <a name="syntax"></a>Syntax


```C++
HRESULT BeginParameterBlock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

Statusänderungen des Erfassungs Effekts-Parameters, bis endparameterblock aufgerufen wird. Effektparameter enthalten alle Zustandsänderungen außerhalb eines bestanden. Löschen Sie Parameter Blöcke, wenn Sie durch Aufrufen von deleteparameterblock nicht mehr benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect:: endparameterblock**](id3dxeffect--endparameterblock.md)
</dt> <dt>

[**ID3DXEffect:: applyparameterblock**](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[**ID3DXEffect::D eleteparameterblock**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




