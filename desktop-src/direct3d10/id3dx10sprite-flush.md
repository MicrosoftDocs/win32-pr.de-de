---
description: Erzwingen Sie, dass alle Batch-Sprites an das Gerät übermittelt werden. Gerätezustände bleiben unverändert nach dem letzten Aufruf von ID3DX10Sprite::Begin. Die Liste der Batch-Sprites wird dann gelöscht.
ms.assetid: ae03e17c-1a14-4a41-a9a9-8757d2f7a81d
title: ID3DX10Sprite::Flush-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Flush
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d74c96ebab8b1e174a44124aaa53b714a9ea860fc9fa2ea5ae3e25c9779aae01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302243"
---
# <a name="id3dx10spriteflush-method"></a>ID3DX10Sprite::Flush-Methode

Erzwingen Sie, dass alle Batch-Sprites an das Gerät übermittelt werden. Gerätezustände bleiben unverändert nach dem letzten Aufruf von ID3DX10Sprite::Begin. Die Liste der Batch-Sprites wird dann gelöscht.

## <a name="syntax"></a>Syntax


```C++
HRESULT Flush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.

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

 

 




