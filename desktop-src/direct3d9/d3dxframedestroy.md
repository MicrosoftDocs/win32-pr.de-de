---
description: Zerstört die Teilstruktur von Frames unter dem Stamm, einschließlich des Stamms.
ms.assetid: 0bbb529f-01d8-430b-a72b-4af5f7a71253
title: D3DXFrameDestroy-Funktion (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameDestroy
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1c0809ff61abec6f55564ca17a116ad4c826bca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355808"
---
# <a name="d3dxframedestroy-function"></a>D3DXFrameDestroy-Funktion

Zerstört die Teilstruktur von Frames unter dem Stamm, einschließlich des Stamms.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXFrameDestroy(
  _In_ LPD3DXFRAME             pFrameRoot,
  _In_ LPD3DXALLOCATEHIERARCHY pAlloc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pframeroot* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXFRAME**](d3dxframe.md)**

Zeiger auf den Stamm Knoten.

</dd> <dt>

*palloc* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Zuordnungs Schnittstelle zum Aufheben der Zuordnung von Knoten der Frame Hierarchie.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Animations Funktionen](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




