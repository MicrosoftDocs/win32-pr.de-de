---
description: 'InkOverlay.TabletRemoved-Ereignis: Tritt auf, wenn eine IInkTablet aus dem System entfernt wird.'
ms.assetid: 2217a69e-5b39-4827-82cd-99a02e9d39c6
title: InkOverlay.TabletRemoved-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5572ec4c8afd664ef96534e93c402ec2141f65
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086648"
---
# <a name="inkoverlaytabletremoved-event"></a>InkOverlay.TabletRemoved-Ereignis

Tritt ein, wenn [**eine IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) aus dem System entfernt wird.

## <a name="syntax"></a>Syntax


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TabletId* \[ In\]
</dt> <dd>

Der Long-Wert, der als ID für das [**entfernte IInkTablet-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) verwendet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICETabletRemoved definiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**IInkTablet-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




