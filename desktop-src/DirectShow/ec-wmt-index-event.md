---
description: Wird gesendet, wenn eine Anwendung den WM-ASF-Writer-Filter zum Indizieren Windows Media Video Dateien verwendet.
ms.assetid: e5f69aa1-f9b0-4403-acab-25d1f971a876
title: EC_WMT_INDEX_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28e10b1d0e4a559bb10fbc521e232d08e08b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356470"
---
# <a name="ec_wmt_index_event-dshowh"></a>EC_WMT_INDEX_EVENT (DShow. h)

Wird gesendet, wenn eine Anwendung den [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter zum Indizieren Windows Media Video Dateien verwendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Kann eine der folgenden **WMT- \_ Status** Meldungen sein.



| Wert                | BESCHREIBUNG              |
|----------------------|--------------------------|
| WMT \_ gestartet         | Die Indizierung wurde gestartet.      |
| WMT \_ geschlossen          | Die Indizierung wurde abgeschlossen.  |
| WMT- \_ Index \_ Fortschritt | Die Indizierung wird ausgeführt. |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Wenn *lParam1* WMT \_ Closed oder WMT \_ gestartet ist, dann ist *lParam2* gleich 0 (null). Wenn *lParam1* den WMT- \_ Index Status \_ hat, ist *lParam2* ein **DWORD** , das den aktuellen Status als Prozentsatz der gesamten Downloadgröße angibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignis Benachrichtigungs Codes](event-notification-codes.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




