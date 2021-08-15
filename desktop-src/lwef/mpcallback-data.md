---
title: MPCALLBACK_DATA -Struktur (MpClient.h)
description: An die Rückruffunktion übergebene Daten.
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- MPCALLBACK_DATA struktur Legacy Windows Umgebungsfeatures
- PMPCALLBACK_DATA strukturzeiger Legacy-Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPCALLBACK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1eb129101c341485a1e6b5763a0325cbf586a6e51e5e2875b4465696c39df8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883652"
---
# <a name="mpcallback_data-structure"></a>\_MPCALLBACK-DATENstruktur

An die Rückruffunktion übergebene Daten.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPCALLBACK_DATA {
  MPNOTIFY        Notify;
  HRESULT         hResult;
  ULARGE_INTEGER  TimeStamp;
  MPCALLBACK_TYPE Type;
  union {
    PMPSTATUS_DATA         pStatusData;
    PMPSCAN_DATA           pScanData;
    PMPCLEAN_DATA          pCleanData;
    PMPCLEAN_PRECHECK_DATA pPrecheckData;
    PMPTHREAT_DATA         pThreatData;
    PMPSIGUPDATE_DATA      pSigUpdateData;
    PMPSAMPLE_DATA         pSampleData;
    PMPRESERVED_DATA       pReservedData;
    PMPCONFIGURATION_DATA  pConfigurationData;
    PMPFASTPATH_DATA       pFastPathData;
    PMPEXPIRATION_DATA     pExpirationData;
    PMPNIS_PRIVATE_DATA    pNISPrivateData;
    PMPHEALTH_DATA         pHealthData;
    PMPENDOFLIFE_DATA      pEndOfLifeData;
    PMPMALWARETOAST_DATA   pMalwareToastData;
  } Data;
} MPCALLBACK_DATA, *PMPCALLBACK_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**Benachrichtigen**
</dt> <dd>

Typ: **[ **MPNOTIFY**](mpnotify.md)**

</dd> <dd>

Ändern Sie die Benachrichtigung in bericht.

</dd> <dt>

**Hresult**
</dt> <dd>

Typ: **HRESULT**

</dd> <dd>

Fehlercode im Falle eines internen Fehlers.

</dd> <dt>

**Timestamp**
</dt> <dd>

Typ: **ULARGE \_ INTEGER**

</dd> <dd>

Aktueller Zeitstempel.

</dd> <dt>

**Typ**
</dt> <dd>

Typ: **[ **MPCALLBACK-TYP \_**](mpcallback-type.md)**

</dd> <dd>

Besonderer Rückrufdatentyp.

</dd> <dt>

**Daten**
</dt> <dd>

Rückruf von speziellen Daten. Der Zeiger auf die entsprechende Struktur hängt vom Wert des Typs **ab.**

<dl> <dt>

**pStatusData**
</dt> <dd>

Typ: **PMPSTATUS \_ DATA**

</dd> <dd>

Wenn **Sie**  ==  **MPCALLBACK \_ STATUS eingeben.** Weitere Informationen [**finden Sie unter MPSTATUS \_ DATA**](mpstatus-data.md).

</dd> <dt>

**pScanData**
</dt> <dd>

Typ: **PMPSCAN \_ DATA**

</dd> <dd>

Wenn Sie  ==  **MPCALLBACK \_ SCAN eingeben.** Weitere Informationen [**finden Sie unter MPSCAN \_ DATA**](mpscan-data.md).

</dd> <dt>

**pCleanData**
</dt> <dd>

Typ: **PMPCLEAN \_ DATA**

</dd> <dd>

Wenn Sie  ==  **MPCALLBACK \_ CLEAN eingeben.** Weitere Informationen [**finden Sie unter MPCLEAN \_ DATA**](mpclean-data.md).

</dd> <dt>

**pPrecheckData**
</dt> <dd>

Typ: **PMPCLEAN \_ PRECHECK \_ DATA**

</dd> <dd>

Wenn Sie  ==  **MPCALLBACK \_ PRECHECK eingeben.** Weitere Informationen [**finden Sie unter MPCLEAN \_ PRECHECK \_ DATA**](mpclean-precheck-data.md).

</dd> <dt>

**pThreatData**
</dt> <dd>

Typ: **PMPTHREAT \_ DATA**

</dd> <dd>

Wenn Sie  ==  **MPCALLBACK \_ THREAT eingeben.** Weitere Informationen [**finden Sie unter MPTHREAT \_ DATA**](mpthreat-data.md).

</dd> <dt>

**pSigUpdateData**
</dt> <dd>

Typ: **PMPSIGUPDATE \_ DATA**

</dd> <dd>

Wenn Sie  ==  **MPCALLBACK \_ SIGUPDATE eingeben.** Weitere Informationen [**finden Sie unter MPSIGUPDATE \_ DATA**](mpsigupdate-data.md).

</dd> <dt>

**pSampleData**
</dt> <dd>

