---
title: EM_FILELINEINDEX Meldung (kommstrg. h)
description: Ruft den Zeichen Index des ersten Zeichens einer angegebenen Zeile in einem mehrzeiligen Bearbeitungs Steuerelement ab, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- Windows-Steuerelemente für EM_FILELINEINDEX Meldung
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
ms.openlocfilehash: a4ce5f5ca07fc9fb9869898965422c7c8a6aa3fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104228"
---
# <a name="em_filelineindex-message-commctrlh"></a>EM_FILELINEINDEX Meldung (kommstrg. h)

Ruft den Zeichen Index des ersten Zeichens einer angegebenen Zeile in einem mehrzeiligen Bearbeitungs Steuerelement ab, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden. Ein Zeichen Index ist der null basierte Index des Zeichens vom Anfang des Bearbeitungs Steuer Elements.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die null basierte Zeilennummer. Der Wert-1 gibt die aktuelle Zeilennummer an (die Zeile, die die Einfügemarke enthält).

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Zeichen Index der im *wParam* -Parameter angegebenen Zeile, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden, oder es ist-1, wenn die angegebene Zeilennummer größer als die Anzahl der Zeilen im Bearbeitungs Steuerelement ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10, 1809 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2019 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ filelinefromchar**](em-filelinefromchar.md)
</dt> </dl>

 

 





