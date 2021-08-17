---
title: RAS_SERVER_0 -Struktur (Rassapi.h)
description: Die RAS \_ SERVER 0-Struktur wird von der RasAdminServerGetInfo-Funktion verwendet, um Informationen zu den ports zurück, die auf einem \_ RAS-Server konfiguriert sind.
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- RAS_SERVER_0-Struktur
- PRAS_SERVER_0 Strukturzeiger RAS
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
ms.openlocfilehash: dbb7a135fd6f8d1d77b59d1085460d51ad5357e47ca1a050e3d1ba6fd89461c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789384"
---
# <a name="ras_server_0-structure"></a>RAS \_ SERVER \_ 0-Struktur

\[Die **RAS \_ SERVER \_ 0-Struktur** wird ab vista Windows unterstützt.\]

Die **RAS \_ SERVER \_ 0-Struktur** wird von der [**RasAdminServerGetInfo-Funktion**](rasadminservergetinfo.md) verwendet, um Informationen zu den ports zurück, die auf einem RAS-Server konfiguriert sind.

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

**TotalPorts**
</dt> <dd>

Gibt die Gesamtzahl der auf dem RAS-Server konfigurierten Ports an, mit denen Remoteclients eine Verbindung herstellen können. Wenn z. B. die Gesamtzahl der Ports, die für die Einwahl bei einem Server konfiguriert sind, aber einer der Ports derzeit für das Auswählen verwendet wird, ist **TotalPorts** drei.

</dd> <dt>

**PortsInUse**
</dt> <dd>

Gibt die Anzahl der Ports an, die derzeit von Remoteclients verwendet werden.

</dd> <dt>

**RasVersion**
</dt> <dd>

Gibt die Version des RAS-Servers an. Verwenden Sie diese Informationen, um versionsspezifische Aktionen zu ergreifen. Dieser Member ist einer der folgenden Werte.



| Wert                                                                                                                                                                  | Bedeutung                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <dt>**RASDOWNLEVEL**</dt> </dl>              | Gibt einen RAS-Server der LAN Manager-Version 1.0 an.<br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <dt>**RASADMIN \_ 35**</dt> </dl>                | Gibt einen Windows NT Server 3.51 und früher RAS-Server oder -Client an.<br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <dt>**RASADMIN \_ CURRENT**</dt> </dl> | Gibt einen Windows NT 4.0 RAS-Server oder -Client an.<br/>                     |



 

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

[Ras-Dienst (RAS): Übersicht](about-remote-access-service.md)
</dt> <dt>

[RAS-Serververwaltungsstrukturen](ras-server-administration-structures.md)
</dt> <dt>

[**RasAdminServerGetInfo**](rasadminservergetinfo.md)
</dt> </dl>

 

 





