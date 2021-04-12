---
title: TTM_SETMAXTIPWIDTH Meldung (kommstrg. h)
description: Legt die maximale Breite für ein QuickInfo-Fenster fest.
ms.assetid: 3cfb6011-d0c3-4a57-aead-d4ec09a057cc
keywords:
- Windows-Steuerelemente für TTM_SETMAXTIPWIDTH Meldung
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
ms.openlocfilehash: 55ce930b289205b5fb0d2768068b8cb28cd11aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213715"
---
# <a name="ttm_setmaxtipwidth-message"></a>TTM \_ SetMaxTipWidth-Meldung

Legt die maximale Breite für ein QuickInfo-Fenster fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Maximale QuickInfo-Fensterbreite oder-1, um eine beliebige Breite zuzulassen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige maximale QuickInfo-Breite zurück.

## <a name="remarks"></a>Bemerkungen

Der Wert für die maximale Breite zeigt nicht die tatsächliche Breite eines QuickInfo-Fensters an. Wenn eine QuickInfo-Zeichenfolge die maximale Breite überschreitet, unterbricht das Steuerelement den Text in mehrere Zeilen und verwendet Leerzeichen, um Zeilenumbrüche zu bestimmen. Wenn der Text nicht in mehrere Zeilen segmentiert werden kann, wird er in einer einzelnen Zeile angezeigt, die die maximale QuickInfo-Breite überschreiten kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TTM \_ GetMaxTipWidth**](ttm-getmaxtipwidth.md)
</dt> </dl>

 

 





