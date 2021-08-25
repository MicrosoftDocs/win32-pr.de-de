---
title: EM_FILELINEINDEX Meldung (CommCtrl.h)
description: Ruft den Zeichenindex des ersten Zeichens einer angegebenen Zeile in einem mehrzeiligen Bearbeitungssteuerelement ab, unabhängig davon, wie Zeilen auf dem Bildschirm angezeigt werden.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_FILELINEINDEX Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_FILELINEINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7c4bd1f21ee6bcdf7bec56828ea9c2996c837def614c0c537ef83ee053ebfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915610"
---
# <a name="em_filelineindex-message-commctrlh"></a>EM_FILELINEINDEX Meldung (CommCtrl.h)

Ruft den Zeichenindex des ersten Zeichens einer angegebenen Zeile in einem mehrzeiligen Bearbeitungssteuerelement ab, unabhängig davon, wie Zeilen auf dem Bildschirm angezeigt werden. Ein Zeichenindex ist der nullbasierte Index des Zeichens vom Anfang des Bearbeitungssteuerelements.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die nullbasierte Zeilennummer. Der Wert -1 gibt die aktuelle Zeilennummer an (die Zeile, die das Caretzeichen enthält).

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Zeichenindex der im *wParam-Parameter* angegebenen Zeile, unabhängig davon, wie Zeilen auf dem Bildschirm angezeigt werden, oder -1, wenn die angegebene Zeilennummer größer als die Anzahl der Zeilen im Bearbeitungssteuerelement ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur 1809 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2019-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ FILELINEFROMCHAR**](em-filelinefromchar.md)
</dt> </dl>

 

 





