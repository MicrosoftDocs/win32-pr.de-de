---
title: EM_LINEINDEX Meldung (Winuser. h)
description: Ruft den Zeichen Index des ersten Zeichens einer angegebenen Zeile in einem mehrzeiligen Bearbeitungs Steuerelement ab.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- Windows-Steuerelemente für EM_LINEINDEX Meldung
topic_type:
- apiref
api_name:
- EM_LINEINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611d4ff892f95287c45166ae55ff2389f454512c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949711"
---
# <a name="em_lineindex-message-winuserh"></a>EM_LINEINDEX Meldung (Winuser. h)

Ruft den Zeichen Index des ersten Zeichens einer angegebenen Zeile in einem mehrzeiligen Bearbeitungs Steuerelement ab. Ein Zeichen Index ist der null basierte Index des Zeichens vom Anfang des Bearbeitungs Steuer Elements. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

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

Der Rückgabewert ist der Zeichen Index der im *wParam* -Parameter angegebenen Zeile, oder es ist-1, wenn die angegebene Zeilennummer größer als die Anzahl der Zeilen im Bearbeitungs Steuerelement ist.

## <a name="remarks"></a>Bemerkungen

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ linefromchar**](em-linefromchar.md)
</dt> </dl>

 

 





