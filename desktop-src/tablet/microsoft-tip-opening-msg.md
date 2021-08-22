---
description: Benachrichtigt das Fenster, wenn der Texteingabebereich geöffnet wird.
ms.assetid: 6eadd648-bffb-4227-bdcd-cd733f692734
title: MICROSOFT_TIP_OPENING_MSG Nachricht (Peninputpanel.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e183cc426cd5d73e52c6aaef007bc5579ceb3eb0f4ceaf3f9f4084677b7a556
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335900"
---
# <a name="microsoft_tip_opening_msg-message"></a>MICROSOFT \_ TIP \_ OPENING \_ MSG message

Benachrichtigt das Fenster, wenn der Texteingabebereich geöffnet wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Derzeit nicht verwendet, sollte **NULL** sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Derzeit nicht verwendet, sollte **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Anwendungen sollten [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) aufrufen, nachdem diese Meldung verarbeitet wurde. Informationen zu den Rückgabewerten finden Sie unter **DefWindowProc.**

## <a name="remarks"></a>Hinweise

Diese Benachrichtigung informiert Sie, wenn der Eingabebereich geöffnet wird. Wenn Sie in diesem Fall eine Aktion ausführen möchten, behandeln Sie die Nachricht, führen Sie den Vorgang im Handler aus, und übergeben Sie die Nachricht dann an [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

> [!Note]  
> Diese Meldung wird auch gesendet, wenn der Texteingabebereich bereits sichtbar ist und der Benutzer von der Tastatur zur Handschrift wechselt.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista<br/>                                                                   |
| Header<br/> | <dl> <dt>Peninputpanel.h</dt> </dl> |



 