Typ: **PMPSAMPLE \_ DATA**

</dd> <dd>

Wenn Sie  ==  **MPCALLBACK \_ SAMPLE eingeben.** Weitere Informationen [**finden Sie unter MPSAMPLE \_ DATA**](mpsample-data.md).

</dd> <dt>

**pReservedData**
</dt> <dd>

Typ: **PMPRESERVED \_ DATA**

</dd> <dd>

Wenn Sie  ==  **MPCALLBACK \_ RESERVED eingeben.** Weitere Informationen [**finden Sie unter MPRESERVED \_ DATA**](mpreserved-data.md).

</dd> <dt>

**pConfigurationData**
</dt> <dd>

Typ: **PMPCONFIGURATION \_ DATA**

</dd> <dd>

Wenn Sie  ==  **MPCALLBACK \_ CONFIGURATION NOTIFICATION \_ eingeben.** Weitere Informationen [**finden Sie unter MPCONFIGURATION \_ DATA**](mpconfiguration-data.md).

</dd> <dt>

**pFastPathData**
</dt> <dd>

Typ: **PMPFASTPATH \_ DATA**

</dd> <dd>

Wenn Sie  ==  **MPCALLBACK \_ FASTPATH eingeben.** Weitere Informationen [**finden Sie unter MPFASTPATH \_ DATA**](mpfastpath-data.md).

</dd> <dt>

**pExpirationData**
</dt> <dd>

Typ: **PMPEXPIRATION \_ DATA**

</dd> <dd>

Wenn Sie  ==  **MPCALLBACK PRODUCT \_ EXPIRATION \_ eingeben.** Weitere Informationen [**finden Sie unter MPEXPIRATION \_ DATA**](mpexpiration-data.md).

</dd> <dt>

**pNISPrivateData**
</dt> <dd>

Typ: **PMPNIS \_ PRIVATE \_ DATA**

</dd> <dd>

Wenn Sie  ==  **MPCALLBACK \_ NIS PRIVATE \_ eingeben.** Weitere Informationen [**finden Sie unter PRIVATE \_ \_ MPNIS-DATEN.**](mpnis-private-data.md)

</dd> <dt>

**pHealthData**
</dt> <dd>

Typ: **PMPHEALTH \_ DATA**

</dd> <dd>

Wenn Sie  ==  **MPCALLBACK \_ HEALTH eingeben.** Weitere Informationen [**finden Sie unter MPHEALTH \_ DATA**](mphealth-data.md).

</dd> <dt>

**pEndOfLifeData**
</dt> <dd>

Typ: **PMPENDOFLIFE \_ DATA**

</dd> <dd>

Wenn **Sie**  ==  **MPCALLBACK \_ ENDOFLIFE eingeben.** Weitere Informationen [**finden Sie unter MPENDOFLIFE \_ DATA**](mpendoflife-data.md).

</dd> <dt>

**pMalwareToastData**
</dt> <dd>

Typ: **PMPMALWARETOAST \_ DATA**

</dd> <dd>

Wenn Sie  ==  **MPCALLBACK \_ MALWARETOAST eingeben.** Weitere Informationen [**finden Sie unter MPMALWARETOAST \_ DATA**](mpmalwaretoast-data.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MPCALLBACK-TYP \_**](mpcallback-type.md)
</dt> <dt>

[**MPCLEAN \_ DATA**](mpclean-data.md)
</dt> <dt>

[**MPCLEAN \_ PRECHECK \_ DATA**](mpclean-precheck-data.md)
</dt> <dt>

[**MPCONFIGURATION-DATEN \_**](mpconfiguration-data.md)
</dt> <dt>

[**MPENDOFLIFE-DATEN \_**](mpendoflife-data.md)
</dt> <dt>

[**\_MPEXPIRATION-DATEN**](mpexpiration-data.md)
</dt> <dt>

[**MPFASTPATH-DATEN \_**](mpfastpath-data.md)
</dt> <dt>

[**\_MPHEALTH-DATEN**](mphealth-data.md)
</dt> <dt>

[**MPMALWARETOAST-DATEN \_**](mpmalwaretoast-data.md)
</dt> <dt>

[**PRIVATE \_ \_ MPNIS-DATEN**](mpnis-private-data.md)
</dt> <dt>

[**MPNOTIFY**](mpnotify.md)
</dt> <dt>

[**M BEIBEHALTENE \_ DATEN**](mpreserved-data.md)
</dt> <dt>

[**\_MPSAMPLE-DATEN**](mpsample-data.md)
</dt> <dt>

[**\_MPSCAN-DATEN**](mpscan-data.md)
</dt> <dt>

[**\_MPSIGUPDATE-DATEN**](mpsigupdate-data.md)
</dt> <dt>

[**\_MPSTATUS-DATEN**](mpstatus-data.md)
</dt> <dt>

[**\_MPTHREAT-DATEN**](mpthreat-data.md)
</dt> </dl>

 

 





