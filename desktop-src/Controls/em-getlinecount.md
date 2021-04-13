---
title: EM_GETLINECOUNT Meldung (Winuser. h)
description: Ruft die Anzahl der Zeilen in einem mehrzeiligen Bearbeitungs Steuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- Windows-Steuerelemente für EM_GETLINECOUNT Meldung
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
ms.openlocfilehash: 15ffbeafb13850317faccb4be44571d81b0d7e36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475570"
---
# <a name="em_getlinecount-message-winuserh"></a>EM_GETLINECOUNT Meldung (Winuser. h)

Ruft die Anzahl der Zeilen in einem mehrzeiligen Bearbeitungs Steuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

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

Der Rückgabewert ist eine ganze Zahl, die die Gesamtzahl der Textzeilen im mehrzeiligen Bearbeitungs Steuerelement oder im Rich Edit-Steuerelement angibt. Wenn das Steuerelement keinen Text hat, ist der Rückgabewert 1. Der Rückgabewert ist nie kleiner als 1.

## <a name="remarks"></a>Bemerkungen

Die **EM \_ getLineCount** -Nachricht Ruft die Gesamtanzahl von Textzeilen ab, nicht nur die Anzahl der Zeilen, die zurzeit sichtbar sind.

Wenn die Funktion "WordWrap" aktiviert ist, kann sich die Anzahl der Zeilen ändern, wenn sich die Abmessungen des Bearbeitungsfensters ändern.

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

[**EM \_ getline**](em-getline.md)
</dt> <dt>

[**EM- \_ LineLength**](em-linelength.md)
</dt> <dt>

[**\_GetLineCount bearbeiten**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
</dt> </dl>

 

 





