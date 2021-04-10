---
title: CB_SETCURSEL Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB \_ setcurrsel-Nachricht, um eine Zeichenfolge in der Liste eines Kombinations Felds auszuwählen.
ms.assetid: d4ce3811-6e0a-4952-97cf-ba6efde0de0d
keywords:
- Windows-Steuerelemente für CB_SETCURSEL Meldung
topic_type:
- apiref
api_name:
- CB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd130204e6dc8bb4166c21bc9c4d52950182c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040591"
---
# <a name="cb_setcursel-message"></a>CB- \_ setcurrsel-Meldung

Eine Anwendung sendet eine **CB \_ setcurrsel** -Nachricht, um eine Zeichenfolge in der Liste eines Kombinations Felds auszuwählen. Bei Bedarf führt die Liste einen Bildlauf in der Zeichenfolge durch. Der Text im Bearbeitungs Steuerelement des Kombinations Felds ändert sich, um die neue Auswahl widerzuspiegeln, und jede vorherige Auswahl in der Liste wird entfernt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den NULL basierten Index der auszuwählen Zeichenfolge an. Wenn dieser Parameter-1 ist, wird jede aktuelle Auswahl in der Liste entfernt, und das Bearbeitungs Steuerelement wird gelöscht.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert der Index des ausgewählten Elements. Wenn *wParam* größer als die Anzahl der Elemente in der Liste ist oder wenn *wParam* den Wert-1 aufweist, ist der Rückgabewert CB \_ Err, und die Auswahl wird gelöscht.

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

[**CB- \_ FindString**](cb-findstring.md)
</dt> <dt>

[**CB \_ getcurrsel**](cb-getcursel.md)
</dt> <dt>

[**CB- \_ SelectString**](cb-selectstring.md)
</dt> </dl>

 

 





