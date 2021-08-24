---
title: TB_HITTEST Meldung (Commctrl.h)
description: Bestimmt, wo sich ein Punkt in einem Symbolleistensteuerelement befindet.
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- TB_HITTEST Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d89cecf1d1df5c370ab9a00ae1251df9df7ef919f9959b998407a9fb5881178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696160"
---
# <a name="tb_hittest-message"></a>\_TB-HITTEST-Nachricht

Bestimmt, wo sich ein Punkt in einem Symbolleistensteuerelement befindet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf [](/previous-versions//dd162805(v=vs.85)) eine POINT-Struktur, die die x-Koordinate des Treffertests im **x-Member** und die y-Koordinate des Treffertests im **y-Element** enthält. Die Koordinaten sind relativ zum Clientbereich der Symbolleiste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Ganzzahlwert zurück. Wenn der Rückgabewert 0 (null) oder ein positiver Wert ist, handelt es sich um den nullbasierten Index des Nichtseparatorelements, in dem der Punkt liegt. Wenn der Rückgabewert negativ ist, liegt der Punkt nicht innerhalb einer Schaltfläche. Der absolute Wert des Rückgabewerts ist der Index eines Trennzeichenelements oder des nächsten Nichtseparatorelements.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

