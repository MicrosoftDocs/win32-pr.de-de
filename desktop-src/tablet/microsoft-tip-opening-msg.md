---
description: Benachrichtigt das Fenster, wenn der Text Eingabebereich geöffnet wird.
ms.assetid: 6eadd648-bffb-4227-bdcd-cd733f692734
title: MICROSOFT_TIP_OPENING_MSG Meldung ("Pendel Panel. h")
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0938b8a00e39f54817b8ec52e86e00aae52111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372492"
---
# <a name="microsoft_tip_opening_msg-message"></a>\_Meldung zum \_ Öffnen der \_ Nachricht von Microsoft Tip

Benachrichtigt das Fenster, wenn der Text Eingabebereich geöffnet wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wird derzeit nicht verwendet, sollte **null** sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Wird derzeit nicht verwendet, sollte **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Anwendungen sollten [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) nach der Verarbeitung dieser Nachricht anrufen. Weitere Informationen zu den Rückgabe Werten finden Sie unter **defwindowproc** .

## <a name="remarks"></a>Bemerkungen

Diese Benachrichtigung informiert Sie, wenn der Eingabebereich geöffnet wird. Wenn Sie in diesem Fall eine Aktion durchführen möchten, behandeln Sie die Nachricht, führen Sie den Vorgang im Handler aus, und übergeben Sie die Nachricht dann an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

> [!Note]  
> Diese Meldung wird auch gesendet, wenn der Text Eingabebereich bereits sichtbar ist und der Benutzer von der Tastatur zur Handschrift Skin wechselt.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista<br/>                                                                   |
| Header<br/> | <dl> <dt>"Pendel Panel. h"</dt> </dl> |



 

