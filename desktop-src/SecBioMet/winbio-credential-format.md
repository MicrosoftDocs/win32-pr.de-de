---
title: WINBIO_CREDENTIAL_FORMAT -Enumeration (Winbio \_ types.h)
description: Definiert Flags, die zum Angeben des Anmeldeinformationsformats des Endbenutzers verwendet werden können.
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- WINBIO_CREDENTIAL_FORMAT enumeration Windows Biometric Framework-API
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
ms.openlocfilehash: 82185bdb9d8170abbdba04e758010443dc8be6a37e198edb27a137024dacf9af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910823"
---
# <a name="winbio_credential_format-enumeration"></a>WINBIO \_ CREDENTIAL \_ FORMAT-Enumeration

Definiert Flags, die zum Angeben des Anmeldeinformationsformats des Endbenutzers verwendet werden können. Diese Enumeration wird von der [**WinBioSetCredential-Funktion**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) verwendet.

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

<span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**WINBIO \_ PASSWORD \_ GENERIC**
</dt> <dd>

Das Kennwort hat ein generisches Format.

</dd> <dt>

<span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**GEPACKTES \_ \_ WINBIO-KENNWORT**
</dt> <dd>

Das Kennwort hat ein komprimiertes Format.

</dd> <dt>

<span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO \_ PASSWORD \_ PROTECTED**
</dt> <dd>

Die Kennwort-Anmeldeinformationen wurden mit [**CredProtect umschlossen.**](/windows/desktop/api/wincred/nf-wincred-credprotecta)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (einschließlich Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungsenumeration](client-application-enumerations.md)
</dt> <dt>

[**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

