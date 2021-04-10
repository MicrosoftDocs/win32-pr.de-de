---
title: TB_GETSTRING Meldung (kommstrg. h)
description: Ruft eine Zeichenfolge aus dem Zeichen folgen Pool einer Symbolleiste ab.
ms.assetid: a5f80c16-bc6d-466d-8ec6-77451432148e
keywords:
- Windows-Steuerelemente für TB_GETSTRING Meldung
topic_type:
- apiref
api_name:
- TB_GETSTRING
- TB_GETSTRINGA
- TB_GETSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465ad2546397fa31c33d6a52b4989902c979d91d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040365"
---
# <a name="tb_getstring-message"></a>TB \_ GetString-Nachricht

Ruft eine Zeichenfolge aus dem Zeichen folgen Pool einer Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die Länge des *LPARAM* -Puffers in Bytes an. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Index der Zeichenfolge an.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Puffer, der zum Zurückgeben der Zeichenfolge verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Zeichen folgen Länge zurück, wenn erfolgreich, andernfalls-1.

## <a name="remarks"></a>Bemerkungen

Diese Meldung gibt die angegebene Zeichenfolge aus dem Zeichen folgen Pool der Symbolleiste zurück. Sie entspricht nicht notwendigerweise der Text Zeichenfolge, die derzeit von einer Schaltfläche angezeigt wird. Um die aktuelle Text Zeichenfolge einer Schaltfläche abzurufen, senden Sie der Symbolleiste eine [**TB \_ getbuttontext**](tb-getbuttontext.md) -Nachricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ Getstringw** (Unicode) und **TB \_ getstraninga** (ANSI)<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**TB \_ AddString**](tb-addstring.md)
</dt> <dt>

[**TB ( \_ AddButtons)**](tb-addbuttons.md)
</dt> <dt>

[**TB ( \_ InsertButton)**](tb-insertbutton.md)
</dt> </dl>

 

