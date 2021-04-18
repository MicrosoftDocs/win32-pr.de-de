---
description: Wird von einem Bytestream gesendet, wenn sich die Merkmale des Bytestreams geändert haben.
ms.assetid: EC34A7A3-BF01-4F9E-BA79-131B76D4C58F
title: Mebytestreamcharakteristicschangi-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e626f510927970aad3c51182fca3a6dfddb0009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347257"
---
# <a name="mebytestreamcharacteristicschanged-event"></a>Mebytestreamcharakteristicschangi-Ereignis

Wird von einem Bytestream gesendet, wenn sich die Merkmale des Bytestreams geändert haben.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE               | BESCHREIBUNG                           |
|-----------------------|---------------------------------------|
| VT \_ leer <br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Ereignis zeigt an, dass sich mindestens eine der folgenden Eigenschaften geändert hat:

-   Funktionsflags ([**IMF Bytestream:: getcapability**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))
-   Flag für das Ende des Streams ([**IMF Bytestream:: isendobstream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))
-   Length ([**IMF Bytestream:: GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))

Dieses Ereignis wird nicht von allen [**IMF Bytestream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) -Implementierungen unterstützt. Um das Ereignis zu empfangen, Fragen Sie das Byte-Stream-Objekt für die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




