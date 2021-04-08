---
title: WM_CAP_GET_STATUS Meldung (VFW. h)
description: Mit der \_ Statusmeldung "WM-Cap- \_ Status abrufen" wird \_ der Status des Aufzeichnungs Fensters abgerufen. Sie können diese Nachricht explizit oder mithilfe des capgetstatus-Makros senden.
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- WM_CAP_GET_STATUS-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_GET_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ef6590770e8a9ece3eb8abaffb4dbca0b1a4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040070"
---
# <a name="wm_cap_get_status-message"></a>\_ \_ \_ Status Meldung zur WM-Abdeckung

Mit der Statusmeldung " **WM-Cap- \_ \_ \_ Status** abrufen" wird der Status des Aufzeichnungs Fensters abgerufen. Sie können diese Nachricht explizit oder mithilfe des [**capgetstatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) -Makros senden.


```C++
WM_CAP_GET_STATUS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPSTATUS) (s); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*
</dt> <dd>

Größe (in Bytes) der Struktur, auf die von **s** verwiesen wird.

</dd> <dt>

<span id="s"></span><span id="S"></span>*Hymnen*
</dt> <dd>

Zeiger auf eine [**capstatus**](/windows/win32/api/vfw/ns-vfw-capstatus) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich oder **false** , wenn das Aufzeichnungs Fenster nicht mit einem Aufzeichnungs Treiber verbunden ist.

## <a name="remarks"></a>Bemerkungen

Die [**capstatus**](/windows/win32/api/vfw/ns-vfw-capstatus) -Struktur enthält den aktuellen Status des Aufzeichnungs Fensters. Da dieser Zustand dynamisch ist und sich als Reaktion auf verschiedene Nachrichten ändert, sollte die Anwendung diese Struktur nach dem Senden der [**WM- \_ Cap- \_ DLG \_**](wm-cap-dlg-videoformat.md) -Nachricht (oder mithilfe des [**capdlgvideoformat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) -Makros) und immer dann, wenn Sie Menü Elemente aktivieren oder den tatsächlichen Zustand des Fensters bestimmen muss, initialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> <dt>

[Video Erfassungs Meldungen](video-capture-messages.md)
</dt> </dl>

 

 





