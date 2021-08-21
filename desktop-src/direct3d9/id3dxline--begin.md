---
description: Bereitet ein Gerät für das Zeichnen von Linien vor.
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: ID3DXLine::Begin-Methode (D3dx9core.h)
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
ms.openlocfilehash: 9daa65558c58849d406056ce3358c26fdf2ce1c604342f993babe6af553d130f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629650"
---
# <a name="id3dxlinebegin-method"></a>ID3DXLine::Begin-Methode

Bereitet ein Gerät für das Zeichnen von Linien vor.

## <a name="syntax"></a>Syntax


```C++
HRESULT Begin();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Der Aufruf von **ID3DXLine::Begin** ist optional. Wenn sie außerhalb einer ID3DXLine::Begin/ID3DXLine::End-Sequenz aufgerufen wird, rufen die Draw-Funktionen intern ID3DXLine::Begin und ID3DXLine::End auf. Um zusätzlichen Mehraufwand zu vermeiden, sollte diese Methode verwendet werden, wenn mehrere Draw-Funktionen nacheinander aufgerufen werden.

Diese Methode muss innerhalb einer [**IDirect3DDevice9::BeginScene-**](/windows/desktop/api) und [**IDirect3DDevice9::EndScene-Sequenz**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) aufgerufen werden.

ID3DXLine::Begin kann nicht als Ersatz für [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) oder [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md)verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
