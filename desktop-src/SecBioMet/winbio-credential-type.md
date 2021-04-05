---
title: WINBIO_CREDENTIAL_TYPE-Enumeration (winbio \_ types. h)
description: Definiert Flags, die verwendet werden können, um nach dem Anmelde Informationstyp zu filtern.
ms.assetid: 7ef2d4b3-e1f9-46a0-8fc2-0e8660805ac3
keywords:
- WINBIO_CREDENTIAL_TYPE Enumeration Windows-Biometrieframework-API
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
ms.openlocfilehash: ae41693db264308d33bc30191bdb73007b6b2dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859268"
---
# <a name="winbio_credential_type-enumeration"></a>Winbio \_ Credential \_ Type-Enumeration

Definiert Flags, die verwendet werden können, um nach dem Anmelde Informationstyp zu filtern. Diese Enumeration wird von den Funktionen " [**winbiosetcredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)", " [**winbioremovecredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)" und " [**winbiogetkredentialstate**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) " verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_CREDENTIAL_TYPE { 
  WINBIO_CREDENTIAL_PASSWORD  = 0x00000001,
  WINBIO_CREDENTIAL_ALL       = 0xffffffff
} WINBIO_CREDENTIAL_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WINBIO_CREDENTIAL_PASSWORD"></span><span id="winbio_credential_password"></span>**Kennwort für winbio-Anmelde Informationen \_ \_**
</dt> <dd>

Filtert Kenn Wort Anmelde Informationen.

</dd> <dt>

<span id="WINBIO_CREDENTIAL_ALL"></span><span id="winbio_credential_all"></span>**winbio \_ Credential \_ all**
</dt> <dd>

Filtert alle Anmelde Informationen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Enumerationen von Client Anwendungen](client-application-enumerations.md)
</dt> <dt>

[**Winbiogetkredentialstate**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> <dt>

[**Winbioremovecredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
</dt> <dt>

[**Winbiosetcredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

 





