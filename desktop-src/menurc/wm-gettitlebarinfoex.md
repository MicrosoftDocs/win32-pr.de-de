---
title: WM_GETTITLEBARINFOEX Meldung (Winuser. h)
description: Wird gesendet, um erweiterte Titelleisten Informationen anzufordern. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 0760dbf1-5b20-471c-bfd9-b8d28b52074b
keywords:
- WM_GETTITLEBARINFOEX von Meldungs Menüs und anderen Ressourcen
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
ms.openlocfilehash: fea31326faf5953df0facf34b58b06d7766c2e7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391652"
---
# <a name="wm_gettitlebarinfoex-message"></a>WM \_ gettitlebarinfoex-Meldung

Wird gesendet, um erweiterte Titelleisten Informationen anzufordern. Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


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

Ein Zeiger auf eine [**titlebarinfoex**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) -Struktur. Der Absender der Nachricht ist für die Zuweisung von Speicher für diese Struktur verantwortlich. Legen Sie den **CBSIZE** -Member dieser-Struktur auf fest, `sizeof(TITLEBARINFOEX)` bevor Sie diese-Struktur mit der Nachricht übergeben.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das folgende Beispiel zeigt, wie der Nachrichtenempfänger einen **LPARAM** -Wert umwandelt, um die [**titlebarinfoex**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) -Struktur abzurufen.

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über Menüs](menus.md)
</dt> </dl>

 

