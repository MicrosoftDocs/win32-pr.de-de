---
description: Wird an die CPlApplet-Funktion einer Systemsteuerung gesendet, um sie zur Durchführung der globalen Initialisierung zu auffordern, insbesondere zur Speicherzuweisung.
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: CPL_INIT (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be6acdf58822e6f10f35880a97a7b5bbb9ce0b7bbbf7556b4c18c3f7ad96f72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456370"
---
# <a name="cpl_init-message"></a>CPL \_ INIT-Nachricht

Wird an die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) einer Systemsteuerung- gesendet, um sie zur Durchführung der globalen Initialisierung zu auffordern, insbesondere der Speicherzuweisung.


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

Wenn die Initialisierung erfolgreich ist, sollte die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) ungleich 0 (null) zurückgeben. Andernfalls sollte 0 (null) zurückgeben werden.

Wenn [**CPlApplet 0**](/windows/win32/api/cpl/nc-cpl-applet_proc) (null) zurückgibt, beendet die steuernde Anwendung die Kommunikation und gibt die DLL frei, die die Systemsteuerung enthält.

## <a name="remarks"></a>Hinweise

Da dies die einzige Möglichkeit ist, Systemsteuerung Anwendung einen Fehlerzustand signalisieren kann, sollte die Anwendung als Reaktion auf diese Meldung Speicher zuweisen.

Diese Meldung wird unmittelbar nach dem Laden der DLL mit der Anwendung gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
