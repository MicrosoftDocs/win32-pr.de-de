---
title: WM_CAP_GET_VIDEOFORMAT Meldung (VFW. h)
description: Die "WM \_ Cap \_ Get Videoformat"- \_ Meldung Ruft eine Kopie des verwendeten Video Formats oder die erforderliche Größe für das Videoformat ab. Sie können diese Nachricht explizit oder mithilfe der Makros capgetvideoformat und capgetvideoformatsize senden.
ms.assetid: ac72dfdb-fe1a-4007-bdce-41e5e67d076a
keywords:
- WM_CAP_GET_VIDEOFORMAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_GET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072d71366efee550b037d4a20388817954937854
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956435"
---
# <a name="wm_cap_get_videoformat-message"></a>WM-Abdeckung \_ \_ get \_ Videoformat Message

Die " **WM \_ Cap \_ get \_ Videoformat** "-Meldung Ruft eine Kopie des verwendeten Video Formats oder die erforderliche Größe für das Videoformat ab. Sie können diese Nachricht explizit oder mithilfe der Makros [**capgetvideoformat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) und [**capgetvideoformatsize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) senden.


```C++
WM_CAP_GET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*
</dt> <dd>

Größe (in Bytes) der Struktur, auf die von **s** verwiesen wird.

</dd> <dt>

<span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psvideoformat*
</dt> <dd>

Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur. Sie können auch **null** angeben, um die erforderliche Anzahl von Bytes abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Größe (in Bytes) des Video Formats oder 0 (null) zurück, wenn das Erfassungsfenster nicht mit einem Aufzeichnungs Treiber verbunden ist. Für Videoformate, für die eine Palette erforderlich ist, wird die aktuelle Palette ebenfalls zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Da komprimierte Videoformate die Größenanforderungen variieren, müssen Anwendungen zuerst die Größe abrufen, dann Arbeitsspeicher zuweisen und schließlich die Videoformat Daten anfordern.

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

 

