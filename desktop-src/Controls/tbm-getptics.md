---
title: TBM_GETPTICS (Commctrl.h)
description: Ruft die Adresse eines Arrays ab, das die Positionen der Teilstriche für eine Trackleiste enthält.
ms.assetid: d15a4b4d-2ced-40a4-9351-ed7ecc5a5751
keywords:
- TBM_GETPTICS meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TBM_GETPTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f67bc6f1e5f67f262559d1c63401f1c19f8680798beae92d8847d4908f7cbe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078074"
---
# <a name="tbm_getptics-message"></a>TBM \_ GETPTICS-Nachricht

Ruft die Adresse eines Arrays ab, das die Positionen der Teilstriche für eine Trackleiste enthält.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Adresse eines Arrays von **DWORD-Werten** zurück. Die Elemente des Arrays geben die logischen Positionen der Teilstriche der Trackleiste an, ohne die ersten und letzten Teilstriche, die von der Trackleiste erstellt wurden. Die logischen Positionen können beliebige ganzzahlige Werte im Bereich von minimalen bis maximalen Schiebereglerpositionen der Trackleiste sein.

## <a name="remarks"></a>Hinweise

Die Anzahl der Elemente im Array ist zwei kleiner als die Von der [**TBM \_ GETNUMTICS-Nachricht zurückgegebene Teilstrichanzahl.**](tbm-getnumtics.md) Beachten Sie, dass die Werte im Array möglicherweise doppelte Positionen enthalten und nicht sequenziell sind. Der zurückgegebene Zeiger ist gültig, bis Sie die Teilstriche der Trackleiste ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





