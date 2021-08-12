---
title: TB_GETBUTTONINFO Meldung (Commctrl.h)
description: Ruft erweiterte Informationen für eine Schaltfläche in einer Symbolleiste ab.
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- TB_GETBUTTONINFO Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_GETBUTTONINFO
- TB_GETBUTTONINFOA
- TB_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 457b8ca82d570b9d6c55cf97392803fce9a81cbe1d5db8122fcdaa975dd99d5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669933"
---
# <a name="tb_getbuttoninfo-message"></a>TB \_ GETBUTTONINFO-Nachricht

Ruft erweiterte Informationen für eine Schaltfläche in einer Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Befehlsbezeichner der Schaltfläche.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TBBUTTONINFO-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) die die Schaltflächeninformationen empfängt. Die **CbSize-** und **dwMask-Member** dieser Struktur müssen vor dem Senden dieser Nachricht ausgefüllt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den nullbasierten Index der Schaltfläche oder -1 zurück, wenn ein Fehler auftritt.

## <a name="remarks"></a>Hinweise

Wenn Sie [**TB \_ ADDBUTTONS**](tb-addbuttons.md) oder [**TB \_ INSERTBUTTON**](tb-insertbutton.md) verwenden, um Schaltflächen auf der Symbolleiste zu platzieren, wird der Schaltflächentext häufig durch den Index des Zeichenfolgenpools angegeben. **TB \_ GETBUTTONINFO** ruft diese Zeichenfolge nicht ab. Um **TB \_ GETBUTTONINFO** zum Abrufen von Schaltflächentext zu verwenden, müssen Sie zuerst die Textzeichenfolge mit [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)festlegen. Nachdem Sie den Schaltflächentext mit **TB \_ SETBUTTONINFO** festgelegt haben, können Sie den Zeichenfolgenpoolindex nicht mehr verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ GETBUTTONINFOW** (Unicode) und **TB \_ GETBUTTONINFOA** (ANSI)<br/>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> <dt>

[**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> </dl>

 

 





