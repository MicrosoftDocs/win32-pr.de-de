---
title: MPCALLBACK_DATA Struktur (mpclient. h)
description: An die Rückruffunktion über gegebene Daten.
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- MPCALLBACK_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPCALLBACK_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: 9741ca479eeb9770a3ae8c2aedbc51a8a2643033
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103567"
---
# <a name="mpcallback_data-structure"></a>Mpcallback- \_ Datenstruktur

An die Rückruffunktion über gegebene Daten.

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

Typ: **[ **mpnotify**](mpnotify.md)**

</dd> <dd>

Ändern Sie die Benachrichtigung in den Bericht.

</dd> <dt>

**HRESULT**
</dt> <dd>

Typ: **HRESULT**

</dd> <dd>

Fehlercode im Falle eines internen Fehlers.

</dd> <dt>

**Zeitstempel**
</dt> <dd>

Typ: **ularge \_ Integer**

</dd> <dd>

Aktueller Zeitstempel.

</dd> <dt>

**Type**
</dt> <dd>

Typ: **[ **mpcallback- \_ Typ**](mpcallback-type.md)**

</dd> <dd>

Spezieller Rückruf Datentyp.

</dd> <dt>

**Daten**
</dt> <dd>

Rückruf-Sonderdaten. Der Zeiger auf die entsprechende-Struktur hängt vom Wert des **Typs** ab.

<dl> <dt>

**pstatus Data**
</dt> <dd>

Typ: **pmpstatus- \_ Daten**

</dd> <dd>

Wenn Sie  ==  **mpcallback- \_ Status** eingeben. Siehe [**mpstatus- \_ Daten**](mpstatus-data.md).

</dd> <dt>

**pscandata**
</dt> <dd>

Typ: **pmpscan- \_ Daten**

</dd> <dd>

Beim **Typ**  ==  **mpcallback \_ Scan**. Siehe [**mpscan- \_ Daten**](mpscan-data.md).

</dd> <dt>

**pcleandata**
</dt> <dd>

Typ: **pmpclean- \_ Daten**

</dd> <dd>

Wenn **Sie**  ==  **mpcallback \_ Bereinigen**. Siehe [**mpclean \_ Data**](mpclean-data.md).

</dd> <dt>

**pprecheckdata**
</dt> <dd>

Type: **pmpclean \_ Precheck- \_ Daten**

</dd> <dd>

Beim **Typ**  ==  **mpcallback \_ Precheck**. Siehe [**mpclean \_ Precheck \_ Data**](mpclean-precheck-data.md).

</dd> <dt>

**p-Data**
</dt> <dd>

Typ: **pmpthreat- \_ Daten**

</dd> <dd>

Beim **Typ**  ==  **mpcallback \_ Threat**. Siehe [**mpthreat- \_ Daten**](mpthreat-data.md).

</dd> <dt>

**psigupdatedata**
</dt> <dd>

Typ: **pmpsigupdate- \_ Daten**

</dd> <dd>

Wenn Sie  ==  **mpcallback \_ sigupdate** eingeben. Siehe [**mpsigupdate- \_ Daten**](mpsigupdate-data.md).

</dd> <dt>

**psampledata**
</dt> <dd>

Type: **pmpsample \_ Data**

</dd> <dd>

Wenn Sie  ==  **mpcallback- \_ Beispiel** eingeben. Siehe [**mpsample \_ Data**](mpsample-data.md).

</dd> <dt>

**preserveddata**
</dt> <dd>

Typ: **pmbeibehaltene \_ Daten**

</dd> <dd>

Wenn der **Typ**  ==  **mpcallback \_ reserviert** ist. Siehe [**mbeibehaltene \_ Daten**](mpreserved-data.md).

</dd> <dt>

**pconfigurationdata**
</dt> <dd>

Typ: **pmpconfiguration- \_ Daten**

</dd> <dd>

Wenn Sie  ==  **mpcallback- \_ Konfigurations \_ Benachrichtigung** eingeben. Siehe [**mpconfiguration \_ Data**](mpconfiguration-data.md).

</dd> <dt>

**pfastpathdata**
</dt> <dd>

Typ: **pmpfastpath- \_ Daten**

</dd> <dd>

Wenn Sie  ==  **mpcallback \_ FastPath** eingeben. Siehe [**mpfastpath- \_ Daten**](mpfastpath-data.md).

</dd> <dt>

**pexpirationdata**
</dt> <dd>

Typ: **\_ pmpabgelaufdaten**

</dd> <dd>

Wenn Sie  ==  **mpcallback- \_ Produkt \_ Ablauf** eingeben. Siehe [**mpablauf- \_ Daten**](mpexpiration-data.md).

</dd> <dt>

**pnisprivatedata**
</dt> <dd>

Typ: **pmpnis \_ private \_ Daten**

</dd> <dd>

Wenn Sie  ==  **mpcallback \_ NIS \_ private** eingeben. Weitere Informationen finden Sie unter [**mpnis \_ private \_ Data**](mpnis-private-data.md).

</dd> <dt>

**phealthdata**
</dt> <dd>

Typ: **pmphealth- \_ Daten**

</dd> <dd>

Beim **Typ**  ==  **mpcallback \_ Health**. Siehe [**mphealth- \_ Daten**](mphealth-data.md).

</dd> <dt>

**"pdoflifedata"**
</dt> <dd>

Typ: **\_ pmpendomelife-Daten**

</dd> <dd>

Wenn Sie  ==  **mpcallback \_ endoentlife** eingeben. Weitere Informationen finden Sie unter [**\_ mpendomelife-Daten**](mpendoflife-data.md).

</dd> <dt>

**pmalwaretoastdata**
</dt> <dd>

Typ: **pmpmalwarepopup- \_ Daten**

</dd> <dd>

Wenn Sie  ==  **mpcallback \_ malwaretoast** eingeben. Siehe [**mpmalwarepopup- \_ Daten**](mpmalwaretoast-data.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**mpcallback- \_ Typ**](mpcallback-type.md)
</dt> <dt>

[**mpclean- \_ Daten**](mpclean-data.md)
</dt> <dt>

[**mpclean- \_ vorprüf \_ Daten**](mpclean-precheck-data.md)
</dt> <dt>

[**mpconfiguration- \_ Daten**](mpconfiguration-data.md)
</dt> <dt>

[**\_mpendomelife-Daten**](mpendoflife-data.md)
</dt> <dt>

[**mpablauf- \_ Daten**](mpexpiration-data.md)
</dt> <dt>

[**mpfastpath- \_ Daten**](mpfastpath-data.md)
</dt> <dt>

[**mphealth- \_ Daten**](mphealth-data.md)
</dt> <dt>

[**mpmalwarepopup- \_ Daten**](mpmalwaretoast-data.md)
</dt> <dt>

[**Private mpnis- \_ \_ Daten**](mpnis-private-data.md)
</dt> <dt>

[**Mpnotify**](mpnotify.md)
</dt> <dt>

[**mbeibehaltene \_ Daten**](mpreserved-data.md)
</dt> <dt>

[**mpsample- \_ Daten**](mpsample-data.md)
</dt> <dt>

[**mpscan- \_ Daten**](mpscan-data.md)
</dt> <dt>

[**mpsigupdate- \_ Daten**](mpsigupdate-data.md)
</dt> <dt>

[**mpstatus- \_ Daten**](mpstatus-data.md)
</dt> <dt>

[**mpthreat- \_ Daten**](mpthreat-data.md)
</dt> </dl>

 

 





