---
description: Stellt Aktivierungs factorys dar, die durch Aufrufen der RoRegisterActivationFactories-Funktion registriert werden.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (Roapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8efc7d3364f02c11750e6b42ddec6d2a3dee3f83368d277bc979a22ea3a0854a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741597"
---
# <a name="ro_registration_cookie"></a>\_ \_ RO-REGISTRIERUNGSCOOKIE

Stellt Aktivierungs factorys dar, die durch Aufrufen der [**RoRegisterActivationFactories-Funktion registriert**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) werden.


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a>Hinweise

Die [**RoRegisterActivationFactories-Funktion**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) gibt ein **RO REGISTRATION \_ \_ COOKIE** zurück, wenn eine aktivierbare Klassen factorys bei der Windows werden. Die [**RoRevokeActivationFactories-Funktion**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) verwendet das Cookie, um die Klassen factorys zu entfernen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                     |
| Header<br/>                   | <dl> <dt>Roapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
