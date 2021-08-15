---
title: EM_GETOPTIONS Nachricht (Richedit.h)
description: Ruft Rich Edit-Steuerelementoptionen ab.
ms.assetid: 183f0fed-8666-4ed5-ac48-362c818378d2
keywords:
- EM_GETOPTIONS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cba85b5fe3ffd47763d25b9ca13bf10f6202a6876e25d300f66d9af3852edd5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019518"
---
# <a name="em_getoptions-message"></a>EM \_ GETOPTIONS-Nachricht

Ruft Rich Edit-Steuerelementoptionen ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt eine Kombination der aktuellen Optionsflagswerte zurück, die in der [**EM \_ SETOPTIONS-Nachricht**](em-setoptions.md) beschrieben sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ SETOPTIONS**](em-setoptions.md)
</dt> </dl>

 

 





