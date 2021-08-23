---
description: Ruft die globale Animationszeit ab.
ms.assetid: a46e2a57-a76a-4d79-a3b6-30b242321ed2
title: ID3DXAnimationController::GetTime-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6241bbd8c447889a4718369feabf8f26dacc73c58b8e6826c1797d0639422fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987830"
---
# <a name="id3dxanimationcontrollergettime-method"></a>ID3DXAnimationController::GetTime-Methode

Ruft die globale Animationszeit ab.

## <a name="syntax"></a>Syntax


```C++
DOUBLE GetTime();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Gibt die globale Animationszeit zurück.

## <a name="remarks"></a>Hinweise

Animationen werden mithilfe einer lokalen Animationszeit entworfen und mit [**AdvanceTime**](id3dxanimationcontroller--advancetime.md)in die globale Zeit gemischt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
