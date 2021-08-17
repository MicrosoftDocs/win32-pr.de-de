---
title: EM_SETPASSWORDCHAR Meldung (Winuser.h)
description: Legt das Kennwortzeichen für ein Bearbeitungssteuerelement fest oder entfernt es. Wenn ein Kennwortzeichen festgelegt wird, wird dieses Zeichen anstelle der vom Benutzer eingegebenen Zeichen angezeigt. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- EM_SETPASSWORDCHAR Windows-Steuerelementen
topic_type:
- apiref
api_name:
- EM_SETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56cdfbc108ad5bc1b3e2e11b72937a92da473bcbfa01e974056743ed2e6fde1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412315"
---
# <a name="em_setpasswordchar-message"></a>EM \_ SETPASSWORDCHAR-Meldung

Legt das Kennwortzeichen für ein Bearbeitungssteuerelement fest oder entfernt es. Wenn ein Kennwortzeichen festgelegt wird, wird dieses Zeichen anstelle der vom Benutzer eingegebenen Zeichen angezeigt. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Zeichen, das anstelle der vom Benutzer eingegebenen Zeichen angezeigt werden soll. Wenn dieser Parameter 0 (null) ist, entfernt das Steuerelement das aktuelle Kennwortzeichen und zeigt die vom Benutzer eingegebenen Zeichen an.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn ein Bearbeitungssteuerelement die **EM \_ SETPASSWORDCHAR-Meldung** empfängt, werden alle sichtbaren Zeichen mithilfe des durch den *wParam-Parameter* angegebenen Zeichens neu gezeichnet. Wenn *wParam 0* (null) ist, zeichnet das Steuerelement alle sichtbaren Zeichen mithilfe der vom Benutzer eingegebenen Zeichen neu.

Wenn ein Bearbeitungssteuerelement im [**ES \_ PASSWORD-Format**](edit-control-styles.md) erstellt wird, wird das Standardkennwortzeichen auf ein Sternchen \* () festgelegt. Wenn ein Bearbeitungssteuerelement ohne das **ES \_ PASSWORD-Format** erstellt wird, ist kein Kennwortzeichen vorhanden. Das **ES \_ PASSWORD-Format** wird entfernt, wenn eine **EM \_ SETPASSWORDCHAR-Nachricht** gesendet wird, wobei der *wParam-Parameter* auf 0 (null) festgelegt ist.

**Bearbeiten von Steuerelementen:** Mehrzeilige Bearbeitungssteuerelemente unterstützen weder das Kennwortformat noch Meldungen.

**Rich Edit:** Wird in Microsoft Rich Edit 2.0 und höher unterstützt. Sowohl einzeilige als auch mehrzeilige Bearbeitungssteuerelemente unterstützen das Kennwortformat und Nachrichten. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ GETPASSWORDCHAR**](em-getpasswordchar.md)
</dt> </dl>

 

 





