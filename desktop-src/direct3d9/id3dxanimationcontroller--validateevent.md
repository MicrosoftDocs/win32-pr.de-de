---
description: Überprüft, ob ein angegebenes Ereignis Handle gültig ist und das Animations Ereignis noch nicht abgeschlossen wurde.
ms.assetid: 242ad1e2-4b04-4ce1-9cdf-f66da9f83f06
title: 'ID3DXAnimationController:: ValidateEvent-Methode (D3dx9anim. h)'
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
ms.openlocfilehash: e1a632fa867269f04e8f5f66e6bc352ef1701cd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354411"
---
# <a name="id3dxanimationcontrollervalidateevent-method"></a>ID3DXAnimationController:: ValidateEvent-Methode

Überprüft, ob ein angegebenes Ereignis Handle gültig ist und das Animations Ereignis noch nicht abgeschlossen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT ValidateEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hevent* \[ in\]
</dt> <dd>

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignis Handle für ein Animations Ereignis.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt S \_ OK zurück, wenn das Ereignis Handle gültig ist und das Ereignis noch nicht abgeschlossen wurde.

Gibt "E Fail" zurück, \_ Wenn das Ereignis Handle ungültig ist und/oder das Ereignis abgeschlossen wurde.

## <a name="remarks"></a>Bemerkungen

Die-Methode gibt an, dass ein Ereignis Handle gültig ist, auch wenn das Ereignis ausgeführt wird, aber noch nicht abgeschlossen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




