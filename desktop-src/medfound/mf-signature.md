---
description: Enthält eine GRL-Signatur (Global Revocation List).
ms.assetid: 388a901c-6202-41cf-9c3d-f29d8ccca76b
title: MF_SIGNATURE-Struktur
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
ms.openlocfilehash: 4d5eec1105e490e68b5fecb46253154b3ed85a112b10641e8394bcc713b71c62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059165"
---
# <a name="mf_signature-structure"></a>MF \_ SIGNATURE-Struktur

Enthält eine GRL-Signatur (Global Revocation List).

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

**dwSignVer**
</dt> <dd>

Die Signaturversionsnummer.

</dd> <dt>

**cbSign**
</dt> <dd>

Die Größe der Signatur in Bytes.

</dd> <dt>

**rgSign**
</dt> <dd>

Ein Bytearray der Größe **cbSign,** das die Signatur enthält. Die tatsächliche Arraygröße ist größer als die in der Strukturdeklaration angegebenen Größe.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird nicht in einem SDK-Header deklariert. Um diese Struktur zu verwenden, fügen Sie ihrem Quellcode die hier gezeigte Deklaration hinzu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[OPM-Zertifikatsperrung](opm-certificate-revocation.md)
</dt> <dt>

[OPM-Strukturen](opm-structures.md)
</dt> </dl>

 

 




