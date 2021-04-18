---
description: Gibt ein Ereignis Handle für das Ereignis zurück, das momentan auf dem angegebenen Animations Titel ausgeführt wird.
ms.assetid: 2e3d4b85-42f0-463f-9eca-d9b1fa8932f6
title: 'ID3DXAnimationController:: getcurrenttrackevent-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b00b90f6fbb3f4bb6170c8987f3634fec4bd0bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365327"
---
# <a name="id3dxanimationcontrollergetcurrenttrackevent-method"></a>ID3DXAnimationController:: getcurrenttrackevent-Methode

Gibt ein Ereignis Handle für das Ereignis zurück, das momentan auf dem angegebenen Animations Titel ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
D3DXEVENTHANDLE GetCurrentTrackEvent(
  [in] UINT           Track,
  [in] D3DXEVENT_TYPE EventType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Nach *verfolgen* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Bezeichner nachverfolgen.

</dd> <dt>

*EventType* \[ in\]
</dt> <dd>

Type: **[ **D3DXEVENT- \_ Typ**](./d3dxevent-type.md)**

Typ des abzufragende Ereignisses.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignis Handle für das Ereignis, das zurzeit auf der angegebenen Spur ausgeführt wird. **Null** wird zurückgegeben, wenn kein Ereignis auf der angegebenen Spur ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
