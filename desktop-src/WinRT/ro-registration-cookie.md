---
description: Stellt Aktivierungs Factorys dar, die durch Aufrufen der Funktion roregisteractivationfactorys registriert werden.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (roapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe9b5242901c1beff4152bc16108976d6f7de275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348396"
---
# <a name="ro_registration_cookie"></a>Registrierungs Cookie für die \_ Registrierung \_

Stellt Aktivierungs Factorys dar, die durch Aufrufen der Funktion [**roregisteractivationfactorys**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) registriert werden.


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a>Bemerkungen

Die Funktion [**roregisteractivationfactorys**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) gibt ein **\_ Registrierungs \_ Cookie für Registrierungs** stellen zurück, wenn eine aktivierbare Klassenfactorys beim Windows-Runtime registriert sind. Die [**rorevokeactivationfactoryfunktion**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) verwendet das Cookie, um die Klassenfactorys zu entfernen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                     |
| Header<br/>                   | <dl> <dt>Roapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Roregisteractivationfactorys**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[**Rorevokeactivationfactorys**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
