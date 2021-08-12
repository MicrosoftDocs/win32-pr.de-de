---
title: TB_COMMANDTOINDEX (Commctrl.h)
description: Ruft den nullbasierten Index für die Schaltfläche ab, die dem angegebenen Befehlsbezeichner zugeordnet ist.
ms.assetid: vs|controls|~\controls\toolbar\messages\tb_commandtoindex.htm
keywords:
- TB_COMMANDTOINDEX von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TB_COMMANDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea21f7436745ff3b6a8d69df4c2be43e59fc82e8e4e934302cddb71c9d342e43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670393"
---
# <a name="tb_commandtoindex-message"></a>TB \_ COMMANDTOINDEX-Meldung

Ruft den nullbasierten Index für die Schaltfläche ab, die dem angegebenen Befehlsbezeichner zugeordnet ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Befehlsbezeichner, der der Schaltfläche zugeordnet ist.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den nullbasierten Index für die Schaltfläche oder -1 zurück, wenn der angegebene Befehlsbezeichner ungültig ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





