---
description: Ordnet dem ID3DXPRTBuffer-Objekt ein ID3DXTextureGutterHelper-Objekt zu.
ms.assetid: 095fea82-ac7a-42fa-990a-084715c73823
title: ID3DXPRTBuffer::AttachGH-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AttachGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: afb625c0f8db9d04737420ab386095bbe70b3e0f23e375f75c212da71e59b0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801948"
---
# <a name="id3dxprtbufferattachgh-method"></a>ID3DXPRTBuffer::AttachGH-Methode

Ordnet dem [**ID3DXPRTBuffer-Objekt**](id3dxprtbuffer.md) ein [**ID3DXTextureGutterHelper-Objekt**](id3dxtexturegutterhelper.md) zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachGH(
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pGH* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**

Zeiger auf die [**ID3DXTextureGutterHelper-Schnittstelle**](id3dxtexturegutterhelper.md) eines Objekts, das Textur-Gutterdaten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.

## <a name="remarks"></a>Hinweise

Der Verweiszähler des [**ID3DXTextureGutterHelper-Objekts**](id3dxtexturegutterhelper.md) wird automatisch um eins erhöht. Alle vorhandenen **ID3DXTextureGutterHelper-Zeiger** werden freigegeben.

Sie müssen sicherstellen, dass die Anzahl der **ID3DXPRTBuffer::AttachGH-Aufrufe** mit der Anzahl der [**ID3DXPRTBuffer::ReleaseGH-Aufrufe**](id3dxprtbuffer--releasegh.md) übereinstimmt. Nach dem Aufruf von **ID3DXPRTBuffer::ReleaseGH** sollte der von **ID3DXPRTBuffer::AttachGH** zurückgegebene pGH-Zeiger nicht mehr verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::ReleaseGH**](id3dxprtbuffer--releasegh.md)
</dt> </dl>

 

 




