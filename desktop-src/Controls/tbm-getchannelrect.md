---
title: TBM_GETCHANNELRECT Meldung (kommstrg. h)
description: Ruft die Größe und Position des umgebenden Rechtecks für den Kanal einer TrackBar ab.
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- Windows-Steuerelemente für TBM_GETCHANNELRECT Meldung
topic_type:
- apiref
api_name:
- TBM_GETCHANNELRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02982e9ce417b9fcf3e16d0e14d061e3ffd97a8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949592"
---
# <a name="tbm_getchannelrect-message"></a>TBM- \_ GetChannelRect-Nachricht

Ruft die Größe und Position des umgebenden Rechtecks für den Kanal einer TrackBar ab. (Der Kanal ist der Bereich, in dem der Schieberegler verschoben wird. Sie enthält die Hervorhebung, wenn ein Bereich ausgewählt ist.)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur. Die Meldung füllt diese Struktur mit dem umgebenden Rechteck des Kanals in den Client Koordinaten des TrackBar-Fensters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

