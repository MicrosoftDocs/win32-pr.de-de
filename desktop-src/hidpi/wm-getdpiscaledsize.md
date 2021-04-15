---
title: WM_GETDPISCALEDSIZE Meldung (Winuser. h)
description: Diese Meldung weist das Betriebssystem an, dass die Größe des Fensters auf andere Dimensionen als die Standardgröße festgelegt wird.
ms.assetid: 038CAA21-0944-45D3-8C40-A6498F36D9E4
keywords:
- WM_GETDPISCALEDSIZE Message High dpi
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
ms.openlocfilehash: b95631e51247d7919307f36dd0af10c72621a612
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476857"
---
# <a name="wm_getdpiscaledsize-message"></a>WM \_ getdpiscaledsize-Meldung

Diese Meldung weist das Betriebssystem an, dass die Größe des Fensters auf andere Dimensionen als die Standardgröße festgelegt wird.

Diese Nachricht wird mit einem dpi-kontextkontext von pro Monitor v2 an Fenster der obersten Ebene gesendet, bevor eine [**WM- \_ dpichanged**](wm-dpichanged.md) -Nachricht gesendet wird. Dadurch kann das Fenster die gewünschte Größe für die ausstehende dpi-Änderung berechnen. [ \_ \_](dpi-awareness-context.md) Da die lineare DPI-Skalierung das Standardverhalten ist, ist dies nur in Szenarios nützlich, in denen das Fenster nicht linear skaliert werden soll. Wenn die Anwendung auf diese Meldung antwortet, ist die resultierende Größe das Kandidaten Rechteck, das an **WM \_ dpichanged** gesendet wird.

Verwenden Sie diese Meldung, um die Größe der mit [**WM \_ dpichanged**](wm-dpichanged.md)bereitgestellten Rect zu ändern.


```C++
#define WM_GETDPISCALEDSIZE       0x02E4
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der wParam-Wert enthält einen dpi-Wert. Die skalierte Fenstergröße, die von der Anwendung festgelegt wird, muss berechnet werden, als ob das Fenster zu diesem dpi-Wert wechseln soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Der lParam ist ein in/out-Zeiger auf eine Größen Struktur. Der \_ in- \_ Wert in lParam ist die ausstehende Größe des Fensters nach einem vom Benutzer initiierten Verschiebe Vorgang oder einem Aufrufen von [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Wenn die Größe des Fensters geändert wird, ist diese Größe nicht notwendigerweise identisch mit der aktuellen Größe des Fensters, wenn diese Nachricht empfangen wird.

Der \_ out- \_ Wert in der lParam sollte von der Anwendung geschrieben werden, um die gewünschte skalierte Fenstergröße anzugeben, die dem bereitgestellten dpi-Wert in der wParam entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt einen booleschen Wert zurück. Die Rückgabe von true gibt an, dass eine neue Größe berechnet wurde. Wenn false zurückgegeben wird, wird die Nachricht nicht behandelt, und die standardmäßige lineare DPI-Skalierung wird auf das Fenster angewendet.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird nur an Fenster der obersten Ebene gesendet, die über einen dpi-Kontext von pro Monitor v2 verfügen.

Dieses Ereignis ist erforderlich, um eine ordnungsgemäße nichtlineare Skalierung zu ermöglichen, und stellt sicher, dass die Position des Windows in Beziehung zum Cursor und beim hin-und herwechseln zwischen den Monitoren konstant bleibt.

In [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)gibt es keine bestimmte Standardbehandlung für diese Nachricht. Wie bei allen Nachrichten, die nicht explizit behandelt werden, gibt [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca) für diese Nachricht 0 (null) zurück. Wie bereits erwähnt, weist diese Rückgabe das System an, das lineare Standardverhalten zu verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

