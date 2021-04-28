---
description: 'InkOverlay.TabletAdded-Ereignis: Tritt auf, wenn dem System eine IInkTablet hinzugefügt wird.'
ms.assetid: 2076a520-bd37-43b5-b57f-030828b096cb
title: InkOverlay.TabletAdded-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c22630430622c98026c81adb1c6a131a53277a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116788"
---
# <a name="inkoverlaytabletadded-event"></a>InkOverlay.TabletAdded-Ereignis

Tritt ein, wenn dem System eine [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) hinzugefügt wird.

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

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICETabletAdded definiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**IInkTablet-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




