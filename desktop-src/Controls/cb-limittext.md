---
title: CB_LIMITTEXT Meldung (Winuser. h)
description: Schränkt die Länge des Texts ein, den der Benutzer in das Bearbeitungs Steuerelement eines Kombinations Felds eingeben darf.
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- Windows-Steuerelemente für CB_LIMITTEXT Meldung
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
ms.openlocfilehash: 34ea9ccd63bb1503e73aebdd584a53bc32bcb8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040595"
---
# <a name="cb_limittext-message"></a>CB- \_ limittext Nachricht

Schränkt die Länge des Texts ein, den der Benutzer in das Bearbeitungs Steuerelement eines Kombinations Felds eingeben darf.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die maximale Anzahl von **tchars** , die vom Benutzer eingegeben werden können, ohne das abschließende Null Zeichen. Wenn dieser Parameter 0 (null) ist, ist die Textlänge auf 0x7ffffffe-Zeichen beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist immer " **true**".

## <a name="remarks"></a>Bemerkungen

Wenn das Kombinations Feld den [**\_ autohscroll**](combo-box-styles.md) -Stil "CBS" nicht aufweist, hat das Festlegen des Text Limits auf einen höheren Wert als die Größe des Bearbeitungs Steuer Elements keine Auswirkungen.

Die **CB- \_ limittext** -Nachricht schränkt nur den Text ein, den der Benutzer eingeben kann. Sie hat keine Auswirkung auf einen Text, der sich bereits im Bearbeitungs Steuerelement befindet, wenn die Nachricht gesendet wird, und wirkt sich auch nicht auf die Länge des Texts aus, der in das Bearbeitungs Steuerelement kopiert wird, wenn eine Zeichenfolge im Listenfeld ausgewählt ist.

Der Standard Grenzwert für den Text, den ein Benutzer im Bearbeitungs Steuerelement eingeben kann, ist 30.000 **tchars**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



 

 





