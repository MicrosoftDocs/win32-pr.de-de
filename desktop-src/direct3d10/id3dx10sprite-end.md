---
description: Rufen Sie dies nach ID3DX10Sprite::Flush auf. Wenn D3DX10 SPRITE SAVE STATE angegeben wurde, als ID3DX10Sprite::Begin aufgerufen wurde, stellt diese API den Gerätestatus wie vor dem Aufruf von \_ \_ \_ ID3DX10Sprite::Begin wieder bereit.
ms.assetid: 71645edb-be4a-4d87-9fb0-557cf5cf10e5
title: ID3DX10Sprite::End-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.End
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 02cfa1e92275230bd3a853aa9079187181089c46b4e4f193404b9dc0c709c9e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302289"
---
# <a name="id3dx10spriteend-method"></a>ID3DX10Sprite::End-Methode

Rufen Sie dies nach ID3DX10Sprite::Flush auf. Wenn D3DX10 SPRITE SAVE STATE angegeben wurde, als ID3DX10Sprite::Begin aufgerufen wurde, stellt diese API den Gerätestatus wie vor dem Aufruf von \_ \_ \_ ID3DX10Sprite::Begin wieder bereit.

## <a name="syntax"></a>Syntax


```C++
HRESULT End();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




