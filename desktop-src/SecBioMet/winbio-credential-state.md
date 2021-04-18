---
title: WINBIO_CREDENTIAL_STATE-Enumeration (winbio \_ types. h)
description: Definiert Werte, die angeben, ob den biometrischen Daten eines Endbenutzers Anmelde Informationen zugeordnet wurden.
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
keywords:
- WINBIO_CREDENTIAL_STATE Enumeration Windows-Biometrieframework-API
- PWINBIO_CREDENTIAL_STATE enumerationszeiger Windows-Biometrieframework-API
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
ms.openlocfilehash: 3f8b8292cbbaefeeda0f6bf349f55e8f825f1756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340427"
---
# <a name="winbio_credential_state-enumeration"></a>Winbio \_ Credential \_ State-Enumeration

Definiert Werte, die angeben, ob den biometrischen Daten eines Endbenutzers Anmelde Informationen zugeordnet wurden. Diese Enumeration wird von der [**winbiogetkredentialstate**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) -Funktion verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_CREDENTIAL_STATE { 
  WINBIO_CREDENTIAL_NOT_SET  = 0x00000001,
  WINBIO_CREDENTIAL_SET      = 0x00000002
} WINBIO_CREDENTIAL_STATE, *PWINBIO_CREDENTIAL_STATE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**winbio-Anmelde Informationen \_ \_ nicht \_ festgelegt**
</dt> <dd>

Dem Endbenutzer wurden Anmelde Informationen zugeordnet.

</dd> <dt>

<span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**winbio-Anmelde Informationen \_ \_ Satz**
</dt> <dd>

Dem Endbenutzer wurden keine Anmelde Informationen zugeordnet.

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
</dt> </dl>

 

 





