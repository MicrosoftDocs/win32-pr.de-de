---
title: WM_CHANGECBCHAIN (Winuser.h)
description: Wird an das erste Fenster in der Zwischenablage-Viewerkette gesendet, wenn ein Fenster aus der Kette entfernt wird. Ein Fenster empfängt diese Nachricht über seine WindowProc-Funktion.
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- WM_CHANGECBCHAIN der Exchange
topic_type:
- apiref
api_name:
- WM_CHANGECBCHAIN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25dac74784a214f77f8b2912e2fd643624ae767027121e2262d81989d54d3831
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736314"
---
# <a name="wm_changecbchain-message"></a>WM \_ CHANGECBCHAIN-Nachricht

Wird an das erste Fenster in der Zwischenablage-Viewerkette gesendet, wenn ein Fenster aus der Kette entfernt wird.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster, das aus der Viewer-Kette der Zwischenablage entfernt wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das nächste Fenster in der Kette, das auf das entfernte Fenster folgt. Dieser Parameter ist **NULL,** wenn das zu entfernende Fenster das letzte Fenster in der Kette ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Jedes Zwischenablage-Viewerfenster speichert das Handle im nächsten Fenster in der Zwischenablage-Viewer-Kette. Anfangs ist dieses Handle der Rückgabewert der [**SetClipboardViewer-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)

Wenn ein Zwischenablageanzeigefenster die **WM \_ CHANGECBCHAIN-Nachricht** empfängt, sollte es die [**SendMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-sendmessage) aufrufen, um die Nachricht an das nächste Fenster in der Kette zu übergeben, es sei denn, das nächste Fenster ist das Fenster, das entfernt wird. In diesem Fall sollte der Zwischenablage-Viewer das vom *lParam-Parameter* angegebene Handle als nächstes Fenster in der Kette speichern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> </dl>

 

