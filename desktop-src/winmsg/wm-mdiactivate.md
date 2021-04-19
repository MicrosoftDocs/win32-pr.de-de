---
description: Eine Anwendung sendet die WM- \_ mdiaktivierungs-Meldung an ein MDI-Client Fenster (Multiple Document Interface), um das Client Fenster anzuweisen, ein anderes untergeordnetes MDI-Fenster zu aktivieren.
ms.assetid: c5de18b5-fac3-4e55-9eca-3b6672df0e7b
title: WM_MDIACTIVATE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b240c41d3b7127a5d69b855f3a5587e194b02d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367953"
---
# <a name="wm_mdiactivate-message"></a>WM- \_ mdiaktivierungs Meldung

Eine Anwendung sendet die **WM- \_ mdiaktivierungs** -Meldung an ein MDI-Client Fenster (Multiple Document Interface), um das Client Fenster anzuweisen, ein anderes untergeordnetes MDI-Fenster zu aktivieren.


```C++
#define WM_MDIACTIVATE                  0x0222
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das untergeordnete MDI-Fenster, das aktiviert werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht an ein MDI-Client Fenster sendet, ist der Rückgabewert 0 (null).

Ein untergeordnetes MDI-Fenster sollte NULL zurückgeben, wenn es diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Wenn das Client Fenster diese Nachricht verarbeitet, sendet es die **WM- \_ mdiaktivierung** an das untergeordnete Fenster, das deaktiviert wird, und an das untergeordnete Fenster, das aktiviert wird. Die von einem untergeordneten MDI-Fenster empfangenen Nachrichten Parameter lauten wie folgt:

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Ein Handle für das untergeordnete MDI-Fenster, das deaktiviert wird.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Ein Handle für das untergeordnete MDI-Fenster, das aktiviert wird.

</dd> </dl>

Ein untergeordnetes MDI-Fenster wird unabhängig vom MDI-Rahmen Fenster aktiviert. Wenn das Rahmen Fenster aktiv wird, empfängt das untergeordnete Fenster, das zuletzt mithilfe der " **WM \_ mdiaktivierungs** "-Meldung aktiviert wurde, die [**WM- \_ ncaktivierungs**](wm-ncactivate.md) Nachricht, um einen aktiven Fensterrahmen und eine Titelleiste zu zeichnen. das untergeordnete Fenster empfängt keine weitere **WM- \_ mdiaktivierungs** -Nachricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**WM- \_ mdigetactive**](wm-mdigetactive.md)
</dt> <dt>

[**WM- \_ mdinext**](wm-mdinext.md)
</dt> <dt>

[**WM- \_ ncaktivierung**](wm-ncactivate.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Mehrere Dokument Schnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 




