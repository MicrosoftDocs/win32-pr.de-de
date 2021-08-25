---
title: DTM_GETRANGE (Commctrl.h)
description: Ruft die aktuellen minimalen und maximalen zulässigen Systemzeiten für ein Datums- und Uhrzeitauswahl-Steuerelement (DTP) ab. Sie können diese Nachricht explizit senden oder das DateTime \_ GetRange-Makro verwenden.
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- DTM_GETRANGE von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- DTM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9c0c90780e4bcd35da2d410f7b4743547cbd8d31ac06293c411f2415e4e408
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877950"
---
# <a name="dtm_getrange-message"></a>SMS \_ GETRANGE-Nachricht

Ruft die aktuellen minimalen und maximalen zulässigen Systemzeiten für ein Datums- und Uhrzeitauswahl-Steuerelement (DTP) ab. Sie können diese Nachricht explizit senden oder das [**DateTime \_ GetRange-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf ein Zwei-Element-Array von [**SYSTEMTIME-Strukturen.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD-Wert** zurück, der eine Kombination aus GDTR \_ MIN oder GDTR \_ MAX ist. Das erste Element des [**SYSTEMTIME-Arrays**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) enthält die minimal zulässige Zeit, wenn GDTR \_ MIN festgelegt ist. Das zweite Element des **SYSTEMTIME-Arrays** enthält die maximal zulässige Zeit, wenn GDTR \_ MAX festgelegt ist.

## <a name="remarks"></a>Hinweise

Die Datums- und Uhrzeitauswahl zeigt nur Datums- und Uhrzeitangaben an, die innerhalb des angegebenen Bereichs liegen, was den Benutzer daran hindert, ein Datum und eine Uhrzeit auszuwählen, die außerhalb des Bereichs liegen. Wenn die [**MELDUNG \_ SETSYSTEMTIME des SYSTEMS**](dtm-setsystemtime.md) ein Datum und eine Uhrzeit angibt, die außerhalb des Bereichs liegen, wird ein Fehler angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

