---
title: DTM_GETSYSTEMTIME Meldung (kommstrg. h)
description: Ruft den aktuell ausgewählten Zeitpunkt von einem DTP-Steuerelement (Date and Time Picker) ab und platziert ihn in einer angegebenen SYSTEMTIME-Struktur. Sie können diese Nachricht explizit senden oder das DateTime- \_ GetSystemTime-Makro verwenden.
ms.assetid: 81c95187-109c-4b36-98ea-a2e77ce42d9a
keywords:
- Windows-Steuerelemente für DTM_GETSYSTEMTIME Meldung
topic_type:
- apiref
api_name:
- DTM_GETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e14d8c998720cc987a03877e1918e97304bf769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104841"
---
# <a name="dtm_getsystemtime-message"></a>DTM \_ GetSystemTime-Nachricht

Ruft den aktuell ausgewählten Zeitpunkt von einem DTP-Steuerelement (Date and Time Picker) ab und platziert ihn in einer angegebenen [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur. Sie können diese Nachricht explizit senden oder das [**DateTime- \_ GetSystemTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur. Wenn bei **DTM \_ GetSystemTime** GDT \_ gültig zurückgegeben wird, enthält diese Struktur den aktuell ausgewählten Zeitpunkt. Andernfalls enthält Sie keine gültigen Informationen. Dieser Parameter muss ein gültiger Zeiger sein. Er darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt GDT \_ gültig zurück, wenn die Zeit Informationen erfolgreich in *LPARAM* platziert wurden. Gibt GDT \_ None zurück, wenn das Steuerelement auf das [**DTS \_ shownone-Format**](date-and-time-picker-control-styles.md) festgelegt wurde und das Kontrollkästchen für das Steuerelement nicht aktiviert war. Gibt GDT-Fehler zurück, \_ Wenn ein Fehler auftritt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

