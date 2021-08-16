---
title: TBM_GETTIC Meldung (Commctrl.h)
description: Ruft die logische Position eines Teilstrichs in einer Trackleiste ab. Die logische Position kann jeder der ganzzahligen Werte im Bereich der Trackleiste von minimalen bis maximalen Schiebereglerpositionen sein.
ms.assetid: 9d70c860-de97-4579-bb10-e9e9db7f1784
keywords:
- TBM_GETTIC Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 0b7cdd2c28f9add787c41da3cde3fabc3a5dff33812b3dd9c07a26a603d3a79e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829604"
---
# <a name="tbm_gettic-message"></a>TBM \_ GETTIC-Nachricht

Ruft die logische Position eines Teilstrichs in einer Trackleiste ab. Die logische Position kann jeder der ganzzahligen Werte im Bereich der Trackleiste von minimalen bis maximalen Schiebereglerpositionen sein.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index, der ein Teilstrich identifiziert. Gültige Indizes liegen im Bereich von 0 bis 2 kleiner als die Tickanzahl, die von der [**TBM \_ GETNUMTICS-Nachricht**](tbm-getnumtics.md) zurückgegeben wird.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die logische Position des angegebenen Teilstrichs oder -1 zurück, wenn *wParam* keinen gültigen Index angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





