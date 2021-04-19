---
title: RAS_PORT_1 Struktur (rassapi. h)
description: Die Struktur des RAS- \_ Ports \_ 1 enthält Informationen zu einem RAS-Port.
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- RAS_PORT_1 Struktur-RAS
- PRAS_PORT_1-Struktur Zeiger RAS
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
ms.openlocfilehash: d73fe450e5ea5f8ceee48436dbbe05570d0d818a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346721"
---
# <a name="ras_port_1-structure"></a>RAS- \_ Port \_ 1-Struktur

\[Diese Version der RAS-Struktur von **\_ Port \_ 1** wird ab Windows Vista nicht unterstützt. Verwenden Sie stattdessen den neueren [**RAS- \_ Port \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) , der in MPRAPI. h definiert ist.\]

Die Struktur des **RAS- \_ Ports \_ 1** enthält Informationen zu einem RAS-Port.

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

Gibt eine [**RAS- \_ Port \_ 0**](ras-port-0-str.md) -Struktur an, die Informationen über den Port enthält, z. b. den Namen des Ports, den Namen des Remote Benutzers, der mit dem Port verbunden ist, usw.

</dd> <dt>

**Linecondition**
</dt> <dd>

Gibt den Status des Ports an. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                            | Bedeutung                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <dt>**RAS- \_ Port \_ nicht \_ betriebsbereit**</dt> </dl> | Der Port ist nicht funktionstüchtig. Überprüfen Sie das Ereignisprotokoll auf Fehler, die vom Server gemeldet wurden.<br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <dt>**RAS- \_ Port \_ getrennt**</dt> </dl>           | Der Port ist derzeit nicht getrennt.<br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <dt>**RAS \_ - \_ Port \_ Rückruf**</dt> </dl>          | Der RAS-Server Ruft den RAS-Client zurück.<br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <dt>**RAS- \_ Port Überwachung \_**</dt> </dl>                    | Der Port wartet darauf, dass ein Client in aufruft.<br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <dt>**RAS- \_ Port \_ Authentifizierung**</dt> </dl>     | Der Server authentifiziert den Remote Client.<br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <dt>**RAS- \_ Port \_ authentifiziert**</dt> </dl>        | Der Remote Client ist jetzt authentifiziert.<br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <dt>**RAS- \_ Port \_ Initialisierung**</dt> </dl>           | Das an den Port angefügte Gerät wird initialisiert. \_ \_ Wenn die Initialisierung abgeschlossen ist, ändert sich der Status des Ports in den RAS-Port.<br/> |



 

</dd> <dt>

**Hardwarecondition**
</dt> <dd>

Gibt einen der folgenden Werte an, um den Status des Geräts anzugeben, das mit dem Port verbunden ist.



| Wert                                                                                                                                                                                                  | Bedeutung                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <dt>**RAS- \_ Modem \_ betriebsbereit**</dt> </dl>                 | Das an diesen Port angefügte Modem ist funktionstüchtig und bereit zum Empfangen von Client aufrufen.<br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <dt>**\_ \_ Hardware \_ Fehler des RAS-Modem**</dt> </dl> | Das an diesen Port angefügte Modem hat ein Hardwareproblem.<br/>                              |



 

</dd> <dt>

**Linespeed**
</dt> <dd>

Gibt die Geschwindigkeit in Bits pro Sekunde an, mit der der Computer mit dem Port kommunizieren kann.

</dd> <dt>

**Numstatistics**
</dt> <dd>

Dieser Member wird nicht verwendet. Die RAS-Verwaltungsfunktionen, wie z. b. die [**rasadminportgetinfo**](rasadminportgetinfo.md) -Funktion, verwenden die Struktur der [**RAS- \_ Port \_ Statistik**](ras-port-statistics-str.md) , um Port Statistiken zurückzugeben.

</dd> <dt>

**Nummediaparms**
</dt> <dd>

Gibt die Anzahl der medienspezifischen Parameter für diesen Port an. Bei seriellen Medien ist dies in der Regel die Anzahl der Werte, die in der SERIAL.INI-Datei angezeigt werden.

</dd> <dt>

**Sizemediaparms**
</dt> <dd>

Gibt die Größe (in Bytes) des Puffers an, der für alle medienspezifischen Parameter benötigt wird. Die [**rasadminportgetinfo**](rasadminportgetinfo.md) -Funktion gibt einen Puffer zurück, der ein Array von [**RAS- \_ Parameter**](ras-parameters-str.md) Strukturen mit den Medien Parametern und-Werten für den Port enthält.

</dd> <dt>

**Projresult**
</dt> <dd>

Eine [**RAS- \_ PPP- \_ Projektions \_ Ergebnis**](ras-ppp-projection-result-str.md) Struktur, die die PPP-Projektionsinformationen für diesen Port angibt. Diese Struktur stellt Informationen für jedes Protokoll bereit, das verhandelt wird, wenn ein RAS-Client eine Verbindung mit einem Server herstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remote Zugriffs Dienst (RAS) (Übersicht)](about-remote-access-service.md)
</dt> <dt>

[RAS-Server-Verwaltungsstrukturen](ras-server-administration-structures.md)
</dt> <dt>

[**RAS- \_ Parameter**](ras-parameters-str.md)
</dt> <dt>

[**RAS- \_ Port \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**RAS- \_ Port \_ Statistik**](ras-port-statistics-str.md)
</dt> <dt>

[**Ergebnis der RAS- \_ PPP- \_ Projektion \_**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**Rasadminakzeptnewconnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**Rasadminconnectionhangupnotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**Rasadminportgetinfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





