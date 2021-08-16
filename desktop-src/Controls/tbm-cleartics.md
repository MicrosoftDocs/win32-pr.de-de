---
title: TBM_CLEARTICS Meldung (Commctrl.h)
description: Entfernt die aktuellen Teilstriche aus einer Trackleiste. Diese Meldung entfernt nicht die ersten und letzten Teilstriche, die automatisch von der Trackleiste erstellt werden.
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- TBM_CLEARTICS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TBM_CLEARTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9390fc45c5b96a7b85d3b1b366e34d24c3b4bf0bc60ec066ead28357bcec1439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046770"
---
# <a name="tbm_cleartics-message"></a>TBM \_ CLEARTICS-Meldung

Entfernt die aktuellen Teilstriche aus einer Trackleiste. Diese Meldung entfernt nicht die ersten und letzten Teilstriche, die automatisch von der Trackleiste erstellt werden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Neu gezeichnetes Flag. Wenn dieser Parameter **TRUE** ist, wird die Trackleiste neu gezeichnet, nachdem die Teilstriche gelöscht wurden. Wenn dieser Parameter **FALSE** ist, löscht die Nachricht die Teilstriche, zeichnet die Trackleiste jedoch nicht neu.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





