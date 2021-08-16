---
title: WM_GETDPISCALEDSIZE Meldung (Winuser.h)
description: Diese Meldung teilt dem Betriebssystem mit, dass das Fenster auf andere Dimensionen als die Standardgröße angepasst wird.
ms.assetid: 038CAA21-0944-45D3-8C40-A6498F36D9E4
keywords:
- WM_GETDPISCALEDSIZE Meldung Hoher DPI-Anteil
topic_type:
- apiref
api_name:
- WM_GETDPISCALEDSIZE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3386a0f38187e375f9dae0e390a413a1e64565f15d39e1e9f1e436c9238bea99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759291"
---
# <a name="wm_getdpiscaledsize-message"></a>WM \_ GETDPISCALEDSIZE-Nachricht

Diese Meldung teilt dem Betriebssystem mit, dass das Fenster auf andere Dimensionen als die Standardgröße angepasst wird.

Diese Meldung wird mit dem [DPI \_ AWARENESS \_ CONTEXT](dpi-awareness-context.md) von Pro Monitor v2 an Fenster der obersten Ebene gesendet, bevor eine [**\_ WM-DPICHANGED-Nachricht**](wm-dpichanged.md) gesendet wird, und ermöglicht es dem Fenster, die gewünschte Größe für die ausstehende DPI-Änderung zu berechnen. Da die lineare DPI-Skalierung das Standardverhalten ist, ist dies nur in Szenarien nützlich, in denen das Fenster nicht linear skaliert werden soll. Wenn die Anwendung auf diese Nachricht antwortet, ist die resultierende Größe das Kandidatenrechteck, das an **WM \_ DPICHANGED** gesendet wird.

Verwenden Sie diese Meldung, um die Größe des mit [**WM \_ DPICHANGED**](wm-dpichanged.md)bereitgestellten Rect zu ändern.


```C++
#define WM_GETDPISCALEDSIZE       0x02E4
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

WPARAM enthält einen DPI-Wert. Die größe des skalierten Fensters, die die Anwendung festlegen würde, muss so berechnet werden, als ob das Fenster zu diesem DPI wechseln würde.

</dd> <dt>

*lParam* 
</dt> <dd>

LPARAM ist ein In/Out-Zeiger auf eine SIZE-Struktur. Der \_ \_ Wert In in der LPARAM ist die ausstehende Größe des Fensters nach einer vom Benutzer initiierten Verschiebung oder einem Aufruf von [**SetWindowPos.**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) Wenn die Größe des Fensters geändert wird, entspricht diese Größe nicht unbedingt der aktuellen Größe des Fensters zum Zeitpunkt des Empfangs dieser Nachricht.

Der \_ \_ Out-Wert in der LPARAM sollte von der Anwendung in geschrieben werden, um die gewünschte skalierte Fenstergröße anzugeben, die dem bereitgestellten DPI-Wert im WPARAM entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt eine BOOL zurück. Wenn TRUE zurückgegeben wird, wird angegeben, dass eine neue Größe berechnet wurde. Die Rückgabe von FALSE gibt an, dass die Nachricht nicht behandelt wird, und die standardmäßige lineare DPI-Skalierung gilt für das Fenster.

## <a name="remarks"></a>Hinweise

Diese Meldung wird nur an Fenster der obersten Ebene gesendet, die über den DPI-Kontext "Pro Monitor v2" verfügen.

Dieses Ereignis ist erforderlich, um eine ordnungsgemäß nicht lineare Skalierung zu ermöglichen, und stellt sicher, dass die Position des Fensters in Bezug auf den Cursor und beim Wechseln zwischen Monitoren konstant bleibt.

Es gibt keine bestimmte Standardbehandlung dieser Nachricht in [DefWindowProc.](/windows/win32/api/winuser/nf-winuser-defwindowproca) Wie bei allen Nachrichten, die nicht explizit verarbeitet werden, gibt [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) für diese Nachricht 0 (null) zurück. Wie bereits erwähnt, weist diese Rückgabe das System an, das lineare Standardverhalten zu verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1703 \[\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



 

