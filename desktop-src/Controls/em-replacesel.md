---
title: EM_REPLACESEL Meldung (Winuser. h)
description: Ersetzt den markierten Text in einem Bearbeitungs Steuerelement oder in einem Rich-Edit-Steuerelement durch den angegebenen Text.
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- Windows-Steuerelemente für EM_REPLACESEL Meldung
topic_type:
- apiref
api_name:
- EM_REPLACESEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9745b870a310626a6cbbbddbef118a63c64479
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106269"
---
# <a name="em_replacesel-message"></a>EM \_ replacesel-Nachricht

Ersetzt den markierten Text in einem Bearbeitungs Steuerelement oder in einem Rich-Edit-Steuerelement durch den angegebenen Text.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob der Ersetzungs Vorgang rückgängig gemacht werden kann. Wenn dies **zutrifft**, kann der Vorgang rückgängig gemacht werden. Wenn dies **false** ist, kann der Vorgang nicht rückgängig gemacht werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Ersetzungstext enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **EM \_ replacesel** -Nachricht, um nur einen Teil des Texts in einem Bearbeitungs Steuerelement zu ersetzen. Um den gesamten Text zu ersetzen, verwenden Sie die [**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext) -Nachricht.

Wenn keine Auswahl vorhanden ist, wird der Ersetzungstext an der Einfügemarke eingefügt.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

In einem Rich-Edit-Steuerelement übernimmt der Ersetzungstext die Formatierung des Zeichens bei der Einfügemarke oder, wenn eine Auswahl vorliegt, das erste Zeichen in der Auswahl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

