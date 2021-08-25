---
description: Gibt ein Ereignishand handle für das nächste Prioritätsmischungsereignis zurück, das nach einem angegebenen Ereignis auftreten soll.
ms.assetid: 64fa6fca-dc4a-4534-ab8e-b11b3c7ed23c
title: ID3DXAnimationController::GetUpcomingPriorityBlend-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4c58bf5e2a8736db98e0461988f984709e756d269d09c74dd673356676702ff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849080"
---
# <a name="id3dxanimationcontrollergetupcomingpriorityblend-method"></a>ID3DXAnimationController::GetUpcomingPriorityBlend-Methode

Gibt ein Ereignishand handle für das nächste Prioritätsmischungsereignis zurück, das nach einem angegebenen Ereignis auftreten soll.

## <a name="syntax"></a>Syntax


```C++
D3DXEVENTHANDLE GetUpcomingPriorityBlend(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hEvent* \[ In\]
</dt> <dd>

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignishand handle für ein angegebenes Ereignis, nach dem nach einem folgenden Prioritätsmischungsereignis gesucht werden soll. Wenn null festgelegt **ist,** gibt die Methode das nächste geplante Prioritätsmischungsereignis zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignishand handle für das nächste geplante Prioritätsmischungsereignis. **NULL** wird zurückgegeben, wenn kein neues Prioritätsmischungsereignis geplant ist.

## <a name="remarks"></a>Hinweise

Diese Methode kann iterativ verwendet werden, um ein gewünschtes Prioritätsüberblendungsereignis zu finden, indem wiederholt **NULL** für hEvent übergeben wird.

> [!Note]  
> Iterieren Sie nicht weiter, nachdem die Methode NULL zurückgegeben **hat.**

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




