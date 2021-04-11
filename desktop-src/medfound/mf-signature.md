---
description: Enthält eine GRL-Signatur (Global Sperrlist).
ms.assetid: 388a901c-6202-41cf-9c3d-f29d8ccca76b
title: MF_SIGNATURE Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_SIGNATURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4827fea8e4259609cbb54f2b58a3d1c88ad6c23e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218117"
---
# <a name="mf_signature-structure"></a>MF- \_ Signatur Struktur

Enthält eine GRL-Signatur (Global Sperrlist).

## <a name="syntax"></a>Syntax


```C++
typedef struct _MF_SIGNATURE {
  DWORD dwSignVer;
  DWORD cbSign;
  BYTE  rgSign[1];
} MF_SIGNATURE;
```



## <a name="members"></a>Member

<dl> <dt>

**dwsignver**
</dt> <dd>

Die Signatur Versionsnummer.

</dd> <dt>

**cbsign**
</dt> <dd>

Die Größe der Signatur in Bytes.

</dd> <dt>

**rgsign**
</dt> <dd>

Ein Bytearray der Größe **cbsign** , das die Signatur enthält. Die tatsächliche Array Größe ist größer als die in der Struktur Deklaration angegebene Größe.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur ist nicht in einem SDK-Header deklariert. Um diese Struktur zu verwenden, fügen Sie die hier gezeigte Deklaration dem Quellcode hinzu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[OPM-Zertifikat Sperrung](opm-certificate-revocation.md)
</dt> <dt>

[OPM-Strukturen](opm-structures.md)
</dt> </dl>

 

 




