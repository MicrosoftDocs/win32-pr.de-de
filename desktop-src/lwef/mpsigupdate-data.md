---
title: MPSIGUPDATE_DATA Struktur (mpclient. h)
description: Benachrichtigungs Daten werden an die Rückruffunktion der Signatur Aktualisierung übermittelt.
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- MPSIGUPDATE_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPSIGUPDATE_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPSIGUPDATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442b19da394043b6fc6b8693f51c5f150233f970
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104540"
---
# <a name="mpsigupdate_data-structure"></a>Mpsigupdate- \_ Datenstruktur

Benachrichtigungs Daten werden an die Rückruffunktion der Signatur Aktualisierung übermittelt.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPSIGUPDATE_DATA {
  DWORD                 dwPercentComplete;
  DWORD                 dwTotalUpdates;
  DWORD                 dwCurrentUpdateIndex;
  MPSIGUPDATE_TYPE      eType;
  MP_UPDATE_STAGE       Stage;
  MP_MIDL_STRING LPWSTR Path;
} MPSIGUPDATE_DATA, *PMPSIGUPDATE_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**dwprozentucomplete**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Eine Schätzung des Prozentsatzes für alle Updates, die heruntergeladen und/oder installiert wurden.

</dd> <dt>

**dwtotalupdates**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Gesamtzahl der herunter zuladenden und/oder zu installierenden Updates.

</dd> <dt>

**dwcurrentupdateingedex**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

NULL basierter Indexwert, der angibt, welches Update zwischen den erforderlichen zurzeit heruntergeladen und/oder installiert wird.

</dd> <dt>

**ETYPE**
</dt> <dd>

Typ: **mpsigupdate- \_ Typ**

</dd> <dd>

Aktualisieren Sie den Typ. Einer der folgenden möglichen Werte:



| Wert                                                                                                                                                                                                                             | Bedeutung                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <dt>**mpsigupdate- \_ Typ " \_ None"**</dt> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <dt>**verwalteter mpsigupdate- \_ Typ \_**</dt> </dl>                                   | WSUS-Update Abbrechen erfordert Administratorrechte.<br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <dt>**mpsigupdate- \_ Typ \_ http**</dt> </dl>                                            | HTTP-Update. Zum Abbrechen sind keine Administrator Rechte erforderlich.<br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <dt>**mpsigupdate- \_ Typ \_ http \_ SRV**</dt> </dl>                               | HTTP vom Dienst. Abbrechen erfordert Administratorrechte.<br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <dt>**mpsigupdate- \_ Typ \_ UNC**</dt> </dl>                                               | UNC-Freigabe. Zum Abbrechen sind keine Administrator Rechte erforderlich.<br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <dt>**mpsigupdate- \_ Typ \_ nicht verwaltet**</dt> </dl>                             | MU/wu-Update. Abbrechen erfordert Administratorrechte.<br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <dt>**\_ \_ verwaltete \_ Plattform für mpsigupdate-Typ**</dt> </dl>       | WSUS-Update für Plattform. Abbrechen erfordert Administratorrechte.<br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <dt>**mpsigupdate- \_ Typ \_ nicht verwaltete \_ Plattform**</dt> </dl> | MU/wu-Update für Plattform. Abbrechen erfordert Administratorrechte.<br/> |



 

</dd> <dt>

**Phase**
</dt> <dd>

Typ: **MP- \_ Aktualisierungs \_ Phase**

</dd> <dd>

Aktualisierungs Phase. Einer der folgenden möglichen Werte:



| Wert                                                                                                                                                                         | Bedeutung                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <dt>**MP- \_ Stufe \_ unbekannt**</dt> </dl>       | Die Aktualisierungs Phase ist unbekannt.<br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <dt>**MP- \_ Suche- \_ Update**</dt> </dl>       | Aktualisierungs Phase aktualisieren.<br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <dt>**MP- \_ Download \_ Update**</dt> </dl> | Download Stufe aktualisieren.<br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <dt>**MP- \_ Installations \_ Update**</dt> </dl>    | Aktualisieren Sie die Installationsphase.<br/>  |



 

</dd> <dt>

**Pfad**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Aktualisieren Sie den Pfad.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





