---
title: PBM_GETSTATE Meldung (kommstrg. h)
description: Ruft den Status der Statusanzeige ab.
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- Windows-Steuerelemente für PBM_GETSTATE Meldung
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
ms.openlocfilehash: 07d4f7029fca46a046545efd1cea8e0eab99c757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956813"
---
# <a name="pbm_getstate-message"></a>PBM \_ GetState-Nachricht

Ruft den Status der Statusanzeige ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den aktuellen Status der Statusanzeige zurück. Einer der folgenden Werte.



| Rückgabecode                                                                                 | Beschreibung             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**PBST \_ Normal**</dt> </dl> | Läuft.<br/> |
| <dl> <dt>**PBST- \_ Fehler**</dt> </dl>  | Fehler.<br/>       |
| <dl> <dt>**PBST \_ angehalten**</dt> </dl> | Angehalten.<br/>      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





