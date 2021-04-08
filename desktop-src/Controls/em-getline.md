---
title: EM_GETLINE Meldung (Winuser. h)
description: Kopiert eine Textzeile aus einem Bearbeitungs Steuerelement und platziert Sie in einem angegebenen Puffer. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- Windows-Steuerelemente für EM_GETLINE Meldung
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e014eaccba65b4ea1fc96e26872954a9cfc06e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949495"
---
# <a name="em_getline-message-winuserh"></a>EM_GETLINE Meldung (Winuser. h)

Kopiert eine Textzeile aus einem Bearbeitungs Steuerelement und platziert Sie in einem angegebenen Puffer. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index der Zeile, die aus einem mehrzeiligen Bearbeitungs Steuerelement abgerufen werden soll. Der Wert 0 (null) gibt die oberste Zeile an. Dieser Parameter wird von einem einzeiligen Bearbeitungs Steuerelement ignoriert.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf den Puffer, der eine Kopie der Zeile empfängt. Legen Sie vor dem Senden der Nachricht das erste Wort dieses Puffers auf die Größe des Puffers in **TCHAR** s fest. Bei ANSI-Text ist dies die Anzahl der Bytes. bei Unicode-Text ist dies die Anzahl der Zeichen. Die Größe im ersten Wort wird von der kopierten Zeile überschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Anzahl der kopierten **TCHAR**-s. Der Rückgabewert ist 0 (null), wenn die durch den *wParam* -Parameter angegebene Zeilennummer größer als die Anzahl der Zeilen im Bearbeitungs Steuerelement ist.

## <a name="remarks"></a>Bemerkungen

Steuer **Elemente bearbeiten:** Die kopierte Zeile enthält kein abschließende Null Zeichen.

**Rich Edit-Steuerelemente:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Die kopierte Zeile enthält kein abschließendes NULL Zeichen, es sei denn, es wurde kein Text kopiert. Wenn kein Text kopiert wurde, legt die Nachricht am Anfang des Puffers ein NULL-Zeichen ab. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

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

[**EM- \_ LineLength**](em-linelength.md)
</dt> <dt>

[**\_Getline bearbeiten**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

