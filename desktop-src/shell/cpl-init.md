---
description: Wird an die CPlApplet-Funktion einer System Steuerungsanwendung gesendet, um Sie zur Ausführung einer globalen Initialisierung aufzufordern, insbesondere für die Speicher Belegung.
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: CPL_INIT Meldung (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f5206d773a7a0b1786b8c95104bbcf71561d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977353"
---
# <a name="cpl_init-message"></a>CPL- \_ Init-Nachricht

Wird an die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion einer System Steuerungsanwendung gesendet, um Sie zur Ausführung einer globalen Initialisierung aufzufordern, insbesondere für die Speicher Belegung.


```C++

                CPlApplet(

    hwndCPl,

    CPL_INIT,

    wParam,  // = 0; not used, must be zero

    lParam   // = 0; not used, must be zero 

);

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Initialisierung erfolgreich ist, sollte die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion ungleich 0 (null) zurückgeben. Andernfalls sollte NULL zurückgegeben werden.

Wenn [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) NULL zurückgibt, beendet die steuernde Anwendung die Kommunikation und gibt die dll frei, die die System Steuerungsanwendung enthält.

## <a name="remarks"></a>Bemerkungen

Da dies die einzige Möglichkeit ist, dass eine System Steuerungsanwendung einen Fehlerzustand signalisieren kann, sollte die Anwendung Arbeitsspeicher als Reaktion auf diese Nachricht zuweisen.

Diese Nachricht wird unmittelbar nach dem Laden der dll, die die Anwendung enthält, gesendet.

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

 

 
