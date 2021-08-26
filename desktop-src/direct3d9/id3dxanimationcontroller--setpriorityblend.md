---
description: Legt die prioritätsvermischungsgewichtete Gewichtung fest, die vom Animationscontroller verwendet wird.
ms.assetid: b053024b-f219-48b3-906e-161d9cf47556
title: ID3DXAnimationController::SetPriorityBlend-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e52c08d0731bc89135df4547fcfc88e94b56b826d2ccab338576a22651376d94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069110"
---
# <a name="id3dxanimationcontrollersetpriorityblend-method"></a>ID3DXAnimationController::SetPriorityBlend-Methode

Legt die prioritätsvermischungsgewichtete Gewichtung fest, die vom Animationscontroller verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPriorityBlend(
  [in] FLOAT BlendWeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*BlendWeight* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Prioritätsmischungsgewichtung, die vom Animationscontroller verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Hinweise

Die Überblendgewichtung wird verwendet, um Titel mit hoher und niedriger Priorität miteinander zu mischen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**GetPriorityBlend**](id3dxanimationcontroller--getpriorityblend.md)
</dt> </dl>

 

 
