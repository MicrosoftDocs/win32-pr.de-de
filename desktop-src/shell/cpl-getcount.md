---
description: Wird an die CPlApplet-Funktion einer Systemsteuerung Anwendung gesendet, um die Anzahl der von der Anwendung unterstützten Dialogfelder abzurufen.
title: CPL_GETCOUNT-Nachricht (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6b88b56c-aad7-4144-ab95-15d7eef21861
api_name:
- CPL_GETCOUNT
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58f95a62d17ccafd308666a5632a1f7a42ebfda6ca0a54dfb6dfa9d9eda9b684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715480"
---
# <a name="cpl_getcount-message"></a>CPL \_ GETCOUNT-Nachricht

Wird an die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) einer Systemsteuerung Anwendung gesendet, um die Anzahl der von der Anwendung unterstützten Dialogfelder abzurufen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) gibt die Anzahl der Dialogfelder zurück, die die Systemsteuerung Anwendung unterstützt.

## <a name="remarks"></a>Hinweise

Diese Nachricht wird unmittelbar nach der [**\_ CPL-INIT-Nachricht**](cpl-init.md) gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



 

 
