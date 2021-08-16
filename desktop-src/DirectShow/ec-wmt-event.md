---
description: Wird vom WM-ASF-Readerfilter gesendet, wenn er DURCH DRM (Digital Rights Management) geschützte ASF-Dateien liest.
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: EC_WMT_EVENT (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2ae2659c26d170bef14a76c0528eb5159e92ef3598fb999215e1fbd848ea90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819923"
---
# <a name="ec_wmt_event-dshowh"></a>EC_WMT_EVENT (Dshow.h)

Wird vom [WM-ASF-Readerfilter](wm-asf-reader-filter.md) gesendet, wenn er DURCH DRM (Digital Rights Management) geschützte ASF-Dateien liest.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Einer der folgenden **WMT \_ STATUS-Werte:**



| Wert                         | Beschreibung                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| WMT \_ ERWERBEN \_ EINER LIZENZ         | Wird gesendet, wenn die DRM-Komponente den Lizenzerwerb entweder erfolgreich oder nicht erfolgreich abgeschlossen hat. |
| WMT \_ INDIVIDUALIZE            | Der Sicherheitsupgradeprozess wurde entweder erfolgreich oder nicht erfolgreich abgeschlossen.                                |
| WMT \_ BENÖTIGT \_ INDIVIDUALISIERUNG | Die Datei erfordert, dass eine Anwendung ein Sicherheitsupgrade erhält, bevor die angeforderte Aktion ausgeführt wird.          |
| WMT \_ KEINE \_ RECHTE               | Die Anwendung hat keine Rechte, die angeforderte Aktion für eine durch DRM-Version 1 geschützte Datei auszuführen.                |
| WMT \_ NO \_ RIGHTS \_ EX           | Die Anwendung hat keine Rechte, die angeforderte Aktion für eine durch DRM-Version 7 geschützte Datei auszuführen.                |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zeiger auf eine [**AM \_ WMT \_ EVENT \_ DATA-Struktur,**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) die Informationen über das Ereignis enthält, oder **NULL**. Der **pData-Member** dieser Struktur zeigt auf zusätzliche Daten, deren Typ vom Wert von **lParam1** abhängt, wie in der folgenden Tabelle dargestellt.



| lParam1                       | AM \_ WMT \_ EVENT \_ DATA.pData                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| WMT \_ ERWERBEN \_ EINER LIZENZ         | Zeiger auf eine [**WM \_ GET LICENSE \_ \_ DATA-Struktur.**](/windows/desktop/wmformat/wm-get-license-data) Diese Struktur ist im Windows Media Format SDK dokumentiert. |
| WMT \_ INDIVIDUALIZE            | Zeiger auf eine [**WM \_ INDIVIDUALIZE \_ STATUS-Struktur.**](/windows/desktop/wmformat/wm-individualize-status)                                                        |
| WMT \_ BENÖTIGT \_ INDIVIDUALISIERUNG | **NULL**.                                                                                                                                        |
| WMT \_ KEINE \_ RECHTE               | Zeiger auf eine Breitzeichenzeichenfolge, die eine Abfrage-URL enthält.                                                                                   |
| WMT \_ NO \_ RIGHTS \_ EX           | Zeiger auf eine [**WM \_ GET LICENSE \_ \_ DATA-Struktur.**](/windows/desktop/wmformat/wm-get-license-data)                                                               |



 

Der Wert von *lParam2* kann **NULL** sein. Überprüfen Sie den Wert, bevor Sie den Zeiger dereferenzieren.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Weitere Informationen zum Aktivieren der Wiedergabe von DURCH DRM geschützten Dateien finden Sie in der Dokumentation Windows Media Format SDK.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

