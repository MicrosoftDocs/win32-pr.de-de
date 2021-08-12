---
title: WM_CAP_GET_VIDEOFORMAT Meldung (Vfw.h)
description: Die \_ WM CAP \_ GET \_ VIDEOFORMAT-Nachricht ruft eine Kopie des verwendeten Videoformats oder die für das Videoformat erforderliche Größe ab. Sie können diese Nachricht explizit oder mithilfe der Makros capGetVideoFormat und capGetVideoFormatSize senden.
ms.assetid: ac72dfdb-fe1a-4007-bdce-41e5e67d076a
keywords:
- WM_CAP_GET_VIDEOFORMAT Nachricht Windows Multimedia
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
ms.openlocfilehash: afae3ea79b29cad6a758272f8f3952fdfb830a2b3d6d60f9fc5b4ca5042179fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622619"
---
# <a name="wm_cap_get_videoformat-message"></a>WM \_ CAP \_ GET \_ VIDEOFORMAT-Meldung

Die **WM CAP GET \_ \_ \_ VIDEOFORMAT-Nachricht** ruft eine Kopie des verwendeten Videoformats oder die für das Videoformat erforderliche Größe ab. Sie können diese Nachricht explizit oder mithilfe der Makros [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) und [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) senden.


```C++
WM_CAP_GET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Größe der Struktur in Bytes, auf die von **s** verwiesen wird.

</dd> <dt>

<span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*
</dt> <dd>

Zeiger auf eine [**BITMAPINFO-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) Sie können auch **NULL** angeben, um die Anzahl der erforderlichen Bytes abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Größe des Videoformats in Bytes oder 0 (null) zurück, wenn das Aufzeichnungsfenster nicht mit einem Erfassungstreiber verbunden ist. Für Videoformate, die eine Palette erfordern, wird auch die aktuelle Palette zurückgegeben.

## <a name="remarks"></a>Hinweise

Da komprimierte Videoformate in den Größenanforderungen variieren, müssen Anwendungen zuerst die Größe abrufen, dann Arbeitsspeicher zuordnen und schließlich die Videoformatdaten anfordern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[Video Capture Messages](video-capture-messages.md)
</dt> </dl>

 

