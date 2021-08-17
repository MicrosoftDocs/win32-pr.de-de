---
title: CB_SETEDITSEL Meldung (Winuser.h)
description: Eine Anwendung sendet eine CB \_ SETEDITSEL-Nachricht, um Zeichen im Bearbeitungssteuerelement eines Kombinationsfelds auszuwählen.
ms.assetid: 25a07341-a21c-42a9-a220-62650997757b
keywords:
- CB_SETEDITSEL Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- CB_SETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e8deb133559332ea8f727758086e19cb17483b4c343f8b3f8f1a3694911eedd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832268"
---
# <a name="cb_seteditsel-message"></a>CB \_ SETEDITSEL-Nachricht

Eine Anwendung sendet eine **CB \_ SETEDITSEL-Nachricht,** um Zeichen im Bearbeitungssteuerelement eines Kombinationsfelds auszuwählen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

[**LowORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) von *lParam* gibt die Anfangsposition an. Wenn **LOWORD** -1 ist, wird ggf. die Auswahl entfernt.

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) von *lParam* gibt die Endposition an. Wenn **HIWORD** -1 ist, wird der gesamte Text von der Anfangsposition bis zum letzten Zeichen im Bearbeitungssteuerelement ausgewählt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert **TRUE.** Wenn die Nachricht an ein Kombinationsfeld mit dem [**\_ CBS-DROPDOWNLIST-Format**](combo-box-styles.md) gesendet wird, handelt es sich um CB \_ ERR.

## <a name="remarks"></a>Hinweise

Die Positionen sind nullbasiert. Das erste Zeichen des Bearbeitungssteuerelements befindet sich an der Nullposition. Das erste Zeichen nach dem letzten ausgewählten Zeichen befindet sich an der Endposition. Um beispielsweise die ersten vier Zeichen des Bearbeitungssteuerelements auszuwählen, verwenden Sie eine Anfangsposition von 0 und eine Endposition von 4.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**CB \_ GETEDITSEL**](cb-geteditsel.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

