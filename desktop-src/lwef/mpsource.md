---
title: Mpsource-Enumeration (mpclient. h)
description: Mögliche Quell Kategorie.
ms.assetid: 1AD12D67-C74B-481A-AC9B-D119AABDB6E9
keywords:
- Mpsource-Enumeration Legacy Windows-Umgebungs Features
- Pmpsource-enumerationszeiger ältere Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPSOURCE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e9255029512499a0e2948a44701ef4482aff4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956734"
---
# <a name="mpsource-enumeration"></a>Mpsource-Enumeration

Mögliche Quell Kategorie.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPSOURCE { 
  MPSOURCE_UNKNOWN             = 0,
  MPSOURCE_USER                = 1,
  MPSOURCE_SYSTEM              = 2,
  MPSOURCE_REALTIME            = 3,
  MPSOURCE_IOAV                = 4,
  MPSOURCE_NIS                 = 5,
  MPSOURCE_BHO                 = 6,
  MPSOURCE_IEPROTECT           = 6,
  MPSOURCE_ELAM                = 7,
  MPSOURCE_LOCAL_ATTESTATION   = 8,
  MPSOURCE_REMOTE_ATTESTATION  = 9,
  MPSOURCE_AMSI                = 10,
  MP_SOURCE_MAXVALUE           = 10
} MPSOURCE, *PMPSOURCE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**mpsource \_ unbekannt**
</dt> <dd>

Die Quelle ist unbekannt.

</dd> <dt>

<span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**mpsource- \_ Benutzer**
</dt> <dd>

Vom Benutzer initiiert.

</dd> <dt>

<span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**mpsource- \_ System**
</dt> <dd>

System initiiert.

</dd> <dt>

<span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**mpsource in \_ Echtzeit**
</dt> <dd>

Die Echtzeit-Komponente wurde initiiert.

</dd> <dt>

<span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**mpsource \_ ioav**
</dt> <dd>

Internet Explorer-Downloads und Outlook Express-Anlagen wurden initiiert.

</dd> <dt>

<span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**mpsource \_ NIS**
</dt> <dd>

Netzwerk Inspektionssystem.

</dd> <dt>

<span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**mpsource- \_ BHO**
</dt> <dd>

BHO-Webskript (veraltet).

</dd> <dt>

<span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**mpsource- \_ ieprotect**
</dt> <dd>

IE-iextensionvalidation.

</dd> <dt>

<span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**mpsource \_ Elam**
</dt> <dd>

ELAM

</dd> <dt>

<span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**lokaler mpsource-Nachweis \_ \_**
</dt> <dd>

Lokaler Nachweis.

</dd> <dt>

<span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**mpsource- \_ Remote Nachweis \_**
</dt> <dd>

Remote Nachweis.

</dd> <dt>

<span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**mpsource- \_ AMSI**
</dt> <dd>

AMSI

</dd> <dt>

<span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**MP- \_ Quelle \_ MaxValue**
</dt> <dd>

Maximal möglicher Wert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





