---
title: WM_COPYDATA Meldung (Winuser. h)
description: Eine Anwendung sendet die Nachricht "WM \_ CopyData", um Daten an eine andere Anwendung zu übergeben.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- WM_COPYDATA Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_COPYDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8160c88b11fa109e8bbfaa06f0f6c45c9b7daed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477178"
---
# <a name="wm_copydata-message"></a>Meldung zum WM- \_ CopyData

Eine Anwendung sendet die Nachricht " **WM \_ CopyData** ", um Daten an eine andere Anwendung zu übergeben.


```C++
#define WM_COPYDATA                     0x004A
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster, in dem die Daten übergeben werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**copydatastruct**](/windows/win32/api/winuser/ns-winuser-copydatastruct) -Struktur, die die zu über gebenden Daten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die empfangende Anwendung diese Nachricht verarbeitet, sollte Sie " **true**" zurückgeben. Andernfalls sollte **false** zurückgegeben werden.

## <a name="remarks"></a>Bemerkungen

Die zu über gebenden Daten dürfen keine Zeiger oder andere Verweise auf Objekte enthalten, auf die die Anwendung, die die Daten empfängt, nicht zugreifen kann.

Während diese Nachricht gesendet wird, dürfen die referenzierten Daten nicht von einem anderen Thread des Sendevorgangs geändert werden.

Die empfangende Anwendung sollte die schreibgeschützten Daten berücksichtigen. Der *LPARAM* -Parameter ist nur während der Verarbeitung der Nachricht gültig. Die empfangende Anwendung sollte den von *LPARAM* referenzierten Speicher nicht freigeben. Wenn die empfangende Anwendung auf die Daten zugreifen muss, nachdem [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) zurückgegeben wurde, müssen die Daten in einen lokalen Puffer kopiert werden.

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [Verwenden von Datenkopien](using-data-copy.md).

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

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**Copydatastruct**](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 

