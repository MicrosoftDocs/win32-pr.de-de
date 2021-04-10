---
title: WINBIO_CREDENTIAL_FORMAT-Enumeration (winbio \_ types. h)
description: Definiert Flags, die verwendet werden können, um das Format der Anmelde Informationen für den Endbenutzer anzugeben.
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- WINBIO_CREDENTIAL_FORMAT Enumeration Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa28ea56c7af9f78947e64587740300a70f763ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103695"
---
# <a name="winbio_credential_format-enumeration"></a>Winbio \_ Credential \_ Format-Enumeration

Definiert Flags, die verwendet werden können, um das Format der Anmelde Informationen für den Endbenutzer anzugeben. Diese Enumeration wird von der [**winbiosetcredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) -Funktion verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_CREDENTIAL_FORMAT { 
  WINBIO_PASSWORD_GENERIC    = 0x00000001,
  WINBIO_PASSWORD_PACKED     = 0x00000002,
  WINBIO_PASSWORD_PROTECTED  = 0x00000003
} WINBIO_CREDENTIAL_FORMAT;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**winbio- \_ Kennwort \_ generisch**
</dt> <dd>

Das Kennwort ist in einem generischen Format angegeben.

</dd> <dt>

<span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**winbio- \_ Kennwort \_ gepackt**
</dt> <dd>

Das Kennwort weist ein komprimiertes Format auf.

</dd> <dt>

<span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**winbio- \_ Kennwort \_ geschützt**
</dt> <dd>

Die Kenn Wort Anmelde Informationen wurden mit " [**kredprotect**](/windows/desktop/api/wincred/nf-wincred-credprotecta)" umschließt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Enumerationen von Client Anwendungen](client-application-enumerations.md)
</dt> <dt>

[**Winbiosetcredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

