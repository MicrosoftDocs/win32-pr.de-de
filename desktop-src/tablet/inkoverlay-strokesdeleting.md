---
description: Tritt auf, bevor Striche aus der Ink-Eigenschaft gelöscht werden.
ms.assetid: 09468416-ad08-48ea-aa4a-3af0fe553f3d
title: InkOverlay. strokeslösch-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64422e61869c633514c3e219e3d090476a693dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960501"
---
# <a name="inkoverlaystrokesdeleting-event"></a>InkOverlay. strokeslösch-Ereignis

Tritt auf, bevor Striche aus der [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) -Eigenschaft gelöscht werden.

## <a name="syntax"></a>Syntax


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Striche* \[ in\]
</dt> <dd>

Die [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, die beim Auslösen des **strokeslösch** -Ereignisses gelöscht wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID "DISPID \_ ioestrokeslösch" definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**Ink \[ -Eigenschaft InkCollector/InkOverlay-Klasse\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)
</dt> </dl>

 

