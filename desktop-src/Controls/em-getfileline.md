---
title: EM_GETFILELINE Meldung (kommstrg. h)
description: Kopiert eine Textzeile aus einem Bearbeitungs Steuerelement, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden, und platziert Sie in einem angegebenen Puffer.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- Windows-Steuerelemente für EM_GETFILELINE Meldung
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 6b3be3ea4ae883fc808f7ddc8fb60f0d93bcd6ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477919"
---
# <a name="em_getfileline-message-commctrlh"></a>EM_GETFILELINE Meldung (kommstrg. h)

Kopiert eine Textzeile aus einem Bearbeitungs Steuerelement, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden, und platziert Sie in einem angegebenen Puffer.

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

Die kopierte Zeile enthält kein abschließende Null Zeichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10, 1809 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2019 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ filelinelength**](em-filelinelength.md)
</dt> <dt>

[**\_Getfileline bearbeiten**](/windows/win32/api/commctrl/nf-commctrl-edit_getfileline)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

