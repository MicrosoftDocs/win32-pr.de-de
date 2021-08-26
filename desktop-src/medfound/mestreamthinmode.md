---
description: Wird von einem Medienstream ausgelöst, wenn er den Stream startet oder beendet. Informationen zum Ausschmalen finden Sie unter Informationen zur Ratensteuerung.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: MEStreamThinMode-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 371c628498356f64918d42ffe6af94aef95af34005250ba3a4a891b6b76f6dc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013560"
---
# <a name="mestreamthinmode-event"></a>MEStreamThinMode-Ereignis

Wird von einem Medienstream ausgelöst, wenn er den Stream startet oder beendet. Informationen zur *Ausschmalung* finden Sie unter [Informationen zur Ratensteuerung.](about-rate-control.md)

Dieses Ereignis kann als Antwort auf die [**METHODE VONRATECONTROL::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) oder DIE [**METHODE DERQUALITYAdvise::SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) gesendet werden.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>VARTYPE</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>VT_BOOL<br/></td>
<td>Gibt an, ob die Schlankerlegung gestartet oder beendet wurde.<br/>
<ul>
<li>VARIANT_TRUE: Nach diesem Ereignis übermittelte Beispiele werden ausgesät.</li>
<li>VARIANT_FALSE: Stichproben, die nach diesem Ereignis übermittelt werden, werden nicht ausgesät.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




