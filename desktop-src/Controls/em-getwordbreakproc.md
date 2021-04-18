---
title: EM_GETWORDBREAKPROC Meldung (Winuser. h)
description: Ruft die Adresse der aktuellen WordWrap-Funktion ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 564b4b1b-913f-4040-bb28-eea50c0c3738
keywords:
- Windows-Steuerelemente für EM_GETWORDBREAKPROC Meldung
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb9499492668abac24774b66304ae8a87a2d739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478108"
---
# <a name="em_getwordbreakproc-message"></a>EM \_ getwordbreakproc-Meldung

Ruft die Adresse der aktuellen WordWrap-Funktion ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

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

Der Rückgabewert gibt die Adresse der Anwendungs definierten WordWrap-Funktion an. Der Rückgabewert ist **null** , wenn keine WordWrap-Funktion vorhanden ist.

## <a name="remarks"></a>Bemerkungen

Eine WordWrap-Funktion scannt einen Text Puffer, der Text enthält, der an die Anzeige gesendet werden soll, und sucht nach dem ersten Wort, das nicht in die aktuelle Anzeige Zeile passt. Die WordWrap-Funktion platziert dieses Wort am Anfang der nächsten Zeile auf der Anzeige. Eine WordWrap-Funktion definiert den Punkt, an dem das System eine Textzeile für mehrzeilige Bearbeitungs Steuerelemente unterbrechen soll, in der Regel bei einem Leerzeichen, das zwei Wörter trennt.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

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

[*Editwordbreakproc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[**EM- \_ Zeilen Trennlinien**](em-fmtlines.md)
</dt> <dt>

[**EM \_ setwordbreakproc**](em-setwordbreakproc.md)
</dt> </dl>

 

