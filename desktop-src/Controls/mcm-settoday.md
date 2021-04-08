---
title: MCM_SETTODAY Meldung (kommstrg. h)
description: Legt den \ 0034; heute \ 0034; fest. Auswahl für ein Monatskalender-Steuerelement. Sie können diese Nachricht explizit oder mit dem monthcal- \_ settoday-Makro senden.
ms.assetid: fcd4d33d-e661-4e02-8d19-666d80e1a070
keywords:
- Windows-Steuerelemente für MCM_SETTODAY Meldung
topic_type:
- apiref
api_name:
- MCM_SETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b725e5f61e3c08170a323b063616434acb857e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743816"
---
# <a name="mcm_settoday-message"></a>MCM \_ settoday-Meldung

Legt die Auswahl "heute" für ein Monatskalender-Steuerelement fest. Sie können diese Nachricht explizit oder mit dem [**monthcal- \_ settoday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die das Datum enthält, das als "heutige" Auswahl für das Steuerelement festgelegt werden soll. Wenn dieser Parameter auf **null** festgelegt ist, wird das Steuerelement zur Standardeinstellung zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Wenn die Auswahl "heute" auf ein anderes Datum als die Standardeinstellung festgelegt ist, gelten die folgenden Bedingungen:

-   Das Steuerelement aktualisiert die "heute"-Auswahl nicht automatisch, wenn die Zeit für den aktuellen Tag Mitternacht überschritten wird.
-   Das-Steuerelement aktualisiert seine Anzeige nicht automatisch basierend auf Gebiets Schema Änderungen.

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

 

