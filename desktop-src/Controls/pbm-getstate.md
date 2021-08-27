---
title: PBM_GETSTATE (Commctrl.h)
description: Ruft den Status der Statusleiste ab.
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- PBM_GETSTATE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- PBM_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cd157ccb6ab8a1fe4cd4a31bf1f8a033f0e591288338e21cc322a8ac10bfc41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047010"
---
# <a name="pbm_getstate-message"></a>PBM \_ GETSTATE-Nachricht

Ruft den Status der Statusleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den aktuellen Status der Statusleiste zurück. Einer der folgenden Werte.



| Rückgabecode                                                                                 | Beschreibung             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**PBST \_ NORMAL**</dt> </dl> | Läuft.<br/> |
| <dl> <dt>**\_PBST-FEHLER**</dt> </dl>  | Fehler.<br/>       |
| <dl> <dt>**PBST \_ PAUSED**</dt> </dl> | Angehalten.<br/>      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





