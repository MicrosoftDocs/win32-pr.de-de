---
title: SBM_GETSCROLLBARINFO Meldung (Winuser. h)
description: Wird von einer Anwendung gesendet, um Informationen über die angegebene Scrollleiste abzurufen.
ms.assetid: db6f704f-99ee-448c-ae7a-dd5a23399fb6
keywords:
- Windows-Steuerelemente für SBM_GETSCROLLBARINFO Meldung
topic_type:
- apiref
api_name:
- SBM_GETSCROLLBARINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8bdd78eb665bd069d854538bb2bdfae1a946765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741376"
---
# <a name="sbm_getscrollbarinfo-message"></a>SBM \_ getscrollbarinfo-Meldung

Wird von einer Anwendung gesendet, um Informationen über die angegebene Scrollleiste abzurufen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**scrollbarinfo**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) -Struktur, die die Informationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn erfolgreich, andernfalls

Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**GetScrollBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo)
</dt> <dt>

[**Scrollbarinfo**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo)
</dt> </dl>

 

