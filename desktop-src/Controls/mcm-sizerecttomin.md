---
title: MCM_SIZERECTTOMIN Meldung (Commctrl.h)
description: Berechnet, wie viele Kalender in das angegebene Rechteck passen, und gibt dann die Mindestgröße zurück, die ein Rechteck für diese Anzahl von Kalendern benötigt. Sie können diese Nachricht explizit oder mithilfe des Makros MonthCal \_ SizeRectToMin senden.
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- MCM_SIZERECTTOMIN Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 547b8e401f270cbca1ff666ba0f1eb263ab3f9245f8a51e6874a7627597b9bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799230"
---
# <a name="mcm_sizerecttomin-message"></a>MCM \_ SIZERECTTOMIN-Nachricht

Berechnet, wie viele Kalender in das angegebene Rechteck passen, und gibt dann die Mindestgröße zurück, die ein Rechteck für diese Anzahl von Kalendern benötigt. Sie können diese Nachricht explizit oder mithilfe des [**Makros MonthCal \_ SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält beim Eintrag einen Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die einen Bereich beschreibt, der größer oder gleich der Größe ist, die für die gewünschte Anzahl von Kalendern erforderlich ist. Enthält nach der Rückgabe dieser Funktion die minimale RECT-Struktur, die dieser Anzahl von Kalendern **entspricht.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

