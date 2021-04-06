---
title: MPTHREAT_INFOEX_BEHAVIOR Struktur (mpclient. h)
description: Enthält Verhaltens Änderungs spezifische Informationen.
ms.assetid: 762E755F-5BA1-476D-B395-6617093309C5
keywords:
- MPTHREAT_INFOEX_BEHAVIOR Struktur Funktionen der Legacy-Windows-Umgebung
- PMPTHREAT_INFOEX_BEHAVIOR Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_BEHAVIOR
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0bc00aeb56aec38b88f2590211c705079834f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743176"
---
# <a name="mpthreat_infoex_behavior-structure"></a>Mpthreat- \_ INFOEX- \_ Verhaltens Struktur

Enthält Verhaltens Änderungs spezifische Informationen.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPTHREAT_INFOEX_BEHAVIOR {
  ULARGE_INTEGER         SignatureID;
  ULONGLONG              EngineVersion;
  ULONGLONG              ASDeltaSignatureVersion;
  ULONGLONG              AVDeltaSignatureVersion;
  MP_HASH_TYPE           HashType;
  DWORD                  FidelityValue;
  MP_MIDL_STRING  LPWSTR HashValue;
  MP_MIDL_STRING  LPWSTR TargetFileName;
  MP_MIDL_STRING  LPWSTR TargetFileHash;
} MPTHREAT_INFOEX_BEHAVIOR, *PMPTHREAT_INFOEX_BEHAVIOR;
```



## <a name="members"></a>Member

<dl> <dt>

**SignatureId**
</dt> <dd>

Typ: **ularge \_ Integer**

</dd> <dd>

Signatur-ID der Verhaltensänderung, die von der Engine zum Zeitpunkt der Erkennung angegeben wurde.

</dd> <dt>

**EngineVersion**
</dt> <dd>

Typ: **ULONGLONG**

</dd> <dd>

Engine-Modulversion.

</dd> <dt>

**Asdelta-signatureversion**
</dt> <dd>

Typ: **ULONGLONG**

</dd> <dd>

AntiSpyware-Signatur Version.

</dd> <dt>

**Avdelta-signatureversion**
</dt> <dd>

Typ: **ULONGLONG**

</dd> <dd>

Antivirus-Signatur Version

</dd> <dt>

**Hashtyp**
</dt> <dd>

Typ: **[ **MP \_ - \_ Hashtyp**](mp-hash-type.md)**

</dd> <dd>

Der verwendete Hashtyp. Siehe [**MP \_ - \_ Hashtyp**](mp-hash-type.md).

</dd> <dt>

**"Fdelta-Wert"**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Fidelity-Wert.

</dd> <dt>

**Hashwert**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Der Hash der Datei.

</dd> <dt>

**TargetFileName**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Der Pfad und der Name der Zieldatei.

</dd> <dt>

**Targetflehash**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Der Hash der Zieldatei.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MP \_ - \_ Hashtyp**](mp-hash-type.md)
</dt> </dl>

 

 





