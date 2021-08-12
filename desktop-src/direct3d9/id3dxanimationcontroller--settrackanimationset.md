---
description: Wendet den Animationssatz auf die angegebene Spur an.
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: ID3DXAnimationController::SetTrackAnimationSet-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a94fee2a0bd80f391b514895aa5b5348cbef6d8a53e31200b49a403a6712e2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296883"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a>ID3DXAnimationController::SetTrackAnimationSet-Methode

Wendet den Animationssatz auf die angegebene Spur an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Nachverfolgen* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Bezeichner der Spur, auf die der Animationssatz angewendet wird.

</dd> <dt>

*pAnimSet* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Zeiger auf die [**ID3DXAnimationSet-Animation,**](id3dxanimationset.md) die der Spur hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Methode legt den Animationssatz auf die angegebene Spur zum Mischen fest. Die Für jede Spur festgelegte Animation wird entsprechend der Gewichtung und Geschwindigkeit der Spur kombiniert, wenn [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
