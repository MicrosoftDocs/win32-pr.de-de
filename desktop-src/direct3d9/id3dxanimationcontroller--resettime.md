---
description: Setzt die globale Animationszeit auf 0 (null) zurück. Alle ausstehenden Ereignisse behalten ihre ursprünglichen Zeitpläne bei, jedoch im neuen Zeitrahmen.
ms.assetid: 70b073ec-ef97-4af4-9f42-b6a6cc13605f
title: ID3DXAnimationController::ResetTime-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ResetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3f5f4ba6f10d5119e479a56e9e207e410b2d1e817d6809e7ceac1c98c8d2ee5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893740"
---
# <a name="id3dxanimationcontrollerresettime-method"></a>ID3DXAnimationController::ResetTime-Methode

Setzt die globale Animationszeit auf 0 (null) zurück. Alle ausstehenden Ereignisse behalten ihre ursprünglichen Zeitpläne bei, jedoch im neuen Zeitrahmen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Hinweise

Diese Methode wird in der Regel verwendet, wenn sich der Globale Animationszeitwert der maximalen Genauigkeit des DOUBLE-Speichers nähert, oder 2⁶⁴ - 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




