---
title: TB_GETSTRING (Commctrl.h)
description: Ruft eine Zeichenfolge aus dem Zeichenfolgenpool einer Symbolleiste ab.
ms.assetid: a5f80c16-bc6d-466d-8ec6-77451432148e
keywords:
- TB_GETSTRING message Windows Controls
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
ms.openlocfilehash: d25cbf20fd084c2ce60b29d131b7f488ca2b8cee178a2218fcfac191b3c1af33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918482"
---
# <a name="tb_getstring-message"></a>TB \_ GETSTRING-Nachricht

Ruft eine Zeichenfolge aus dem Zeichenfolgenpool einer Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LOWORD gibt**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) die Länge des *lParam-Puffers* in Bytes an. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Index der Zeichenfolge an.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Puffer, der zum Zurückgeben der Zeichenfolge verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Zeichenfolgenlänge zurück, wenn erfolgreich, andernfalls -1.

## <a name="remarks"></a>Hinweise

Diese Meldung gibt die angegebene Zeichenfolge aus dem Zeichenfolgenpool der Symbolleiste zurück. Er entspricht nicht unbedingt der Textzeichenfolge, die derzeit von einer Schaltfläche angezeigt wird. Um die aktuelle Textzeichenfolge einer Schaltfläche abzurufen, senden Sie der Symbolleiste eine [**\_ GETBUTTONTEXT-TB-Nachricht.**](tb-getbuttontext.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ GETSTRINGW** (Unicode) und **TB \_ GETSTRINGA** (ANSI)<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**TB \_ ADDSTRING**](tb-addstring.md)
</dt> <dt>

[**TB \_ ADDBUTTONS**](tb-addbuttons.md)
</dt> <dt>

[**TB \_ INSERTBUTTON**](tb-insertbutton.md)
</dt> </dl>

 

