---
title: WINBIO_CREDENTIAL_TYPE-Enumeration (Winbio \_ types.h)
description: Definiert Flags, die zum Filtern nach dem Anmeldeinformationstyp verwendet werden können.
ms.assetid: 7ef2d4b3-e1f9-46a0-8fc2-0e8660805ac3
keywords:
- WINBIO_CREDENTIAL_TYPE Enumeration Windows Biometric Framework-API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_TYPE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d559d97022f6c240e8a310adef829d47799683ad214fd0bfb0b54c6ec66cf5c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867970"
---
# <a name="winbio_credential_type-enumeration"></a>WINBIO \_ CREDENTIAL \_ TYPE-Enumeration

Definiert Flags, die zum Filtern nach dem Anmeldeinformationstyp verwendet werden können. Diese Enumeration wird von den Funktionen [**WinBioSetCredential,**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)und [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_CREDENTIAL_TYPE { 
  WINBIO_CREDENTIAL_PASSWORD  = 0x00000001,
  WINBIO_CREDENTIAL_ALL       = 0xffffffff
} WINBIO_CREDENTIAL_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WINBIO_CREDENTIAL_PASSWORD"></span><span id="winbio_credential_password"></span>**WINBIO \_ CREDENTIAL \_ PASSWORD**
</dt> <dd>

Filtert Kennwortanmeldeinformationen.

</dd> <dt>

<span id="WINBIO_CREDENTIAL_ALL"></span><span id="winbio_credential_all"></span>**WINBIO \_ CREDENTIAL \_ ALL**
</dt> <dd>

Filtert alle Anmeldeinformationen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Clientanwendungsenumerationen](client-application-enumerations.md)
</dt> <dt>

[**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> <dt>

[**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
</dt> <dt>

[**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

 





