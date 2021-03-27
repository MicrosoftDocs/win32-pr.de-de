---
description: Wird einmal an die CPlApplet-Funktion einer System Steuerungsanwendung gesendet, bevor die DLL mit der System Steuerungsanwendung freigegeben wird.
ms.assetid: 1afcb0d3-41a7-4fd8-9561-d96e1e8f0ddb
title: CPL_EXIT Meldung (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0adea6c4b05ee752829634f7478df2ac651e69f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214435"
---
# <a name="cpl_exit-message"></a>CPL-Beendigungs \_ Meldung

Wird einmal an die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion einer System Steuerungsanwendung gesendet, bevor die DLL mit der System Steuerungsanwendung freigegeben wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion diese Nachricht erfolgreich verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird gesendet, nachdem die letzte Nachricht zum [**\_ Anhalten der CPL**](cpl-stop.md) gesendet wurde.

Als Antwort auf diese Nachricht muss eine System Steuerungsanwendung jeglichen zugeordneten Arbeitsspeicher freigeben und Cleanup auf globaler Ebene durchführen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
