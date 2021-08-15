---
title: EM_GETLINECOUNT-Nachricht (Winuser.h)
description: Ruft die Anzahl der Zeilen in einem mehrzeiligen Bearbeitungssteuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETLINECOUNT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETLINECOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44487084da8df8edd463fc0683c9d27fcba19a2993465e5493edfd8bb7c3c6b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006683"
---
# <a name="em_getlinecount-message-winuserh"></a>EM_GETLINECOUNT-Nachricht (Winuser.h)

Ruft die Anzahl der Zeilen in einem mehrzeiligen Bearbeitungssteuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.

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

Der Rückgabewert ist eine ganze Zahl, die die Gesamtzahl der Textzeilen im Mehrzeilen-Bearbeitungssteuerelement oder Rich Edit-Steuerelement angibt. Wenn das Steuerelement keinen Text enthält, ist der Rückgabewert 1. Der Rückgabewert ist nie kleiner als 1.

## <a name="remarks"></a>Hinweise

Die **EM \_ GETLINECOUNT-Nachricht** ruft die Gesamtzahl der Textzeilen ab, nicht nur die Anzahl der derzeit sichtbaren Zeilen.

Wenn das Wordwrap-Feature aktiviert ist, kann sich die Anzahl der Zeilen ändern, wenn sich die Abmessungen des Bearbeitungsfensters ändern.

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

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

[**EM \_ GETLINE**](em-getline.md)
</dt> <dt>

[**EM \_ LINELENGTH**](em-linelength.md)
</dt> <dt>

[**GetLineCount bearbeiten \_**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
</dt> </dl>

 

 





