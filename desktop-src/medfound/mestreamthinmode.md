---
description: Wird von einem Medienstream ausgelöst, wenn der Stream gestartet oder beendet wird. Weitere Informationen zur Daten Verdünnung finden Sie unter Informationen zur Raten Kontrolle.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: Mestreamthinmode-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e19d25e5ab0430d96a9d431c941288e260092b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350554"
---
# <a name="mestreamthinmode-event"></a>Mestreamthinmode-Ereignis

Wird von einem Medienstream ausgelöst, wenn der Stream gestartet oder beendet wird. Weitere Informationen zur Daten *Verdünnung* finden Sie unter Informationen [zur Raten Kontrolle](about-rate-control.md).

Dieses Ereignis kann als Reaktion auf die [**imfratecontrol:: setRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) -Methode oder die [**imfqualityempfehlung:: setdropmode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) -Methode gesendet werden.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>VARTYPE</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>VT_BOOL<br/></td>
<td>Gibt an, ob die Verdünnung gestartet oder beendet wurde.<br/>
<ul>
<li>VARIANT_TRUE: die nach diesem Ereignis übermittelten Beispiele sind dünn.</li>
<li>VARIANT_FALSE: die nach diesem Ereignis übermittelten Beispiele sind nicht dünn.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



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

 

 




