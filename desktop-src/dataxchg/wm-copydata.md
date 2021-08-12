---
title: WM_COPYDATA (Winuser.h)
description: Eine Anwendung sendet die WM \_ COPYDATA-Nachricht, um Daten an eine andere Anwendung zu übergeben.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- WM_COPYDATA der Exchange
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
ms.openlocfilehash: 4eb91b2544bf0ebf0e8767a611b422de9aaaf1d73161e47c7bf27768f4acecb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304485"
---
# <a name="wm_copydata-message"></a>WM \_ COPYDATA-Nachricht

Eine Anwendung sendet die **WM \_ COPYDATA-Nachricht,** um Daten an eine andere Anwendung zu übergeben.


```C++
#define WM_COPYDATA                     0x004A
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster, das die Daten über gibt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**COPYDATASTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-copydatastruct) die die zu übergebenden Daten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die empfangende Anwendung diese Nachricht verarbeitet, sollte sie **TRUE zurückgeben.** Andernfalls sollte FALSE **zurückgegeben werden.**

## <a name="remarks"></a>Hinweise

Die übergebenen Daten dürfen keine Zeiger oder andere Verweise auf Objekte enthalten, auf die die Anwendung, die die Daten empfängt, nicht zugriffen kann.

Während diese Nachricht gesendet wird, dürfen die Daten, auf die verwiesen wird, nicht von einem anderen Thread des sendenden Prozesses geändert werden.

Die empfangende Anwendung sollte die Daten als schreibgeschützt betrachten. Der *lParam-Parameter* ist nur während der Verarbeitung der Nachricht gültig. Die empfangende Anwendung sollte den Arbeitsspeicher, auf den von *lParam verwiesen wird, nicht frei geben.* Wenn die empfangende Anwendung nach der Rückgabe von [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) auf die Daten zugreifen muss, muss sie die Daten in einen lokalen Puffer kopieren.

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [Verwenden von Datenkopierdaten.](using-data-copy.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 

