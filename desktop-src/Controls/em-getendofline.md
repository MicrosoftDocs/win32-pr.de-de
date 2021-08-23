---
title: EM_GETENDOFLINE (Commctrl.h)
description: Ruft das Zeilenendezeichen ab, das beim Einfügen eines Zeilenumbruchs verwendet wird. Senden Sie diese Nachricht explizit oder mithilfe des \_ Makros GetEndOfLine bearbeiten.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETENDOFLINE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_GETENDOFLINE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 64ddb55ce592b71c7abaa8c35b1bf14a004b324586094f27a3b418a67e5b24e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019688"
---
# <a name="em_getendofline-message"></a>EM \_ GETENDOFLINE-Nachricht

Ruft das Zeilenendezeichen für ein Bearbeitungssteuerzeichen ab. Senden Sie diese Nachricht explizit oder mithilfe des [**\_ Makros GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) bearbeiten.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Zeilenendezeichen zurück, das vom Bearbeitungssteuerzeichen verwendet wird. Dies kann einer der folgenden Werte sein.

| Wert                                                                                                                                                   | Bedeutung                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**EC \_ ENDOFLINE \_ CRLF**</dt> </dl> | Das Zeilenendezeichen, das für neue Zeilenumbrüche verwendet wird, ist wagenrücklauf gefolgt von Linefeed (CRLF).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ ENDOFLINE \_ CR**</dt> </dl>       | Das Zeilenendezeichen, das für neue Zeilenumbrüche verwendet wird, ist Wagenrücklauf (CR).<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ ENDOFLINE \_ LF**</dt> </dl>       | Das Zeilenendezeichen, das für neue Zeilenumbrüche verwendet wird, ist linefeed (LF).<br/>                               |

## <a name="remarks"></a>Hinweise

Wenn das verwendete Zeilenendezeichen mit [**\_ setEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline)bearbeiten auf **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** festgelegt ist, gibt diese Meldung das erkannte Zeilenendezeichen zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10, Version 1809 Nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2019-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ SETENDOFLINE*](em-setendofline.md)
</dt> </dl>
 

 





