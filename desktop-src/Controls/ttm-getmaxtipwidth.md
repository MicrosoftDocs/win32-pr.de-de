---
title: TTM_GETMAXTIPWIDTH Nachricht (Commctrl.h)
description: Ruft die maximale Breite für ein QuickInfo-Fenster ab.
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- TTM_GETMAXTIPWIDTH Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TTM_GETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bce561b254645932b214b48879aa0be04deb31b32e8dc591fc3183ec39871273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751050"
---
# <a name="ttm_getmaxtipwidth-message"></a>TTM \_ GETMAXTIPWIDTH-Nachricht

Ruft die maximale Breite für ein QuickInfo-Fenster ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **INT-Wert** zurück, der die maximale QuickInfo-Breite in Pixel darstellt. Wenn zuvor keine maximale Breite festgelegt wurde, gibt die Nachricht -1 zurück.

## <a name="remarks"></a>Hinweise

Der Wert für die maximale QuickInfo-Breite gibt nicht die tatsächliche Breite eines QuickInfo-Fensters an. Wenn eine QuickInfo-Zeichenfolge stattdessen die maximale Breite überschreitet, unterbricht das Steuerelement den Text in mehrere Zeilen und verwendet Leerzeichen, um Zeilenumbrüche zu bestimmen. Wenn der Text nicht in mehrere Zeilen segmentiert werden kann, wird er in einer einzelnen Zeile angezeigt. Die Länge dieser Zeile kann die maximale QuickInfo-Breite überschreiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 





