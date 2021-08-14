---
description: 'InkOverlay.DoubleClick-Ereignis: Tritt auf, wenn auf das InkCollector- oder InkOverlay-Objekt doppelklickt.'
ms.assetid: 76ea40d4-82cf-420a-a9eb-66cb0492b43b
title: InkOverlay.DoubleClick-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf670c191f06e53effa0a59a078a70d7c9d096d72d2ed49a387ffa933eb7bae1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219375"
---
# <a name="inkoverlaydoubleclick-event"></a>InkOverlay.DoubleClick-Ereignis

Tritt ein, wenn auf [**das InkCollector-**](inkcollector-class.md) oder [**InkOverlay-Objekt**](inkoverlay-class.md) doppelklickt.

## <a name="syntax"></a>Syntax


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

Gibt an, ob das Ereignis für das übergeordnete Steuerelement abgebrochen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IPEDblClick definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> </dl>

 

 




