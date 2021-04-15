---
title: MCM_GETCURSEL Meldung (kommstrg. h)
description: Ruft das aktuell ausgewählte Datum ab. Sie können diese Nachricht explizit oder mit dem monthcal \_ getcurrsel-Makro senden.
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- Windows-Steuerelemente für MCM_GETCURSEL Meldung
topic_type:
- apiref
api_name:
- MCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dece95c65e900119c7043c0d5eda22bf473e6c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477556"
---
# <a name="mcm_getcursel-message"></a>MCM \_ getcurrsel-Meldung

Ruft das aktuell ausgewählte Datum ab. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getcurrsel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die die aktuell ausgewählten Datumsinformationen empfängt. Dieser Parameter muss eine gültige Adresse sein und darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL. Diese Meldung schlägt immer fehl, wenn Sie auf die Steuerelemente für Monatskalender angewendet wird, die auf den [**MCS- \_ MultiSelect**](month-calendar-control-styles.md) -Stil

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Uhrzeiten im Monatskalender-Steuerelement](month-calendar-controls.md)
</dt> </dl>

 

