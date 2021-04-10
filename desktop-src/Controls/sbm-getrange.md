---
title: SBM_GETRANGE Meldung (Winuser. h)
description: Die SBM \_ -GetRange-Nachricht wird gesendet, um die minimalen und maximalen Positionswerte für das ScrollBar-Steuerelement abzurufen.
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- Windows-Steuerelemente für SBM_GETRANGE Meldung
topic_type:
- apiref
api_name:
- SBM_GETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ca47e0474152a9771d2787c4a039fb2c868b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956880"
---
# <a name="sbm_getrange-message"></a>SBM- \_ GetRange-Nachricht

Die **SBM- \_ GetRange** -Nachricht wird gesendet, um die minimalen und maximalen Positionswerte für das ScrollBar-Steuerelement abzurufen.

Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten Sie die [**getscrollrange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) -Funktion verwenden. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **getscrollrange** -Funktion ordnungsgemäß funktioniert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die minimale Bild Lauf Position empfängt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die maximale Scrollposition empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

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

[**SBM- \_ GetPos**](sbm-getpos.md)
</dt> <dt>

[**SBM- \_ SetPos**](sbm-setpos.md)
</dt> <dt>

[**SBM-über \_ Tragung**](sbm-setrange.md)
</dt> <dt>

[**SBM- \_ abzeichnende**](sbm-setrangeredraw.md)
</dt> </dl>

 

