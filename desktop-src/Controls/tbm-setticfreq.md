---
title: TBM_SETTICFREQ Nachricht (Commctrl.h)
description: Legt die Intervallhäufigkeit für Teilstriche in einer Trackleiste fest.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- TBM_SETTICFREQ Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TBM_SETTICFREQ
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c1b3e029abc8027d8708da31698f44db85ec78e427ba9461f0a71a740fb05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078014"
---
# <a name="tbm_setticfreq-message"></a>TBM \_ SETTICFREQ-Nachricht

Legt die Intervallhäufigkeit für Teilstriche in einer Trackleiste fest. Wenn die Häufigkeit beispielsweise auf zwei festgelegt ist, wird für jedes andere Inkrement im Bereich der Trackleiste ein Teilstrich angezeigt. Die Standardeinstellung für die Häufigkeit ist 1. Das heißt, jedes Inkrement im Bereich ist einem Teilstrich zugeordnet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Häufigkeit der Teilstriche.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die Trackleiste muss das [**TBS \_ AUTOTICKS-Format**](trackbar-control-styles.md) aufweisen, um diese Meldung verwenden zu können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





