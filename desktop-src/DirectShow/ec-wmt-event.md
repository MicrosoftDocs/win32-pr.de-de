---
description: Wird vom WM-ASF-Reader-Filter gesendet, wenn die von Digital Rights Management (DRM) geschützten ASF-Dateien gelesen werden.
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: EC_WMT_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ce974cd83a404242fb51486f0889ac9b79e044
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358265"
---
# <a name="ec_wmt_event-dshowh"></a>EC_WMT_EVENT (DShow. h)

Wird vom [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter gesendet, wenn die von Digital Rights Management (DRM) geschützten ASF-Dateien gelesen werden.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Einer der folgenden **WMT- \_ Status** Werte:



| Wert                         | BESCHREIBUNG                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| WMT-Abruf \_ \_ Lizenz         | Wird gesendet, wenn der Lizenz Erwerbsprozess von der DRM-Komponente erfolgreich oder erfolglos abgeschlossen wurde. |
| WMT \_ Individual            | Der Sicherheits Upgradevorgang wurde entweder erfolgreich oder erfolglos abgeschlossen.                                |
| WMT \_ erfordert \_ Individualisierung | Die Datei erfordert, dass eine Anwendung vor dem Ausführen der angeforderten Aktion ein Sicherheits Upgrade erhält.          |
| WMT \_ keine \_ Rechte               | Die Anwendung verfügt nicht über die Berechtigung, die angeforderte Aktion für eine Datei auszuführen, die von DRM-Version 1 geschützt wird.                |
| WMT \_ keine \_ Rechte \_ Ex           | Die Anwendung verfügt nicht über die Berechtigung, die angeforderte Aktion für eine Datei auszuführen, die von DRM-Version 7 geschützt wird.                |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zeiger auf eine [**am \_ WMT- \_ Ereignis \_ Daten**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) Struktur, die Informationen über das Ereignis enthält, oder **null**. Der **pData** -Member dieser Struktur verweist auf zusätzliche Daten, deren Typ von dem Wert von **lParam1** abhängt, wie in der folgenden Tabelle dargestellt.



| lParam1                       | AM \_ WMT- \_ Ereignis \_ Daten. pdata                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| WMT-Abruf \_ \_ Lizenz         | Zeiger auf eine [**WM- \_ get- \_ Lizenz \_ Daten**](/windows/desktop/wmformat/wm-get-license-data) Struktur. Diese Struktur ist im Windows Media-Format-SDK dokumentiert. |
| WMT \_ Individual            | Zeiger auf eine [**WM- \_ Individualisierungs \_ Status**](/windows/desktop/wmformat/wm-individualize-status) -Struktur.                                                        |
| WMT \_ erfordert \_ Individualisierung | **Null**.                                                                                                                                        |
| WMT \_ keine \_ Rechte               | Zeiger auf eine breit Zeichen-Zeichenfolge, die eine Challenge-URL enthält.                                                                                   |
| WMT \_ keine \_ Rechte \_ Ex           | Zeiger auf eine [**WM- \_ get- \_ Lizenz \_ Daten**](/windows/desktop/wmformat/wm-get-license-data) Struktur.                                                               |



 

Der Wert von *lParam2* kann **null** sein. Überprüfen Sie den Wert, bevor Sie den Zeiger dereferenzieren.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zum Aktivieren der Wiedergabe von DRM-geschützten Dateien finden Sie in der Dokumentation zum Windows Media-Format SDK.

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

 

