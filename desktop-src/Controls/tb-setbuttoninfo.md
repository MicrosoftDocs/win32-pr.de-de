---
title: TB_SETBUTTONINFO Meldung (Commctrl.h)
description: Legt die Informationen für eine vorhandene Schaltfläche in einer Symbolleiste fest.
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- TB_SETBUTTONINFO Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_SETBUTTONINFO
- TB_SETBUTTONINFOA
- TB_SETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e9fa1da0f9556c025b83ac2b3345680fe11dac0dd15e202ed7336cacfe511e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829624"
---
# <a name="tb_setbuttoninfo-message"></a>TB \_ SETBUTTONINFO-Meldung

Legt die Informationen für eine vorhandene Schaltfläche in einer Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Schaltflächenbezeichner.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TBBUTTONINFO-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) die die neuen Schaltflächeninformationen enthält. Die **CbSize-** und **dwMask-Member** dieser Struktur müssen vor dem Senden dieser Nachricht ausgefüllt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück. Andernfalls wird 0 (null) zurückgegeben.

## <a name="remarks"></a>Hinweise

Text wird Schaltflächen häufig zugewiesen, wenn sie einer Symbolleiste hinzugefügt werden, indem der Index einer Zeichenfolge im Zeichenfolgenpool der Symbolleiste angegeben wird. Wenn Sie eine **TB \_ SETBUTTONINFO** verwenden, um einer Schaltfläche neuen Text zuzuweisen, wird der Text aus dem Zeichenfolgenpool dauerhaft überschrieben. Sie können den Text ändern, indem Sie **TB \_ SETBUTTONINFO** erneut aufrufen, aber Sie können die Zeichenfolge nicht aus dem Zeichenfolgenpool neu zuweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ SETBUTTONINFOW** (Unicode) und **TB \_ SETBUTTONINFOA** (ANSI)<br/>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**TB \_ ADDBUTTONS**](tb-addbuttons.md)
</dt> <dt>

[**TB \_ GETBUTTONINFO**](tb-getbuttoninfo.md)
</dt> <dt>

[**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> <dt>

[**TB \_ GETSTRING**](tb-getstring.md)
</dt> <dt>

[**TB \_ INSERTBUTTON**](tb-insertbutton.md)
</dt> </dl>

 

 





