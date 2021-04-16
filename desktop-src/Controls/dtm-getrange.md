---
title: DTM_GETRANGE Meldung (kommstrg. h)
description: Ruft die aktuellen minimal-und maximal zulässigen Systemzeiten für ein DTP-Steuerelement (Datums-und Zeitauswahl) ab. Sie können diese Nachricht explizit senden oder das DateTime- \_ GetRange-Makro verwenden.
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- Windows-Steuerelemente für DTM_GETRANGE Meldung
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
ms.openlocfilehash: a50a2ae9fe4ca77198f9e63548f709e0f571fdb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477934"
---
# <a name="dtm_getrange-message"></a>DTM- \_ GetRange-Nachricht

Ruft die aktuellen minimal-und maximal zulässigen Systemzeiten für ein DTP-Steuerelement (Datums-und Zeitauswahl) ab. Sie können diese Nachricht explizit senden oder das [**DateTime- \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf ein zwei-Element-Array von [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Strukturen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD** -Wert zurück, der eine Kombination aus dstr \_ Min oder dstr \_ Max ist. Das erste Element des [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Arrays enthält die zulässige Mindestzeit, wenn dstr \_ Min festgelegt ist. Das zweite Element des **SYSTEMTIME** -Arrays enthält die maximal zulässige Zeit, wenn dstr \_ Max festgelegt ist.

## <a name="remarks"></a>Bemerkungen

Die Datums-und Uhrzeit Auswahl zeigt nur Datumsangaben/Uhrzeiten an, die innerhalb des angegebenen Bereichs liegen, sodass der Benutzer kein Datum und keine Uhrzeit auswählen kann, die außerhalb des Bereichs liegt. Wenn die [**DTM- \_ SetSystemTime**](dtm-setsystemtime.md) -Nachricht ein Datum und eine Uhrzeit angibt, die außerhalb des Bereichs liegen, tritt ein Fehler auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

