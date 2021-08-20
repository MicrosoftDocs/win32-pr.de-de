---
title: SB_GETPARTS (Commctrl.h)
description: Ruft die Anzahl der Teile in einem Statusfenster ab. Die Meldung ruft auch die Koordinate des rechten Rands der angegebenen Anzahl von Teilen ab.
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- SB_GETPARTS meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- SB_GETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4318579b67adda9ab55a9dad4ad73949214758443c5e2151ce40cbb996fd90cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168756"
---
# <a name="sb_getparts-message"></a>SB \_ GETPARTS-Nachricht

Ruft die Anzahl der Teile in einem Statusfenster ab. Die Meldung ruft auch die Koordinate des rechten Rands der angegebenen Anzahl von Teilen ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anzahl der Teile, für die Koordinaten abgerufen werden. Wenn dieser Parameter größer als die Anzahl der Teile im Fenster ist, ruft die Meldung koordinaten nur für vorhandene Teile ab.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein ganzzahliges Array, das die gleiche Anzahl von Elementen wie die von *wParam angegebenen Teile aufgibt.* Jedes Element im Array empfängt die Clientkoordinate des rechten Rands des entsprechenden Teils. Wenn ein Element auf -1 festgelegt ist, erstreckt sich die Position des rechten Rands für diesen Teil bis zum rechten Rand des Fensters. Legen Sie diesen Parameter auf 0 fest, um die aktuelle Anzahl von Teilen abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Teile im Fenster zurück.

## <a name="remarks"></a>Hinweise

Diese Meldung gibt immer die Anzahl der Teile in der Statusleiste zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





