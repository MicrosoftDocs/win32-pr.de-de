---
description: Gibt ein Ereignishandle für das nächste Ereignis zurück, das nach einem angegebenen Ereignis auf einer Animationsspur auftreten soll.
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: ID3DXAnimationController::GetUpcomingTrackEvent-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6e2730a9649400af8cc0229cb69ab695044681fde43a29a1a784d212f8d2641
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279030"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a>ID3DXAnimationController::GetUpcomingTrackEvent-Methode

Gibt ein Ereignishandle für das nächste Ereignis zurück, das nach einem angegebenen Ereignis auf einer Animationsspur auftreten soll.

## <a name="syntax"></a>Syntax


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Nachverfolgen* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Nachverfolgungsbezeichner.

</dd> <dt>

*hEvent* \[ In\]
</dt> <dd>

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignishandle für ein angegebenes Ereignis, nach dem nach einem folgenden Ereignis gesucht werden soll. Wenn **null** festgelegt ist, gibt die Methode das nächste geplante Ereignis zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignishandle für das nächste Ereignis, das für die Ausführung auf der angegebenen Spur geplant ist. **NULL** wird zurückgegeben, wenn kein neues Ereignis geplant ist.

## <a name="remarks"></a>Hinweise

Diese Methode kann iterativ verwendet werden, um ein gewünschtes Ereignis zu finden, indem wiederholt **NULL** für hEvent übergeben wird.

> [!Note]  
> Kehren Sie nicht weiter nach, nachdem die Methode **NULL** zurückgegeben hat.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
