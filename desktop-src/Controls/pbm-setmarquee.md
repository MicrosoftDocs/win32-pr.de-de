---
title: PBM_SETMARQUEE Meldung (Commctrl.h)
description: Legt die Statusanzeige auf den Festlaufmodus fest. Dies bewirkt, dass sich die Statusanzeige wie ein Marquee bewegt.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- PBM_SETMARQUEE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- PBM_SETMARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f724f87faa6e989fddb17e8d6fb3b115dd04859ea426addb7d4c0b893aff407a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986140"
---
# <a name="pbm_setmarquee-message"></a>PBM \_ SETMARQUEE-Nachricht

Legt die Statusanzeige auf den Festlaufmodus fest. Dies bewirkt, dass sich die Statusanzeige wie ein Marquee bewegt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob der Festlaufmodus aktiviert oder deaktiviert werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>Zeit in Millisekunden zwischen Aktualisierungen der Marquee-Animation. Wenn dieser Parameter 0 (null) ist, wird die Marquee-Animation alle 30 Millisekunden aktualisiert.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **TRUE** zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Meldung, wenn Sie den Fortschritt bis zum Abschluss nicht kennen, aber angeben möchten, dass der Fortschritt erfolgt.

Senden Sie die **PBM \_ SETMARQUEE-Nachricht,** um die Animation zu starten oder zu beenden.

> [!Note]  
> Sie müssen den Steuerelementstil auf [**PBS \_ MARQUEE**](progress-bar-control-styles.md) festlegen, bevor Sie versuchen, die Animation zu starten.

 

> [!Note]  
> Diese Meldung erfordert ComCtl32.dll Version 6.00 oder höher.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





