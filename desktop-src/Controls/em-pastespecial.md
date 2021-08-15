---
title: EM_PASTESPECIAL (Richedit.h)
description: Eingefügt ein bestimmtes Zwischenablageformat in ein Rich-Edit-Steuerelement.
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- EM_PASTESPECIAL meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_PASTESPECIAL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc1af4dd0566cdf8e256b34f87fcc52ea855bc521c87cbe390e02b8b1cf7b06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412801"
---
# <a name="em_pastespecial-message"></a>\_EM-PASTESPECIAL-Nachricht

Eingefügt ein bestimmtes Zwischenablageformat in ein Rich-Edit-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die [Zwischenablageformate an.](/windows/desktop/dataxchg/clipboard-formats)

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**REPASTESPECIAL-Struktur**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) oder **NULL.** Wenn ein Objekt eingefüllt wird, wird die **REPASTESPECIAL-Struktur** mit dem gewünschten Anzeigeaspekt gefüllt. Wenn *lParam* **NULL ist** oder das **dwAspect-Member** 0 (null) ist, wird der Inhalt des Objektdeskriptors als Anzeigeaspekt verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

