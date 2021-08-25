---
title: PBM_SETSTEP Meldung (Commctrl.h)
description: Gibt das Schrittinkrement für eine Statusanzeige an. Das Schrittinkrement ist der Betrag, um den die Statusanzeige ihre aktuelle Position erhöht, wenn sie eine PBM \_ STEPIT-Nachricht empfängt. Standardmäßig ist das Schrittinkrement auf 10 festgelegt.
ms.assetid: 75c1085b-6c7a-4c44-9a12-f9bf21f7d945
keywords:
- PBM_SETSTEP Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- PBM_SETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88508654565cb3af05dd768ef7ef1e54e5ef0ee80e0797bc45631f6e3fe6912
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798770"
---
# <a name="pbm_setstep-message"></a>PBM \_ SETSTEP-Meldung

Gibt das Schrittinkrement für eine Statusanzeige an. Das Schrittinkrement ist der Betrag, um den die Statusanzeige ihre aktuelle Position erhöht, wenn sie eine [**PBM \_ STEPIT-Nachricht**](pbm-stepit.md) empfängt. Standardmäßig ist das Schrittinkrement auf 10 festgelegt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Neuer Schrittinkrement.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das vorherige Schrittinkrement zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





