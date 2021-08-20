---
title: TB_GETBUTTONTEXT-Nachricht (Commctrl.h)
description: Ruft den Anzeigetext einer Schaltfläche auf einer Symbolleiste ab.
ms.assetid: 16dd7181-a404-4056-b084-05f49f5a4b14
keywords:
- TB_GETBUTTONTEXT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_GETBUTTONTEXT
- TB_GETBUTTONTEXTA
- TB_GETBUTTONTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ec63815886ecc32f8f0b0759b9f6a8cf847bfe56e6c898fd6e3a3ae8e0f40ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829766"
---
# <a name="tb_getbuttontext-message"></a>TB \_ GETBUTTONTEXT-Nachricht

Ruft den Anzeigetext einer Schaltfläche auf einer Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Befehlsbezeichner der Schaltfläche, deren Text abgerufen werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Puffer, der den Schaltflächentext empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Länge der Zeichenfolge in Zeichen zurück, auf die *lParam* zeigt. Die Länge enthält nicht das abschließende NULL-Zeichen. Wenn der Wert nicht erfolgreich ist, lautet der Rückgabewert -1.

## <a name="remarks"></a>Hinweise

**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies die Sicherheit Ihres Programms beeinträchtigen. Diese Meldung bietet keine Möglichkeit, die Größe des Puffers zu kennen. Wenn Sie diese Nachricht verwenden, rufen Sie zuerst die Nachricht auf, die **NULL** in *lParam* übergibt. Dies gibt die Anzahl von Zeichen zurück, mit Ausnahme von **NULL,** die erforderlich sind. Rufen Sie dann die Nachricht ein zweites Mal auf, um die Zeichenfolge abzurufen. Lesen Sie die [Sicherheitsüberlegungen: Microsoft Windows Controls,](sec-comctls.md) bevor Sie fortfahren.

Die zurückgegebene Zeichenfolge entspricht dem Text, der derzeit von der Schaltfläche angezeigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ GETBUTTONTEXTW** (Unicode) und **TB \_ GETBUTTONTEXTA** (ANSI)<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**TB \_ GETBUTTONINFO**](tb-getbuttoninfo.md)
</dt> <dt>

[**TB \_ GETSTRING**](tb-getstring.md)
</dt> <dt>

[**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> </dl>

 

 





