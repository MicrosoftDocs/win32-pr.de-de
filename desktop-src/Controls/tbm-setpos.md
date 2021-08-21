---
title: TBM_SETPOS Nachricht (Commctrl.h)
description: 'TBM_SETPOS Meldung: Legt die aktuelle logische Position des Schiebereglers in einer Trackleiste fest.'
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- TBM_SETPOS Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 3ccd1cb35f8cde672c51baafe5623291e5449f90aa118eb36cb12152fe155385
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078044"
---
# <a name="tbm_setpos-message"></a>TBM \_ SETPOS-Nachricht

Legt die aktuelle logische Position des Schiebereglers in einer Trackleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Neu gezeichnetes Flag. Wenn dieser Parameter **TRUE** ist, zeichnet die Meldung das Steuerelement mit dem Schieberegler an der von *lParam* angegebenen Position neu. Wenn dieser Parameter **FALSE** ist, zeichnet die Nachricht den Schieberegler nicht an der neuen Position neu. Beachten Sie, dass die Nachricht den Wert der Schiebereglerposition (wie von der [**TBM \_ GETPOS-Nachricht**](tbm-getpos.md) zurückgegeben) unabhängig vom *wParam-Parameter* festlegt.

</dd> <dt>

*lParam* 
</dt> <dd>

Neue logische Position des Schiebereglers. Gültige logische Positionen sind die ganzzahligen Werte im Bereich der Trackleiste von minimalen bis maximalen Schiebereglerpositionen. Wenn sich dieser Wert außerhalb des maximalen und minimalen Bereichs des Steuerelements befindet, wird die Position auf den Maximal- oder Mindestwert festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





