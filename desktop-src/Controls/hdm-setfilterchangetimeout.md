---
title: HDM_SETFILTERCHANGETIMEOUT Meldung (kommstrg. h)
description: Legt das Timeout Intervall zwischen dem Zeitpunkt fest, an dem eine Änderung in den Filter Attributen stattfindet, und dem Veröffentlichen einer Hdn \_ FilterChange-Benachrichtigung. Sie können diese Nachricht explizit senden oder das-Header \_ setfilterchangetimeout-Makro verwenden.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- Windows-Steuerelemente für HDM_SETFILTERCHANGETIMEOUT Meldung
topic_type:
- apiref
api_name:
- HDM_SETFILTERCHANGETIMEOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9876634d12cd15001c296151694cb755ed1b34e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040857"
---
# <a name="hdm_setfilterchangetimeout-message"></a>HDM- \_ setfilterchangetimeout-Meldung

Legt das Timeout Intervall zwischen dem Zeitpunkt fest, an dem eine Änderung in den Filter Attributen stattfindet, und dem Veröffentlichen einer [Hdn \_ FilterChange](hdn-filterchange.md) -Benachrichtigung. Sie können diese Nachricht explizit senden oder das- [**Header \_ setfilterchangetimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Der Timeoutwert in Millisekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des geänderten Filter Steuer Elements zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Hdn- \_ Filter Änderung](hdn-filterchange.md)
</dt> </dl>

 

 





