---
description: Bereitet ein Gerät für Zeichnungs Zeilen vor.
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: 'ID3DXLine:: Begin-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ee241b39f2d0c1939cf2cb0cc09e079abd3430a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365340"
---
# <a name="id3dxlinebegin-method"></a>ID3DXLine:: Begin-Methode

Bereitet ein Gerät für Zeichnungs Zeilen vor.

## <a name="syntax"></a>Syntax


```C++
HRESULT Begin();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

Das Aufrufen von **ID3DXLine:: begin** ist optional. Wenn Sie außerhalb einer ID3DXLine:: begin/ID3DXLine:: End-Sequenz aufgerufen wird, werden die Draw-Funktionen intern ID3DXLine:: BEGIN und ID3DXLine:: End aufrufen. Um zusätzlichen Aufwand zu vermeiden, sollte diese Methode verwendet werden, wenn mehr als eine Draw-Funktion nacheinander aufgerufen wird.

Diese Methode muss innerhalb einer [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) -und [**IDirect3DDevice9:: EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) -Sequenz aufgerufen werden.

ID3DXLine:: begin kann nicht als Ersatz für [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) oder [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md)verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
