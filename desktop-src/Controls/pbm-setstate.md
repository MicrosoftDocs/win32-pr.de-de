---
title: PBM_SETSTATE Meldung (kommstrg. h)
description: Legt den Status der Statusanzeige fest.
ms.assetid: 4626f334-db74-4618-8fc7-e6f21c88ca19
keywords:
- Windows-Steuerelemente für PBM_SETSTATE Meldung
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
ms.openlocfilehash: 5c91e94bcc909957264eff776e56d3580b2c36ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477907"
---
# <a name="pbm_setstate-message"></a>PBM- \_ SetState-Nachricht

Legt den Status der Statusanzeige fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Status der Statusanzeige, die festgelegt wird. Einer der folgenden Werte.



| Wert                                                                                                                                                   | Bedeutung                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <dt>**PBST \_ Normal**</dt> </dl> | Läuft.<br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <dt>**PBST- \_ Fehler**</dt> </dl>    | Fehler.<br/>       |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <dt>**PBST \_ angehalten**</dt> </dl> | Angehalten.<br/>      |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den vorherigen Zustand zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





