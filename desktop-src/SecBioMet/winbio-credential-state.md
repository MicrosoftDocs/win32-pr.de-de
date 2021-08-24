---
title: WINBIO_CREDENTIAL_STATE -Enumeration (Winbio \_ types.h)
description: Definiert Werte, die angeben, ob den biometrischen Daten eines Endbenutzers Anmeldeinformationen zugeordnet wurden.
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
keywords:
- WINBIO_CREDENTIAL_STATE enumeration Windows Biometric Framework-API
- PWINBIO_CREDENTIAL_STATE-Enumerationszeiger Windows Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_STATE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce0e176479a68d39b017e852e17a73691b8349d7c6faa6be62130007a09dcef0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868060"
---
# <a name="winbio_credential_state-enumeration"></a>WINBIO \_ CREDENTIAL \_ STATE-Enumeration

Definiert Werte, die angeben, ob den biometrischen Daten eines Endbenutzers Anmeldeinformationen zugeordnet wurden. Diese Enumeration wird von der [**WinBioGetCredentialState-Funktion**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_CREDENTIAL_STATE { 
  WINBIO_CREDENTIAL_NOT_SET  = 0x00000001,
  WINBIO_CREDENTIAL_SET      = 0x00000002
} WINBIO_CREDENTIAL_STATE, *PWINBIO_CREDENTIAL_STATE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**\_WINBIO-ANMELDEINFORMATIONEN \_ NICHT \_ FESTGELEGT**
</dt> <dd>

Dem Endbenutzer wurden Anmeldeinformationen zugeordnet.

</dd> <dt>

<span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**WINBIO \_ CREDENTIAL \_ SET**
</dt> <dd>

Dem Endbenutzer wurden keine Anmeldeinformationen zugeordnet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (einschließlich Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Clientanwendungsenumeration](client-application-enumerations.md)
</dt> <dt>

[**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> </dl>

 

 





