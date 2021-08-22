---
title: MPFASTPATH_DATA -Struktur (MpClient.h)
description: FastPath-Updatebenachrichtigung.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- MPFASTPATH_DATA struktur Legacy Windows Umgebungsfeatures
- PMPFASTPATH_DATA Strukturzeiger Legacy-Windows-Umgebungsfeatures
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
ms.openlocfilehash: e138e9c45657cfc4ebeba1d1dbeed38070b6e07d09c512ec96835a04702d0c8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119556150"
---
# <a name="mpfastpath_data-structure"></a>\_MPFASTPATH-DATENstruktur

FastPath-Updatebenachrichtigung.

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

Typ: **[ **MP \_ SIGNATURE \_ TYPE**](mp-signature-type.md)**

</dd> <dd>

Signaturtyp.

</dd> <dt>

**FastPathSignatureType**
</dt> <dd>

Typ: **[ **MP \_ FASTPATH \_ TYPE**](mp-fastpath-type.md)**

</dd> <dd>

FastPath-Signaturtyp.

</dd> <dt>

**FastPathSignatureVersion**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

FastPath-Signaturversion (optional).

</dd> <dt>

**CompilationTimestamp**
</dt> <dd>

Typ: **ULARGE \_ INTEGER**

</dd> <dd>

Kompilierungszeitstempel (UTC).

</dd> <dt>

**PersistenceType**
</dt> <dd>

Typ: **[ **MP \_ PERSISTENCE \_ LIMIT \_ TYPE**](mp-persistence-limit-type.md)**

</dd> <dd>

Persistenztyp (optional).

</dd> <dt>

**PersistenceValue**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Persistenzwert (optional).

</dd> <dt>

**PersistencePath**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Persistenzpfad (optional).

</dd> <dt>

**`Reason`**
</dt> <dd>

Typ: **[ **\_ MP-ENTFERNUNGSGRUND \_**](mp-removal-reason.md)**

</dd> <dd>

Grund für das Entfernen der Signatur.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MP \_ \_ FASTPATH-TYP**](mp-fastpath-type.md)
</dt> <dt>

[**MP \_ PERSISTENCE \_ LIMIT \_ TYPE**](mp-persistence-limit-type.md)
</dt> <dt>

[**\_ \_ MP-SIGNATURTYP**](mp-signature-type.md)
</dt> </dl>

 

 





