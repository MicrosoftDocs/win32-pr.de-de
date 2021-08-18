---
title: RAS_PORT_1-Struktur (Rassapi.h)
description: Die RAS \_ PORT \_ 1-Struktur enthält Informationen zu einem RAS-Port.
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- RAS_PORT_1 Struktur von RAS
- PRAS_PORT_1 Strukturzeiger RAS
topic_type:
- apiref
api_name:
- RAS_PORT_1
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c73677b10743434bb9548c8d6add95100c4cf017d25bb44d7436e2f68b9ca4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673110"
---
# <a name="ras_port_1-structure"></a>RAS \_ PORT \_ 1-Struktur

\[Diese Version der **RAS \_ PORT \_ 1-Struktur** wird ab Windows Vista nicht unterstützt. Verwenden Sie stattdessen den neueren [**\_ RAS-PORT \_ 1,**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) der in mprapi.h definiert ist.\]

Die **RAS \_ PORT \_ 1-Struktur** enthält Informationen zu einem RAS-Port.

## <a name="syntax"></a>Syntax


```C++
typedef struct _RAS_PORT_1 {
  RAS_PORT_0                rasport0;
  DWORD                     LineCondition;
  DWORD                     HardwareCondition;
  DWORD                     LineSpeed;
  WORD                      NumStatistics;
  WORD                      NumMediaParms;
  DWORD                     SizeMediaParms;
  RAS_PPP_PROJECTION_RESULT ProjResult;
} RAS_PORT_1, *PRAS_PORT_1;
```



## <a name="members"></a>Member

<dl> <dt>

**rasport0**
</dt> <dd>

Gibt eine [**RAS \_ PORT \_ 0-Struktur**](ras-port-0-str.md) an, die Informationen zum Port enthält, z. B. den Namen des Ports, den Namen des Remotebenutzers, der mit dem Port verbunden ist usw.

</dd> <dt>

**LineCondition**
</dt> <dd>

Gibt den Zustand des Ports an. Dieser Member kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                            | Bedeutung                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <dt>**\_RAS-PORT \_ NICHT \_ BETRIEBSBEREIT**</dt> </dl> | Der Port ist nicht betriebsbereit. Überprüfen Sie das Ereignisprotokoll auf Fehler, die vom Server gemeldet werden.<br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <dt>**\_RAS-PORT \_ GETRENNT**</dt> </dl>           | Der Port ist derzeit getrennt.<br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <dt>**\_RAS-PORT: \_ \_ RÜCKRUF**</dt> </dl>          | Der RAS-Server ruft den RAS-Client zurück.<br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <dt>**\_ \_ RAS-PORT LAUSCHEN**</dt> </dl>                    | Der Port wartet darauf, dass ein Client aufruft.<br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <dt>**\_ \_ RAS-PORTAUTHENTIFIZIERUNG**</dt> </dl>     | Der Server authentifiziert den Remoteclient gerade.<br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <dt>**\_RAS-PORT \_ AUTHENTIFIZIERT**</dt> </dl>        | Der Remoteclient ist jetzt authentifiziert.<br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <dt>**\_INITIALISIERUNG DES RAS-PORTS \_**</dt> </dl>           | Das an den Port angefügte Gerät wird initialisiert. Der Zustand des Ports ändert sich in RAS \_ PORT \_ LISTENING, wenn die Initialisierung abgeschlossen wurde.<br/> |



 

</dd> <dt>

**HardwareCondition**
</dt> <dd>

Gibt einen der folgenden Werte an, um den Zustand des Geräts anzugeben, das an den Port angeschlossen ist.



| Wert                                                                                                                                                                                                  | Bedeutung                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <dt>**\_RAS-MODEM \_ BETRIEBSBEREIT**</dt> </dl>                 | Das an diesen Port angeschlossene Modem ist betriebsbereit und kann Clientaufrufe empfangen.<br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <dt>**\_ \_ RAS-MODEM-HARDWAREFEHLER \_**</dt> </dl> | Das an diesen Port angeschlossene Modem weist ein Hardwareproblem auf.<br/>                              |



 

</dd> <dt>

**LineSpeed**
</dt> <dd>

Gibt die Geschwindigkeit in Bits pro Sekunde an, mit der der Computer mit dem Port kommunizieren kann.

</dd> <dt>

**NumStatistics**
</dt> <dd>

Dieser Member wird nicht verwendet. Die RAS-Verwaltungsfunktionen, z. B. die [**RasAdminPortGetInfo-Funktion,**](rasadminportgetinfo.md) verwenden die [**RAS PORT \_ \_ STATISTICS-Struktur,**](ras-port-statistics-str.md) um Portstatistiken zurückzugeben.

</dd> <dt>

**NumMediaParms**
</dt> <dd>

Gibt die Anzahl der medienspezifischen Parameter für diesen Port an. Bei seriellen Medien ist dies in der Regel die Anzahl der Werte, die in der datei SERIAL.INI angezeigt werden.

</dd> <dt>

**SizeMediaParms**
</dt> <dd>

Gibt die Größe des Puffers in Bytes an, der für alle medienspezifischen Parameter erforderlich ist. Die [**RasAdminPortGetInfo-Funktion**](rasadminportgetinfo.md) gibt einen Puffer zurück, der ein Array von [**RAS \_ PARAMETERS-Strukturen**](ras-parameters-str.md) mit den Medienparametern und -werten für den Port enthält.

</dd> <dt>

**ProjResult**
</dt> <dd>

Eine [**\_ RAS-PROJEKTIONSPROJEKTIONSERGEBNIS-Struktur, \_ \_**](ras-ppp-projection-result-str.md) die die INFORMATIONEN ZUR PROJEKTION FÜR DIESEN Port angibt. Diese Struktur stellt Informationen für jedes Protokoll bereit, das ausgehandelt wird, wenn ein RAS-Client eine Verbindung mit einem Server herstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Remotezugriffsdienst (RAS) – Übersicht](about-remote-access-service.md)
</dt> <dt>

[RAS-Serververwaltungsstrukturen](ras-server-administration-structures.md)
</dt> <dt>

[**\_RAS-PARAMETER**](ras-parameters-str.md)
</dt> <dt>

[**\_RAS-PORT \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**\_ \_ RAS-PORTSTATISTIKEN**](ras-port-statistics-str.md)
</dt> <dt>

[**\_ \_ RAS-PROJEKTIONSERGEBNIS \_**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





