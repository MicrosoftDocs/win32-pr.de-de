---
title: MPEXPIRATION_DATA -Struktur (MpClient.h)
description: Benachrichtigung zum Produktablaufstatus.
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- MPEXPIRATION_DATA struktur Legacy Windows Umgebungsfeatures
- PMPEXPIRATION_DATA Strukturzeiger Legacy-Windows-Umgebungsfeatures
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
ms.openlocfilehash: a5f270b7d433e6de7cd1eb3e7a3cfc88c9cb85c6087c20371ac804ec61d949d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976030"
---
# <a name="mpexpiration_data-structure"></a>\_MPEXPIRATION-DATENstruktur

Benachrichtigung zum Produktablaufstatus.

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

Typ: **MP \_ EXPIRE \_ REASON**

</dd> <dd>

Ablaufgrund. Dies ist einer der folgenden möglichen Werte:



| Wert                                                                                                                                                                                                                                | Bedeutung                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> <dt>**MP \_ ABGELAUFEN \_ UNBEKANNT**</dt> <dt>0</dt> </dl> | Unbekannt<br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> <dt>**MP \_ ABGELAUFEN \_ EVAL**</dt> <dt>1</dt> </dl>          | Bewertung.<br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> <dt>**MP \_ EXPIRED \_ WIES**</dt> <dt>2</dt> </dl>             | Wat.<br/>        |



 

</dd> <dt>

**State**
</dt> <dd>

Typ: **MP EXPIRE STATE \_ \_ \_ REPORT**

</dd> <dd>

Ablaufzustand. Dies ist einer der folgenden möglichen Werte:



| Wert                                                                                                                                                                                                                                                                      | Bedeutung                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> <dt>**MP \_ BERICHT \_ "STATUS \_ \_ ABGELAUFEN" UNBEKANNT**</dt> <dt>0</dt> </dl> | Unbekannter Zustand.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> <dt>**MP \_ BERICHT ZUM \_ ABLAUF \_ DES \_ ZUSTANDS GÜLTIG**</dt> <dt>1</dt> </dl>       | Kein Ablauf.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> <dt>**MP \_ WARNUNG 2 \_ DES \_ \_ STATUSBERICHTS "ABLAUF"**</dt> <dt></dt> </dl> | Nahezu abgelaufen.<br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> <dt>**MP \_ BERICHT ZUM \_ ABLAUF \_ DES \_ ZUSTANDS ABGELAUFEN**</dt> <dt>3</dt> </dl> | Abgelaufen.<br/>       |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





