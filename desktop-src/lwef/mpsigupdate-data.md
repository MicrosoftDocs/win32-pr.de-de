---
title: MPSIGUPDATE_DATA-Struktur (MpClient.h)
description: Benachrichtigungsdaten, die an die Rückruffunktion der Signaturaktualisierung übergeben werden.
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- MPSIGUPDATE_DATA struktur Legacy Windows Environment Features (Legacy-Windows-Umgebungsfeatures)
- PMPSIGUPDATE_DATA Strukturzeiger Legacy Windows Umgebungsfeatures
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
ms.openlocfilehash: d3c117b92882a24a825aee5c5b008e10721c40b8a93d26a9a677bb79858635c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476252"
---
# <a name="mpsigupdate_data-structure"></a>MPSIGUPDATE \_ DATA-Struktur

Benachrichtigungsdaten, die an die Rückruffunktion der Signaturaktualisierung übergeben werden.

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

**dwPercentComplete**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Eine Schätzung des Prozentsatzes für alle Updates, die heruntergeladen und/oder installiert wurden.

</dd> <dt>

**dwTotalUpdates**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Gesamtanzahl der herunterzuladende und/oder zu installierende Updates.

</dd> <dt>

**dwCurrentUpdateIndex**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Nullbasierter Indexwert, der angibt, welches Update für die erforderlichen Updates derzeit heruntergeladen und/oder installiert wird.

</dd> <dt>

**eType**
</dt> <dd>

Typ: **MPSIGUPDATE \_ TYPE**

</dd> <dd>

Updatetyp. Einer der folgenden möglichen Werte:



| Wert                                                                                                                                                                                                                             | Bedeutung                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <dt>**\_MPSIGUPDATE-TYP \_ NONE**</dt> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <dt>**\_VERWALTETER MPSIGUPDATE-TYP \_**</dt> </dl>                                   | WSUS-Update. Zum Abbrechen sind Administratorrechte erforderlich.<br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <dt>**\_MPSIGUPDATE-TYP \_ HTTP**</dt> </dl>                                            | HTTP-Update. Administratorrechte zum Abbrechen nicht erforderlich.<br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <dt>**\_MPSIGUPDATE-TYP \_ HTTP \_ SRV**</dt> </dl>                               | HTTP vom Dienst. Zum Abbrechen sind Administratorrechte erforderlich.<br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <dt>**\_MPSIGUPDATE-TYP \_ UNC**</dt> </dl>                                               | UNC-Freigabe. Administratorrechte zum Abbrechen nicht erforderlich.<br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <dt>**\_MPSIGUPDATE-TYP \_ NICHT VERWALTET**</dt> </dl>                             | MU/WU-Update. Zum Abbrechen sind Administratorrechte erforderlich.<br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <dt>**VERWALTETE PLATTFORM VOM TYP MPSIGUPDATE \_ \_ \_**</dt> </dl>       | WSUS-Update für PLATFORM. Zum Abbrechen sind Administratorrechte erforderlich.<br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <dt>**\_NICHT VERWALTETE \_ \_ PLATTFORM VOM TYP MPSIGUPDATE**</dt> </dl> | MU/WU-Update für PLATFORM. Zum Abbrechen sind Administratorrechte erforderlich.<br/> |



 

</dd> <dt>

**Phase**
</dt> <dd>

Typ: **MP \_ UPDATE \_ STAGE**

</dd> <dd>

Aktualisierungsphase. Einer der folgenden möglichen Werte:



| Wert                                                                                                                                                                         | Bedeutung                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <dt>**MP \_ STAGE \_ UNKNOWN**</dt> </dl>       | Updatephase unbekannt.<br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <dt>**\_UPDATE DER MP-SUCHE \_**</dt> </dl>       | Aktualisieren sie die Suchphase.<br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <dt>**MP \_ DOWNLOAD \_ UPDATE**</dt> </dl> | Update-Downloadphase.<br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <dt>**MP \_ INSTALL \_ UPDATE**</dt> </dl>    | Updateinstallationsphase.<br/>  |



 

</dd> <dt>

**Path**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Aktualisieren Sie den Pfad.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





