---
description: 'Stellt den Zustand des Geräts in dem Zustand wieder her, in dem es sich beim Aufrufen von ID3DXLine:: begin befand'
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: 'ID3DXLine:: End-Methode (D3dx9core. h)'
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
ms.openlocfilehash: 69d8324ab54f37af3f45a5475f08894e278c32e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370467"
---
# <a name="id3dxlineend-method"></a>ID3DXLine:: End-Methode

Stellt den Zustand des Geräts in dem Zustand wieder her, in dem es sich beim Aufrufen von [**ID3DXLine:: begin**](id3dxline--begin.md) befand

## <a name="syntax"></a>Syntax


```C++
HRESULT End();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

**ID3DXLine:: End** kann nicht als Ersatz für [**IDirect3DDevice9:: EndScene**](/windows/desktop/api) oder [**ID3DXRenderToSurface:: EndScene**](id3dxrendertosurface--endscene.md)verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine:: begin**](id3dxline--begin.md)
</dt> </dl>

 

 




