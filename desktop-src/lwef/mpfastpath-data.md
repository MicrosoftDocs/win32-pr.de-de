---
title: MPFASTPATH_DATA Struktur (mpclient. h)
description: FastPath-Aktualisierungs Benachrichtigung.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- MPFASTPATH_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPFASTPATH_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPFASTPATH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2850a48074fee6984564550683c7fe595d0779ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342007"
---
# <a name="mpfastpath_data-structure"></a>Mpfastpath- \_ Datenstruktur

FastPath-Aktualisierungs Benachrichtigung.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPFASTPATH_DATA {
  MP_SIGNATURE_TYPE         SignatureType;
  MP_FASTPATH_TYPE          FastPathSignatureType;
  MP_MIDL_STRING LPWSTR     FastPathSignatureVersion;
  ULARGE_INTEGER            CompilationTimestamp;
  MP_PERSISTENCE_LIMIT_TYPE PersistenceType;
  MP_MIDL_STRING LPWSTR     PersistenceValue;
  MP_MIDL_STRING LPWSTR     PersistencePath;
  MP_REMOVAL_REASON         Reason;
} MPFASTPATH_DATA, *PMPFASTPATH_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**SignatureType**
</dt> <dd>

Typ: **[ **MP- \_ Signatur \_ Typen**](mp-signature-type.md)**

</dd> <dd>

Signaturtyp.

</dd> <dt>

**Fastpathsignaturetype**
</dt> <dd>

Typ: **[ **MP- \_ FastPath- \_ Typ**](mp-fastpath-type.md)**

</dd> <dd>

FastPath-Signaturtyp.

</dd> <dt>

**Fastpathsignatureversion**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

FastPath-Signatur Version (optional).

</dd> <dt>

**Compilationtimestamp**
</dt> <dd>

Typ: **ularge \_ Integer**

</dd> <dd>

Kompilierungszeit Stempel (UTC).

</dd> <dt>

**PersistenceType**
</dt> <dd>

Typ: **[ **MP \_ - \_ persistenzlimit- \_ Typ**](mp-persistence-limit-type.md)**

</dd> <dd>

Persistenztyp (optional).

</dd> <dt>

**Persistencevalue**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Persistenzwert (optional).

</dd> <dt>

**Persistencepath**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Persistenzpfad (optional).

</dd> <dt>

**`Reason`**
</dt> <dd>

Typ: **[ **MP- \_ Entfernungs \_ Grund**](mp-removal-reason.md)**

</dd> <dd>

Grund für das Entfernen der Signatur.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MP- \_ FastPath- \_ Typ**](mp-fastpath-type.md)
</dt> <dt>

[**MP \_ - \_ persistenzgrenzwert \_**](mp-persistence-limit-type.md)
</dt> <dt>

[**MP- \_ Signatur \_ Typen**](mp-signature-type.md)
</dt> </dl>

 

 





