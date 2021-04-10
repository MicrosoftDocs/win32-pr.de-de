---
title: TBM_GETTHUMBRECT Meldung (kommstrg. h)
description: Ruft die Größe und Position des umgebenden Rechtecks für den Schieberegler in einer TrackBar ab.
ms.assetid: f53fd7af-36f8-4490-aa95-f1fa20f34efb
keywords:
- Windows-Steuerelemente für TBM_GETTHUMBRECT Meldung
topic_type:
- apiref
api_name:
- TBM_GETTHUMBRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce1bba8af9a65f297aa0515c1103c50daa1626d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040631"
---
# <a name="tbm_getthumbrect-message"></a>TBM- \_ getthumbrect-Nachricht

Ruft die Größe und Position des umgebenden Rechtecks für den Schieberegler in einer TrackBar ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur. Die Meldung füllt diese-Struktur mit dem umgebenden Rechteck des Schiebe leisten-Schiebereglers in Client Koordinaten des TrackBar-Fensters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

