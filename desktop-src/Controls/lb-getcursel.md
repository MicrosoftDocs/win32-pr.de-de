---
title: LB_GETCURSEL Meldung (Winuser. h)
description: Ruft den Index des derzeit ausgewählten Elements (sofern vorhanden) in einem Listenfeld mit einer einzelnen Auswahl ab.
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- Windows-Steuerelemente für LB_GETCURSEL Meldung
topic_type:
- apiref
api_name:
- LB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6209f1f5b67e059f9a2b8a224e6f96ec671e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040953"
---
# <a name="lb_getcursel-message"></a>LB- \_ getcurrsel-Nachricht

Ruft den Index des derzeit ausgewählten Elements (sofern vorhanden) in einem Listenfeld mit einer einzelnen Auswahl ab.

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

Der Rückgabewert in einem Listenfeld mit einer einzelnen Auswahl ist der null basierte Index des aktuell ausgewählten Elements. Wenn keine Auswahl vorhanden ist, lautet der Rückgabewert lb \_ Err.

## <a name="remarks"></a>Bemerkungen

Um die Indizes der ausgewählten Elemente in einem Listenfeld mit Mehrfachauswahl abzurufen, verwenden Sie die [**\_ getselitems**](lb-getselitems.md) -Nachricht. Um zu ermitteln, ob das Element, das das Fokus Rechteck enthält, in einem Mehrfachauswahl-Listenfeld ausgewählt ist, verwenden Sie die [**\_ GetSEL**](lb-getsel.md) -Nachricht "lb".

Beim Senden an ein Listenfeld mit Mehrfachauswahl gibt **lb \_ getcurrsel** den Index des Elements zurück, das über das Fokus Rechteck verfügt. Wenn keine Elemente ausgewählt sind, wird NULL zurückgegeben.

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

[**LB \_ getcaretindex**](lb-getcaretindex.md)
</dt> <dt>

[**LB- \_ GetSEL**](lb-getsel.md)
</dt> <dt>

[**LB- \_ getselitems**](lb-getselitems.md)
</dt> <dt>

[**LB- \_ setcurrsel**](lb-setcursel.md)
</dt> </dl>

 

 





