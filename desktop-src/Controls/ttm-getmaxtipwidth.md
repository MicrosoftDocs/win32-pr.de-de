---
title: TTM_GETMAXTIPWIDTH Meldung (kommstrg. h)
description: Ruft die maximale Breite für ein QuickInfo-Fenster ab.
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- Windows-Steuerelemente für TTM_GETMAXTIPWIDTH Meldung
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
ms.openlocfilehash: f89c56692db9d451eb18db61af262cc0f3a715f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956487"
---
# <a name="ttm_getmaxtipwidth-message"></a>TTM \_ GetMaxTipWidth-Meldung

Ruft die maximale Breite für ein QuickInfo-Fenster ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **int** -Wert zurück, der die maximale QuickInfo-Breite in Pixel darstellt. Wenn zuvor keine maximale Breite festgelegt wurde, gibt die Meldung-1 zurück.

## <a name="remarks"></a>Bemerkungen

Der Wert für die maximale QuickInfo-Breite zeigt nicht die tatsächliche Breite eines QuickInfo-Fensters an. Wenn eine QuickInfo-Zeichenfolge die maximale Breite überschreitet, unterbricht das Steuerelement den Text in mehrere Zeilen und verwendet Leerzeichen, um Zeilenumbrüche zu bestimmen. Wenn der Text nicht in mehrere Zeilen segmentiert werden kann, wird er in einer einzelnen Zeile angezeigt. Die Länge dieser Zeile kann die maximale QuickInfo-Breite überschreiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TTM \_ SetMaxTipWidth**](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 





