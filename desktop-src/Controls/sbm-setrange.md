---
title: SBM_SETRANGE Meldung (Winuser. h)
description: Die SBM \_ -SetRange-Nachricht wird gesendet, um die minimalen und maximalen Positionswerte für das ScrollBar-Steuerelement festzulegen.
ms.assetid: 9cf84354-3944-4c10-9b59-39427b840868
keywords:
- Windows-Steuerelemente für SBM_SETRANGE Meldung
topic_type:
- apiref
api_name:
- SBM_SETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7a720531ae58fdb0712b8f23fd1aef88b3e4caa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859204"
---
# <a name="sbm_setrange-message"></a>SBM- \_ Nachricht

Die **SBM- \_ SetRange** -Nachricht wird gesendet, um die minimalen und maximalen Positionswerte für das ScrollBar-Steuerelement festzulegen.

Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten Sie die [**setscrollrange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) -Funktion verwenden. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die Funktion **setscrollrange** ordnungsgemäß funktioniert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die minimale Bild Lauf Position an.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt die maximale Scrollposition an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**ComCtl32.dll Version 5,0**: Wenn sich die Position des Bild Lauf Felds geändert hat, ist der Rückgabewert die vorherige Position des Bild Lauf Felds. Andernfalls ist der Wert 0 (null).

**ComCtl32.dll Version 6,0**: die aktuelle Position des Bild Lauf Felds, unabhängig davon, ob es geändert wurde.

## <a name="remarks"></a>Bemerkungen

Die standardmäßigen und maximalen Positionswerte sind 0 (null). Der Unterschied zwischen den Werten, die von den *wParam* -und *LPARAM* -Parametern angegeben werden, darf nicht größer sein als MAXLONG.

Wenn die minimalen und maximalen Positionswerte gleich sind, wird das Bild Lauf leisten-Steuerelement ausgeblendet und deaktiviert.

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

[**SBM- \_ GetRange**](sbm-getrange.md)
</dt> <dt>

[**SBM- \_ SetPos**](sbm-setpos.md)
</dt> <dt>

[**SBM- \_ abzeichnende**](sbm-setrangeredraw.md)
</dt> </dl>

 

