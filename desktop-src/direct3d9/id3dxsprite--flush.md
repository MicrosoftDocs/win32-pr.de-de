---
description: Erzwingt, dass alle Batch-Sprites an das Gerät übermittelt werden. Gerätezustände bleiben unverändert nach dem letzten Aufruf von ID3DXSprite::Begin. Die Liste der Batch-Sprites wird dann gelöscht.
ms.assetid: e5717bde-e339-4344-8ce7-b0c3fe118887
title: ID3DXSprite::Flush-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Flush
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 766fbe41491fc6861ac3eaf366c3a858870c560139f1048d405184b580e72229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292692"
---
# <a name="id3dxspriteflush-method"></a>ID3DXSprite::Flush-Methode

Erzwingt, dass alle Batch-Sprites an das Gerät übermittelt werden. Gerätezustände bleiben unverändert nach dem letzten Aufruf von [**ID3DXSprite::Begin**](id3dxsprite--begin.md). Die Liste der Batch-Sprites wird dann gelöscht.

## <a name="syntax"></a>Syntax


```C++
HRESULT Flush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite::End**](id3dxsprite--end.md)
</dt> </dl>

 

 




