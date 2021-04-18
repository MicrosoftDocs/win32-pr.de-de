---
title: MPEXPIRATION_DATA Struktur (mpclient. h)
description: Status Benachrichtigung zum Produktablauf.
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- MPEXPIRATION_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPEXPIRATION_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPEXPIRATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df5e417b1ce6b1d1f4c15d646b44b0ea6c1fade2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341358"
---
# <a name="mpexpiration_data-structure"></a>Mpablauf- \_ Datenstruktur

Status Benachrichtigung zum Produktablauf.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPEXPIRATION_DATA {
  MP_EXPIRE_REASON       Reason;
  MP_EXPIRE_STATE_REPORT State;
} MPEXPIRATION_DATA, *PMPEXPIRATION_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**`Reason`**
</dt> <dd>

Typ: **MP \_ läuft \_** ab

</dd> <dd>

Grund für den Ablauf. Dies ist einer der folgenden möglichen Werte:



| Wert                                                                                                                                                                                                                                | Bedeutung                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> <dt>**MP \_ Abgelaufenes \_ unbekannter**</dt> <dt>0</dt> </dl> | Unbekannt<br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> <dt>**MP \_ Abgelaufene \_ eval**</dt> <dt>1</dt> </dl>          | Beurteilung.<br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> <dt>**MP \_ Abgelaufenes \_ Wat**</dt> <dt>2</dt> </dl>             | Wat.<br/>        |



 

</dd> <dt>

**State**
</dt> <dd>

Typ: **\_ Bericht zum \_ Status \_ "MP läuft** ab"

</dd> <dd>

Ablauf Status. Dies ist einer der folgenden möglichen Werte:



| Wert                                                                                                                                                                                                                                                                      | Bedeutung                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> <dt>**MP \_ Ablauf \_ Status \_ Bericht \_ unbekannt**</dt> <dt>0</dt> </dl> | Unbekannter Zustand.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> <dt>**MP \_ Ablauf \_ Status \_ Bericht \_ gültig**</dt> <dt>1</dt> </dl>       | Kein Ablauf.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> <dt>**MP \_ Ablauf \_ Status \_ Bericht \_ Warnung**</dt> <dt>2</dt> </dl> | Fast abgelaufen.<br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> <dt>**MP \_ Ablauf \_ Status \_ Bericht \_ abgelaufen**</dt> <dt>3</dt> </dl> | Frist.<br/>       |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





