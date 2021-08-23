---
description: Stellt den Gerätestatus wieder in dem Zustand wieder auf, in dem ID3DXLine::Begin aufgerufen wurde.
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: ID3DXLine::End-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 371463bfc24cbdba63ac51c9b729c267b9d020dd260d6d1b6c6a378bb38c3524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987230"
---
# <a name="id3dxlineend-method"></a>ID3DXLine::End-Methode

Stellt den Gerätestatus wieder in dem Zustand wieder auf, in dem [**ID3DXLine::Begin**](id3dxline--begin.md) aufgerufen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT End();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

**ID3DXLine::End** kann nicht als Ersatz für [**IDirect3DDevice9::EndScene**](/windows/desktop/api) oder [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md)verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine::Begin**](id3dxline--begin.md)
</dt> </dl>

 

 




