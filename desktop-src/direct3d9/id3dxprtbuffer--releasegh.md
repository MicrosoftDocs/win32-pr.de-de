---
description: Die Zuordnung eines angefügten ID3DXTextureGutterHelper-Objekts zum ID3DXPRTBuffer-Objekt wird nicht zugeordnet.
ms.assetid: 0bd8322a-8af1-4173-bbe3-9134c831cf3a
title: ID3DXPRTBuffer::ReleaseGH-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ReleaseGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5691fc2601624733bb8d41b63140b694bd78027e0f6d548b02984bbc12406a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120534"
---
# <a name="id3dxprtbufferreleasegh-method"></a>ID3DXPRTBuffer::ReleaseGH-Methode

Die Zuordnung eines angefügten [**ID3DXTextureGutterHelper-Objekts**](id3dxtexturegutterhelper.md) zum [**ID3DXPRTBuffer-Objekt wird**](id3dxprtbuffer.md) nicht zugeordnet.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReleaseGH();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.

## <a name="remarks"></a>Hinweise

Diese Methode gibt den Zeiger auf die [**ID3DXTextureGutterHelper-Schnittstelle**](id3dxtexturegutterhelper.md) frei.

Sie müssen sicherstellen, dass die Anzahl der [**ID3DXPRTBuffer::AttachGH-Aufrufe**](id3dxprtbuffer--attachgh.md) der Anzahl der **ID3DXPRTBuffer::ReleaseGH-Aufrufe** entspricht. Nach dem **Aufruf von ID3DXPRTBuffer::ReleaseGH** sollte der von **ID3DXPRTBuffer::AttachGH** zurückgegebene pGH-Zeiger nicht mehr verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::AttachGH**](id3dxprtbuffer--attachgh.md)
</dt> </dl>

 

 




