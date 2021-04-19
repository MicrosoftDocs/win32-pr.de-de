---
description: Bei einer Frame Hierarchie registriert alle benannten Matrizen im Animations Mixer.
ms.assetid: df0560c2-4417-4d54-94c8-031521b32189
title: D3DXFrameRegisterNamedMatrices-Funktion (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameRegisterNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8496f467e668939c5d5aa0e90266ab012d436038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366464"
---
# <a name="d3dxframeregisternamedmatrices-function"></a>D3DXFrameRegisterNamedMatrices-Funktion

Bei einer Frame Hierarchie registriert alle benannten Matrizen im Animations Mixer.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXFrameRegisterNamedMatrices(
  _In_ LPD3DXFRAME               pFrameRoot,
  _In_ LPD3DXANIMATIONCONTROLLER pAnimController
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pframeroot* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXFRAME**](d3dxframe.md)**

Der Knoten der obersten Ebene in der Frame Hierarchie.

</dd> <dt>

*panimcontroller* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**

Zeiger auf das Animations Controller Objekt.

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

 

 




