---
title: EM_SETWORDBREAKPROC Meldung (Winuser. h)
description: Ersetzt die Standard-WordWrap-Funktion eines Bearbeitungs Steuer Elements durch eine Anwendungs definierte WordWrap-Funktion. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: e5029b75-5f35-43a5-876d-24e81605bb49
keywords:
- Windows-Steuerelemente für EM_SETWORDBREAKPROC Meldung
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e85335562c9e9881093d89293e7e2ace9cf43b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517975"
---
# <a name="em_setwordbreakproc-message"></a>EM \_ setwordbreakproc-Meldung

Ersetzt die Standard-WordWrap-Funktion eines Bearbeitungs Steuer Elements durch eine Anwendungs definierte WordWrap-Funktion. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Adresse der Anwendungs definierten WordWrap-Funktion. Weitere Informationen zu Zeilenumbruch finden Sie in der Beschreibung der [*editwordbreakproc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) -Rückruffunktion.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Eine WordWrap-Funktion scannt einen Text Puffer, der Text enthält, der an den Bildschirm gesendet werden soll, und sucht nach dem ersten Wort, das nicht in die aktuelle Bildschirm Zeile passt. Die WordWrap-Funktion legt dieses Wort am Anfang der nächsten Zeile auf dem Bildschirm ab.

Eine WordWrap-Funktion definiert den Punkt, an dem das System eine Textzeile für mehrzeilige Bearbeitungs Steuerelemente unterbrechen soll, in der Regel bei einem Leerzeichen, das zwei Wörter trennt. Diese Funktion kann entweder von einem mehrzeiligen oder einem einzeiligen Bearbeitungs Steuerelement aufgerufen werden, wenn der Benutzer die Pfeiltasten in Kombination mit der STRG-Taste drückt, um die Einfügemarke zum nächsten Wort oder zum vorherigen Wort zu bewegen. Die standardmäßige WordWrap-Funktion unterbricht eine Textzeile bei einem Leerzeichen. Die Anwendungs definierte Funktion definiert möglicherweise, dass der WordWrap-Vorgang bei einem Bindestrich oder einem anderen als dem Leerzeichen auftritt.

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

[**EM \_ getwordbreakproc**](em-getwordbreakproc.md)
</dt> </dl>

 

