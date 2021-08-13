---
title: TTM_SETMAXTIPWIDTH (Commctrl.h)
description: Legt die maximale Breite für ein QuickInfo-Fenster fest.
ms.assetid: 3cfb6011-d0c3-4a57-aead-d4ec09a057cc
keywords:
- TTM_SETMAXTIPWIDTH meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TTM_SETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d344a3abcbe2b3bf57a71c8020d383f76ab1922b9009cd69411912d4468fa19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433760"
---
# <a name="ttm_setmaxtipwidth-message"></a>\_TTM-Nachricht "SETMAXTIPWIDTH"

Legt die maximale Breite für ein QuickInfo-Fenster fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Maximale Breite des QuickInfo-Fensters oder -1, um eine beliebige Breite zu ermöglichen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige maximale QuickInfo-Breite zurück.

## <a name="remarks"></a>Hinweise

Der Wert für die maximale Breite gibt nicht die tatsächliche Breite eines QuickInfo-Fensters an. Wenn eine QuickInfo-Zeichenfolge die maximale Breite überschreitet, unterbricht das Steuerelement den Text stattdessen in mehrere Zeilen und verwendet Leerzeichen, um Zeilenumbrüche zu bestimmen. Wenn der Text nicht in mehrere Zeilen segmentiert werden kann, wird er in einer einzelnen Zeile angezeigt, die die maximale QuickInfo-Breite überschreiten kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**TTM \_ GETMAXTIPWIDTH**](ttm-getmaxtipwidth.md)
</dt> </dl>

 

 





