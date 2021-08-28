---
title: CB_LIMITTEXT (Winuser.h)
description: Schränkt die Länge des Texts ein, den der Benutzer in das Bearbeitungssteuerfeld eines Kombinationsfelds eingeben kann.
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- CB_LIMITTEXT der Windows Steuerelemente
topic_type:
- apiref
api_name:
- CB_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e94cdb1bedfb1c0aa3efb401649524782183ced7728304951596c9383efaa0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089080"
---
# <a name="cb_limittext-message"></a>CB \_ LIMITTEXT-Nachricht

Schränkt die Länge des Texts ein, den der Benutzer in das Bearbeitungssteuerfeld eines Kombinationsfelds eingeben kann.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die maximale Anzahl von **TCHARs,** die der Benutzer eingeben kann, ohne das beendende NULL-Zeichen. Wenn dieser Parameter 0 (null) ist, ist die Textlänge auf 0x7FFFFFFE beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist immer **TRUE.**

## <a name="remarks"></a>Hinweise

Wenn das Kombinationsfeld nicht über den [**CBS \_ AUTOHSCROLL-Stil**](combo-box-styles.md) verfügt, hat das Festlegen des Textlimits, das größer als die Größe des Bearbeitungssteuerfelds ist, keine Auswirkungen.

Die **CB \_ LIMITTEXT-Meldung** schränkt nur den Text ein, den der Benutzer eingeben kann. Sie hat keine Auswirkungen auf Text, der sich bereits im Bearbeitungssteuerfeld befindet, wenn die Nachricht gesendet wird, und wirkt sich auch nicht auf die Länge des Texts aus, der in das Bearbeitungssteuerfeld kopiert wird, wenn eine Zeichenfolge im Listenfeld ausgewählt wird.

Der Standardgrenzwert für den Text, den ein Benutzer in das Bearbeitungssteuerfeld eingeben kann, beträgt 30.000 **TCHARs.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



 

 





