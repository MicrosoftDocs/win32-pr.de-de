---
description: Tritt auf, wenn ein iinktablet aus dem System entfernt wird.
ms.assetid: 2217a69e-5b39-4827-82cd-99a02e9d39c6
title: InkOverlay. tabletreverschodas Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a7d0e69bae7cb6360794b9624fcef7c8be639e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106367995"
---
# <a name="inkoverlaytabletremoved-event"></a>InkOverlay. tabletreverschodas Ereignis

Tritt auf, wenn ein [**iinktablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) aus dem System entfernt wird.

## <a name="syntax"></a>Syntax


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tabletid* \[ in\]
</dt> <dd>

Der Long-Wert, der als ID für das [**iinktablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) -Objekt verwendet wurde, das entfernt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icetabletreverschot definiert.

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

[**Iinktablet-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




