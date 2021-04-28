---
title: TBM_SETPOS (Commctrl.h)
description: 'TBM_SETPOS Meldung: Legt die aktuelle logische Position des Schiebereglers in einer Trackleiste fest.'
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- TBM_SETPOS Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f10e05a677119f18489d0eb9eebc4528d3ad115
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085868"
---
# <a name="tbm_setpos-message"></a>TBM \_ SETPOS-Nachricht

Legt die aktuelle logische Position des Schiebereglers in einer Trackleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag neu gezeichnet. Wenn dieser Parameter **TRUE ist,** wird das Steuerelement mit dem Schieberegler an der von lParam angegebenen *Position neu gedraht.* Wenn dieser Parameter **FALSE ist,** wird der Schieberegler in der Meldung nicht an der neuen Position neu gezeichnet. Beachten Sie, dass die Meldung den Wert der Position des Schiebereglers (wie von der [**TBM \_ GETPOS-Nachricht**](tbm-getpos.md) zurückgegeben) unabhängig vom *wParam-Parameter* festgibt.

</dd> <dt>

*lParam* 
</dt> <dd>

Neue logische Position des Schiebereglers. Gültige logische Positionen sind die ganzzahligen Werte im Bereich von minimalen bis maximalen Schiebereglerpositionen der Trackleiste. Wenn dieser Wert außerhalb des maximalen und minimalen Bereichs des Steuerelements liegt, wird die Position auf den höchst- oder minimalen Wert festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





