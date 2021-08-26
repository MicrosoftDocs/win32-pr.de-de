---
title: PBM_SETSTATE Meldung (Commctrl.h)
description: Legt den Status der Statusanzeige fest.
ms.assetid: 4626f334-db74-4618-8fc7-e6f21c88ca19
keywords:
- PBM_SETSTATE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- PBM_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794006517eaa23789f3a25425b1213fede7f8dde9893587def02ebc9605b28f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986060"
---
# <a name="pbm_setstate-message"></a>PBM \_ SETSTATE-Nachricht

Legt den Status der Statusanzeige fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Status der Statusanzeige, die festgelegt wird. Einer der folgenden Werte.



| Wert                                                                                                                                                   | Bedeutung                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <dt>**PBST \_ NORMAL**</dt> </dl> | Läuft.<br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <dt>**\_PBST-FEHLER**</dt> </dl>    | Fehler.<br/>       |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <dt>**PBST \_ ANGEHALTEN**</dt> </dl> | Angehalten.<br/>      |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den vorherigen Zustand zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





