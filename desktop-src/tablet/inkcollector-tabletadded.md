---
description: Tritt auf, wenn ein iinktablet zum System hinzugefügt wird.
ms.assetid: c5f90fce-faf7-411b-a4d6-deb5d0f22f4a
title: InkCollector. TabletAdded-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f18f66a45570b269d36efc012f543a8b25e23f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958758"
---
# <a name="inkcollectortabletadded-event"></a>InkCollector. TabletAdded-Ereignis

Tritt auf, wenn ein [**iinktablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) zum System hinzugefügt wird.

## <a name="syntax"></a>Syntax


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tablet* \[ in\]
</dt> <dd>

Das [**iinktablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) -Objekt, das dem System hinzugefügt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icetabletadded definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkCollector-Klasse**](inkcollector-class.md)
</dt> <dt>

[**Iinktablet-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




