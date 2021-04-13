---
title: EM_GETENDOFLINE Meldung (kommstrg. h)
description: Ruft das Zeilenendezeichen ab, das verwendet wird, wenn ein LineBreak eingefügt wird. Senden Sie diese Nachricht explizit oder mithilfe des \_ getendosline-Makros bearbeiten.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- Windows-Steuerelemente für EM_GETENDOFLINE Meldung
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
ms.openlocfilehash: 98d537d2ea4239ab3f511666aeba46be93a2b881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475573"
---
# <a name="em_getendofline-message"></a>EM \_ getendosline-Meldung

Ruft das Zeilenendezeichen für ein Bearbeitungs Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des [**\_ getendosline**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) -Makros bearbeiten.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Zeilenendezeichen zurück, das vom Bearbeitungs Steuerelement verwendet wird. Dies kann einer der folgenden Werte sein:

| Wert                                                                                                                                                   | Bedeutung                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**EC \_ EndOf line \_ CRLF**</dt> </dl> | Das Zeilenendezeichen, das für neue lineumbrüche verwendet wird, ist Wagen Rücklauf gefolgt von Zeilenvorschub (CRLF).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ EndOf line \_ CR**</dt> </dl>       | Das Zeilenendezeichen, das für neue lineumbrüche verwendet wird, ist Wagen Rücklauf (CR).<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ endosline \_ LF**</dt> </dl>       | Das Zeilenendezeichen, das für neue lineumbrüche verwendet wird, ist Zeilenvorschub (LF).<br/>                               |

## <a name="remarks"></a>Bemerkungen

Wenn das verwendete Zeilenendezeichen auf **EC \_ EndOfLine \_ detectfromcontent** mithilfe von [**Edit \_ setendofline**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline)festgelegt wird, gibt diese Meldung das erkannte Zeilenendezeichen zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809, \[ nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2019 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM- \_ Ziel*](em-setendofline.md)
</dt> </dl>
 

 





