---
description: Eine Anwendung sendet die \_ WM-MDIACTIVATE-Nachricht an ein Clientfenster mit mehreren Dokumenten (Multiple Document Interface, MDI), um das Clientfenster anzuweisen, ein anderes untergeordnetes MDI-Fenster zu aktivieren.
ms.assetid: c5de18b5-fac3-4e55-9eca-3b6672df0e7b
title: WM_MDIACTIVATE Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b71e0f3755d76ecb44d60eecbd3b92c124aa59339a6fbf59a098b1eeb274f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931270"
---
# <a name="wm_mdiactivate-message"></a>WM \_ MDIACTIVATE-Nachricht

Eine Anwendung sendet die **\_ WM-MDIACTIVATE-Nachricht** an ein Clientfenster mit mehreren Dokumenten (Multiple Document Interface, MDI), um das Clientfenster anzuweisen, ein anderes untergeordnetes MDI-Fenster zu aktivieren.


```C++
#define WM_MDIACTIVATE                  0x0222
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das zu aktivierende untergeordnete MDI-Fenster.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht an ein MDI-Clientfenster sendet, ist der Rückgabewert 0 (null).

Ein untergeordnetes MDI-Fenster sollte 0 (null) zurückgeben, wenn diese Meldung verarbeitet wird.

## <a name="remarks"></a>Hinweise

Während das Clientfenster diese Nachricht verarbeitet, sendet es **WM \_ MDIACTIVATE** an das untergeordnete Fenster, das deaktiviert wird, und an das untergeordnete Fenster, das aktiviert wird. Die von einem untergeordneten MDI-Fenster empfangenen Nachrichtenparameter sind wie folgt:

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Ein Handle für das untergeordnete MDI-Fenster, das deaktiviert wird.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Ein Handle für das untergeordnete MDI-Fenster, das aktiviert wird.

</dd> </dl>

Ein untergeordnetes MDI-Fenster wird unabhängig vom MDI-Rahmenfenster aktiviert. Wenn das Rahmenfenster aktiv wird, empfängt das untergeordnete Fenster zuletzt mithilfe der **WM \_ MDIACTIVATE-Nachricht** die [**WM \_ NCACTIVATE-Nachricht,**](wm-ncactivate.md) um einen aktiven Fensterrahmen und eine Titelleiste zu zeichnen. Das untergeordnete Fenster empfängt keine weitere **WM \_ MDIACTIVATE-Meldung.**

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

[**WM \_ MDIGETACTIVE**](wm-mdigetactive.md)
</dt> <dt>

[**WM \_ MMULTIXT**](wm-mdinext.md)
</dt> <dt>

[**WM \_ NCACTIVATE**](wm-ncactivate.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Schnittstelle für mehrere Dokumente](multiple-document-interface.md)
</dt> </dl>

 

 




