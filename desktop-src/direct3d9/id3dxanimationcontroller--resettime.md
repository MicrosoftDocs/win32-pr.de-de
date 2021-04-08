---
description: Setzt die globale Animations Zeit auf 0 (null) zurück. Alle ausstehenden Ereignisse behalten ihre ursprünglichen Zeitpläne, aber im neuen Zeitrahmen bei.
ms.assetid: 70b073ec-ef97-4af4-9f42-b6a6cc13605f
title: 'ID3DXAnimationController:: ResetTime-Methode (D3dx9anim. h)'
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
ms.openlocfilehash: 1206cc8514f3e7eb235f1072bf2a66c4b5bf1e7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762210"
---
# <a name="id3dxanimationcontrollerresettime-method"></a>ID3DXAnimationController:: ResetTime-Methode

Setzt die globale Animations Zeit auf 0 (null) zurück. Alle ausstehenden Ereignisse behalten ihre ursprünglichen Zeitpläne, aber im neuen Zeitrahmen bei.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird normalerweise verwendet, wenn der Wert der globalen Animations Zeit der maximalen Genauigkeit von Double-Speicher entspricht, oder 2 ⁶ ⁴-1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




