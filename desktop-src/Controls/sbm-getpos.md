---
title: SBM_GETPOS Meldung (Winuser.h)
description: Die SBM \_ GETPOS-Nachricht wird gesendet, um die aktuelle Position des Bildlauffelds eines Bildlaufleisten-Steuerelements abzurufen.
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- SBM_GETPOS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- SBM_GETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0105b2c015614c9f064b2c97f60100c2240bd6588612d34b25546c7ced832bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408893"
---
# <a name="sbm_getpos-message"></a>SBM \_ GETPOS-Nachricht

Die **SBM \_ GETPOS-Nachricht** wird gesendet, um die aktuelle Position des Bildlauffelds eines Bildlaufleisten-Steuerelements abzurufen. Die aktuelle Position ist ein relativer Wert, der vom aktuellen Bildlaufbereich abhängt. Wenn der Bildlaufbereich beispielsweise 0 bis 100 beträgt und sich das Bildlauffeld in der Mitte der Leiste befindet, ist die aktuelle Position 50.

Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten sie die [**GetScrollPos-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) verwenden. Ein Fenster empfängt diese Meldung über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Anwendungen, die ein benutzerdefiniertes Scrollleisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **GetScrollPos-Funktion** ordnungsgemäß funktioniert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die aktuelle Position des Bildlauffelds in der Scrollleiste.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**SBM \_ GETRANGE**](sbm-getrange.md)
</dt> <dt>

[**SBM \_ SETPOS**](sbm-setpos.md)
</dt> <dt>

[**SBM \_ SETRANGE**](sbm-setrange.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

