---
title: EM_GETFILELINE (CommCtrl.h)
description: Kopiert eine Textzeile aus einem Bearbeitungssteuerfeld, unabhängig davon, wie Zeilen auf dem Bildschirm angezeigt werden, und platziert sie in einem angegebenen Puffer.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETFILELINE message Windows Controls
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
ms.openlocfilehash: 470c437280b279f56c3dcc8b45de93cf3f792afc5053b7e312b2c19c7ffcec8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049220"
---
# <a name="em_getfileline-message-commctrlh"></a>EM_GETFILELINE (CommCtrl.h)

Kopiert eine Textzeile aus einem Bearbeitungssteuerfeld, unabhängig davon, wie Zeilen auf dem Bildschirm angezeigt werden, und platziert sie in einem angegebenen Puffer.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index der Zeile, die aus einem mehrzeilenbasierten Bearbeitungssteuerpunkt abgerufen werden soll. Der Wert 0 (null) gibt die oberste Zeile an. Dieser Parameter wird von einem einzeilenbasierten Bearbeitungssteuer steuerelement ignoriert.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf den Puffer, der eine Kopie der Zeile empfängt. Legen Sie vor dem Senden der Nachricht das erste Wort dieses Puffers auf die Größe des Puffers in **TCHAR** s fest. Für ANSI-Text ist dies die Anzahl von Bytes. für Unicode-Text ist dies die Anzahl von Zeichen. Die Größe im ersten Wort wird durch die kopierte Zeile überschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Anzahl der **kopierten TCHAR-Werte.** Der Rückgabewert ist 0 (null), wenn die durch den *wParam-Parameter* angegebene Zeilennummer größer als die Anzahl der Zeilen im Bearbeitungssteuerzeichen ist.

## <a name="remarks"></a>Hinweise

Die kopierte Zeile enthält kein beendendes NULL-Zeichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur 1809 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2019-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ FILELINELENGTH**](em-filelinelength.md)
</dt> <dt>

[**Bearbeiten \_ von GetFileLine**](/windows/win32/api/commctrl/nf-commctrl-edit_getfileline)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

