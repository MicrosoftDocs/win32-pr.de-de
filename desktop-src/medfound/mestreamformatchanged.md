---
description: Wird von einem Mediendaten Strom ausgelöst, wenn sich der Medientyp des Streams ändert.
ms.assetid: 14786a9b-413e-4fb4-b267-bfd0ccd4631b
title: Mestreamformatchanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd48e7abc8121707b150af5bc8968a50c1eb44e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863603"
---
# <a name="mestreamformatchanged-event"></a>Mestreamformatchanged-Ereignis

Wird von einem Mediendaten Strom ausgelöst, wenn sich der Medientyp des Streams ändert.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE                | BESCHREIBUNG                                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| VT \_ unbekannt<br/> | Ein Zeiger auf die [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle des neuen Medientyps.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Ereignis, um Formatänderungen im Stream zu signalisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




