---
title: TBM_GETTIC Meldung (kommstrg. h)
description: Ruft die logische Position eines Teil Strichs in einer TrackBar ab. Die logische Position kann ein beliebiger ganzzahliger Wert im Bereich der TrackBar sein, der den minimalen und maximalen Schieberegler-Positionen entspricht.
ms.assetid: 9d70c860-de97-4579-bb10-e9e9db7f1784
keywords:
- Windows-Steuerelemente für TBM_GETTIC Meldung
topic_type:
- apiref
api_name:
- TBM_GETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d534d5100e20cc544c31fca2fc9e49cda3bd976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476797"
---
# <a name="tbm_gettic-message"></a>TBM- \_ GetTic-Nachricht

Ruft die logische Position eines Teil Strichs in einer TrackBar ab. Die logische Position kann ein beliebiger ganzzahliger Wert im Bereich der TrackBar sein, der den minimalen und maximalen Schieberegler-Positionen entspricht.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

NULL basierter Index, der einen Teil Strich identifiziert. Gültige Indizes liegen im Bereich von 0 bis zwei kleiner als der von der [**TBM \_ GetNumTics**](tbm-getnumtics.md) -Nachricht zurückgegebene Tick-Zähler.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die logische Position des angegebenen Teil Strichs oder-1 zurück, wenn *wParam* keinen gültigen Index angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





