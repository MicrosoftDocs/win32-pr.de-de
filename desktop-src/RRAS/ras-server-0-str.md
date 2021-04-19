---
title: RAS_SERVER_0 Struktur (rassapi. h)
description: Die Struktur des RAS- \_ Servers \_ 0 wird von der rasadminservergetinfo-Funktion verwendet, um Informationen zu den auf einem RAS-Server konfigurierten Ports zurückzugeben.
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- RAS_SERVER_0 Struktur-RAS
- PRAS_SERVER_0-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- RAS_SERVER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f910fdfe53221daf8227d9f3e594133548fee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338778"
---
# <a name="ras_server_0-structure"></a>RAS- \_ Server- \_ 0-Struktur

\[Die Struktur des **RAS- \_ Servers \_ 0** wird ab Windows Vista nicht unterstützt.\]

Die Struktur des **RAS- \_ Servers \_ 0** wird von der [**rasadminservergetinfo**](rasadminservergetinfo.md) -Funktion verwendet, um Informationen zu den auf einem RAS-Server konfigurierten Ports zurückzugeben.

## <a name="syntax"></a>Syntax


```C++
typedef struct _RAS_SERVER_0 {
  WORD  TotalPorts;
  WORD  PortsInUse;
  DWORD RasVersion;
} RAS_SERVER_0, *PRAS_SERVER_0;
```



## <a name="members"></a>Member

<dl> <dt>

**Totalports**
</dt> <dd>

Gibt die Gesamtanzahl der auf dem RAS-Server konfigurierten Ports an, die für Remote Clients zum Herstellen einer Verbindung verfügbar sind. Wenn z. b. die Gesamtanzahl der Ports, die für die Einwahl eines Servers konfiguriert sind, vier beträgt, aber einer der Ports zurzeit für das Auschecken verwendet wird, beträgt **totalports** drei.

</dd> <dt>

**Portsinuse**
</dt> <dd>

Gibt die Anzahl der Ports an, die zurzeit von Remote Clients verwendet werden.

</dd> <dt>

**Rasversion**
</dt> <dd>

Gibt die Version des RAS-Servers an. Verwenden Sie diese Informationen, um versionsspezifische Aktionen auszuführen. Dieser Member ist einer der folgenden Werte.



| Wert                                                                                                                                                                  | Bedeutung                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <dt>**Rasdownlevel**</dt> </dl>              | Gibt einen RAS-Server der LAN-Manager-Version 1,0 an.<br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <dt>**Rasadmin \_ 35**</dt> </dl>                | Gibt einen RAS-Server oder-Client für Windows NT Server 3,51 und frühere Versionen an.<br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <dt>**rasadmin \_ aktuell**</dt> </dl> | Gibt einen Windows NT 4,0-RAS-Server oder-Client an.<br/>                     |



 

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

[**Rasadminservergetinfo**](rasadminservergetinfo.md)
</dt> </dl>

 

 





