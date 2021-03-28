---
description: Wird an die CPlApplet-Funktion einer System Steuerungsanwendung gesendet, um die von der Anwendung unterstützte Anzahl von Dialogfeldern abzurufen.
title: CPL_GETCOUNT Meldung (cpl. h)
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
ms.openlocfilehash: 3bf8980fa29841d3c5341daeeccf26cea05db80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525391"
---
# <a name="cpl_getcount-message"></a>CPL- \_ GetCount-Nachricht

Wird an die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion einer System Steuerungsanwendung gesendet, um die von der Anwendung unterstützte Anzahl von Dialogfeldern abzurufen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion gibt die Anzahl der Dialogfelder zurück, die von der System Steuerungsanwendung unterstützt werden.

## <a name="remarks"></a>Bemerkungen

Diese Nachricht wird unmittelbar nach der [**cpl- \_ Init**](cpl-init.md) -Nachricht gesendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



 

 
