---
description: Gibt ein Ereignis Handle an das nächste in der nächsten Priorität angegebene Blend-Ereignis zurück, das nach einem angegebenen Ereignis geplant ist.
ms.assetid: 64fa6fca-dc4a-4534-ab8e-b11b3c7ed23c
title: 'ID3DXAnimationController:: getupcomingpriorityblend-Methode (D3dx9anim. h)'
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
ms.openlocfilehash: 72f9b8854041094d43d9e8250ab61b5f59a67848
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394054"
---
# <a name="id3dxanimationcontrollergetupcomingpriorityblend-method"></a>ID3DXAnimationController:: getupcomingpriorityblend-Methode

Gibt ein Ereignis Handle an das nächste in der nächsten Priorität angegebene Blend-Ereignis zurück, das nach einem angegebenen Ereignis geplant ist.

## <a name="syntax"></a>Syntax


```C++
D3DXEVENTHANDLE GetUpcomingPriorityBlend(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hevent* \[ in\]
</dt> <dd>

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignis Handle für ein angegebenes Ereignis, nach dem nach einem folgenden Ereignis für die Prioritäts Mischung gesucht werden soll. Wenn der Wert auf **null** festgelegt ist, gibt die Methode das nächste Ereignis für die nächste geplante Priorität zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignis Handle zum nächsten geplanten Prioritäts-Blend-Ereignis. **Null** wird zurückgegeben, wenn kein neues Prioritäts-Blend-Ereignis geplant ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann iterativ verwendet werden, um ein gewünschtes Prioritäts-Blend-Ereignis durch wiederholtes übergeben von **null** für hevent zu suchen.

> [!Note]  
> Iterieren Sie nicht weiter, nachdem die Methode **null** zurückgegeben hat.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




