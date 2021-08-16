---
title: EM_GETPASSWORDCHAR (Winuser.h)
description: Ruft das Kennwortzeichen ab, das ein Bearbeitungssteuerzeichen anzeigt, wenn der Benutzer Text einzugeben. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- EM_GETPASSWORDCHAR von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- EM_GETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c4e7ac576f18d0ab28fcf8c2288d2bee7966866a71180a81c34896c2396f56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831207"
---
# <a name="em_getpasswordchar-message"></a>EM \_ GETPASSWORDCHAR-Nachricht

Ruft das Kennwortzeichen ab, das ein Bearbeitungssteuerzeichen anzeigt, wenn der Benutzer Text einzugeben. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.

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

Der Rückgabewert gibt das Zeichen an, das statt aller vom Benutzer typierten Zeichen angezeigt werden soll. Wenn der Rückgabewert **NULL ist,** gibt es kein Kennwortzeichen, und das Steuerelement zeigt die vom Benutzer eingegebenen Zeichen an.

## <a name="remarks"></a>Hinweise

Wenn ein Bearbeitungssteuerzeichen im [**ES \_ PASSWORD-Format**](edit-control-styles.md) erstellt wird, wird das Standardkennwortzeichen auf ein Sternchen () \* festgelegt. Wenn ein Bearbeitungssteuerzeichen ohne **ES \_ PASSWORD-Format erstellt** wird, ist kein Kennwortzeichen enthalten. Um das Kennwortzeichen zu ändern, senden Sie die [**EM \_ SETPASSWORDCHAR-Nachricht.**](em-setpasswordchar.md)

**Steuerelemente bearbeiten:** Mehrline-Bearbeitungssteuerelemente unterstützen das Kennwortformat oder Nachrichten nicht.

**Umfangreiche Bearbeitung:** Wird in Microsoft Rich Edit 2.0 und höher unterstützt. Sowohl einzeilen- als auch mehrzeilenbasierte Bearbeitungssteuerelemente unterstützen das Kennwortformat und Meldungen. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ SETPASSWORDCHAR**](em-setpasswordchar.md)
</dt> </dl>

 

 





