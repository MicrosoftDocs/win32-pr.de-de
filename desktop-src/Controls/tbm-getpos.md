---
title: TBM_GETPOS Meldung (Commctrl.h)
description: Ruft die aktuelle logische Position des Schiebereglers in einer Trackleiste ab. Die logischen Positionen sind die ganzzahligen Werte im Bereich der Trackleiste von minimalen bis maximalen Schiebereglerpositionen.
ms.assetid: 6f082ab2-2f9a-4bc0-bfca-56f7b1a2d921
keywords:
- TBM_GETPOS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TBM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54ed3b8afed7b96e657984a437ff54b1099f196b8dc3d0035468835152b5a841
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078084"
---
# <a name="tbm_getpos-message"></a>TBM \_ GETPOS-Nachricht

Ruft die aktuelle logische Position des Schiebereglers in einer Trackleiste ab. Die logischen Positionen sind die ganzzahligen Werte im Bereich der Trackleiste von minimalen bis maximalen Schiebereglerpositionen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen 32-Bit-Wert zurück, der die aktuelle logische Position des Schiebereglers der Trackleiste angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TBM \_ SETPOS**](tbm-setpos.md)
</dt> </dl>

 

 





