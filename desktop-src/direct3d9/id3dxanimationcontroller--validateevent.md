---
description: Überprüft, ob ein angegebenes Ereignishand handle gültig ist und das Animationsereignis noch nicht abgeschlossen wurde.
ms.assetid: 242ad1e2-4b04-4ce1-9cdf-f66da9f83f06
title: ID3DXAnimationController::ValidateEvent-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ValidateEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 24c5195d38aeaebefd1713df31f23b6b2ec7b2324a31381027f3442b541678c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094177"
---
# <a name="id3dxanimationcontrollervalidateevent-method"></a>ID3DXAnimationController::ValidateEvent-Methode

Überprüft, ob ein angegebenes Ereignishand handle gültig ist und das Animationsereignis noch nicht abgeschlossen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT ValidateEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hEvent* \[ In\]
</dt> <dd>

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignishand handle für ein Animationsereignis.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt S \_ OK zurück, wenn das Ereignishand handle gültig ist und das Ereignis noch nicht abgeschlossen wurde.

Gibt E \_ FAIL zurück, wenn das Ereignishandy ungültig ist und/oder das Ereignis abgeschlossen wurde.

## <a name="remarks"></a>Hinweise

Die -Methode gibt an, dass ein Ereignishand handle gültig ist, auch wenn das Ereignis ausgeführt wird, aber noch nicht abgeschlossen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




