---
title: WM_GETTITLEBARINFOEX Meldung (Winuser.h)
description: Wird gesendet, um informationen zur erweiterten Titelleiste anzufordern. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 0760dbf1-5b20-471c-bfd9-b8d28b52074b
keywords:
- WM_GETTITLEBARINFOEX Meldung Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- WM_GETTITLEBARINFOEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1acbe85afa1871caf796c70a9535f5646d2511317a0e9ee0564db55101a16449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869666"
---
# <a name="wm_gettitlebarinfoex-message"></a>WM \_ GETTITLEBARINFOEX-Nachricht

Wird gesendet, um informationen zur erweiterten Titelleiste anzufordern. Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_GETTITLEBARINFOEX            0x033F
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**TITLEBARINFOEX-Struktur.**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) Der Absender der Nachricht ist für die Zuweisung von Arbeitsspeicher für diese Struktur verantwortlich. Legen Sie den **cbSize-Member** dieser Struktur auf fest, `sizeof(TITLEBARINFOEX)` bevor Sie diese Struktur mit der Meldung übergeben.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das folgende Beispiel zeigt, wie der Nachrichtenempfänger einen **LPARAM-Wert** umformt, um die [**TITLEBARINFOEX-Struktur**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) abzurufen.

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Menüs](menus.md)
</dt> </dl>

 

