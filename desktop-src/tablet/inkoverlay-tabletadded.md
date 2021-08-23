---
description: 'InkOverlay.TabletAdded-Ereignis: Tritt auf, wenn dem System eine IInkTablet hinzugefügt wird.'
ms.assetid: 2076a520-bd37-43b5-b57f-030828b096cb
title: InkOverlay.TabletAdded-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23086ed2b2238a142a1b7f3116eb2cb86ba14ad90f758a9c15052f5b520be347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967089"
---
# <a name="inkoverlaytabletadded-event"></a>InkOverlay.TabletAdded-Ereignis

Tritt ein, wenn [**dem System eine IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) hinzugefügt wird.

## <a name="syntax"></a>Syntax


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tablet* \[ In\]
</dt> <dd>

Das [**IInkTablet-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) das dem System hinzugefügt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICETabletAdded definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**IInkTablet-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




