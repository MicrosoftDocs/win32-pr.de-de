---
description: Beendet eine Szene.
ms.assetid: f721593e-6cba-4569-8276-6a4ffc0fc37a
title: 'ID3DXRenderToSurface:: EndScene-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.EndScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d5aa0c1fbccb756ac612b813ad151813a782b122
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761994"
---
# <a name="id3dxrendertosurfaceendscene-method"></a>ID3DXRenderToSurface:: EndScene-Methode

Beendet eine Szene.

## <a name="syntax"></a>Syntax


```C++
HRESULT EndScene(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MipFilter* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Filteroptionen, aufgelistet in [D3DX \_ Filter](d3dx-filter.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> <dt>

[**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md)
</dt> </dl>

 

 
