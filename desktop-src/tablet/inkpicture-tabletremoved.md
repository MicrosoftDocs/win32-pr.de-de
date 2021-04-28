---
description: 'InkPicture.TabletRemoved-Ereignis: Tritt auf, wenn eine IInkTablet aus dem System entfernt wird.'
ms.assetid: 9a4640a7-cbd9-4304-88c6-86036423628d
title: InkPicture.TabletRemoved-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 929458c6b972143852b5921a8c8364a54a4b6f41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113648"
---
# <a name="inkpicturetabletremoved-event"></a>InkPicture.TabletRemoved-Ereignis

Tritt ein, wenn eine [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) aus dem System entfernt wird.

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

Der long-Wert, der als ID für das [**entfernte IInkTablet-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) verwendet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den Dispatch-Only-Schnittstellen **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ ICETabletRemoved definiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**IInkTablet-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




