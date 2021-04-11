---
title: MCM_SIZERECTTOMIN Meldung (kommstrg. h)
description: Berechnet, wie viele Kalender in das angegebene Rechteck passen, und gibt dann die Mindestgröße zurück, die ein Rechteck aufweisen muss, um dieser Anzahl von Kalendern gerecht zu werden. Sie können diese Nachricht explizit oder mit dem monthcal \_ sizerecttomin-Makro senden.
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- Windows-Steuerelemente für MCM_SIZERECTTOMIN Meldung
topic_type:
- apiref
api_name:
- MCM_SIZERECTTOMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f525f4cca9280b92fab0b9b86aa1d950ed990ef4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105981"
---
# <a name="mcm_sizerecttomin-message"></a>MCM \_ sizerecttomin-Meldung

Berechnet, wie viele Kalender in das angegebene Rechteck passen, und gibt dann die Mindestgröße zurück, die ein Rechteck aufweisen muss, um dieser Anzahl von Kalendern gerecht zu werden. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ sizerecttomin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält bei einem Eintrag einen Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die einen Bereich beschreibt, der größer oder gleich der Größe ist, die für die gewünschte Anzahl von Kalendern erforderlich ist. Wenn diese Funktion zurückgegeben wird, enthält Sie die minimale **Rect** -Struktur, die dieser Anzahl von Kalendern entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

