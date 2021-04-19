---
description: 'Erzwingt, dass alle Batch-Sprites an das Gerät übermittelt werden. Gerätezustände verbleiben nach dem letzten ID3DXSprite:: begin-Rückruf. Die Liste der im Batch verarbeiteten Sprites wird dann gelöscht.'
ms.assetid: e5717bde-e339-4344-8ce7-b0c3fe118887
title: 'ID3DXSprite:: Flush-Methode (D3dx9core. h)'
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
ms.openlocfilehash: 3bcd89984672f0dcfa2df120ede1abdfee23d171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367381"
---
# <a name="id3dxspriteflush-method"></a>ID3DXSprite:: Flush-Methode

Erzwingt, dass alle Batch-Sprites an das Gerät übermittelt werden. Gerätezustände verbleiben nach dem letzten [**ID3DXSprite:: begin**](id3dxsprite--begin.md)-Rückruf. Die Liste der im Batch verarbeiteten Sprites wird dann gelöscht.

## <a name="syntax"></a>Syntax


```C++
HRESULT Flush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite:: End**](id3dxsprite--end.md)
</dt> </dl>

 

 




