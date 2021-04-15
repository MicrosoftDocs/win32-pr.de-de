---
title: SB_GETPARTS Meldung (kommstrg. h)
description: Ruft die Anzahl der Teile in einem Statusfenster ab. Die Meldung ruft auch die Koordinate des rechten Rands der angegebenen Anzahl von Teilen ab.
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- Windows-Steuerelemente für SB_GETPARTS Meldung
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
ms.openlocfilehash: cee0f33331c579490cf66a38b9ce6655215ae673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518446"
---
# <a name="sb_getparts-message"></a>SB \_ GetParts-Nachricht

Ruft die Anzahl der Teile in einem Statusfenster ab. Die Meldung ruft auch die Koordinate des rechten Rands der angegebenen Anzahl von Teilen ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anzahl der Teile, für die Koordinaten abgerufen werden sollen. Wenn dieser Parameter größer als die Anzahl der Teile im Fenster ist, ruft die Nachricht nur die Koordinaten für vorhandene Teile ab.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein ganzzahliges Array, das über die gleiche Anzahl von Elementen wie von *wParam* angegebene Teile verfügt. Jedes Element im Array empfängt die Client Koordinate des rechten Rands des entsprechenden Teils. Wenn ein Element auf-1 festgelegt ist, wird die Position des rechten Rands für diesen Teil auf den rechten Rand des Fensters erweitert. Wenn Sie die aktuelle Anzahl von Teilen abrufen möchten, legen Sie diesen Parameter auf NULL fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Teile im Fenster zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung gibt immer die Anzahl der Teile in der Statusleiste zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





