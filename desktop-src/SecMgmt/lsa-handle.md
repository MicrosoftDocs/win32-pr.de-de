---
description: Handle für das lokale Richtlinien Objekt.
ms.assetid: f5878d27-558b-4ef1-9401-1277e740c61d
title: LSA_HANDLE (ntabcapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07bd71a14666dde7bb92e439159a55dd71706612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042315"
---
# <a name="lsa_handle"></a>LSA- \_ handle

Der **LSA- \_ handle** -Datentyp ist ein Handle für das lokale [**Richtlinien**](policy-object.md) Objekt.


```C++
typedef PVOID LSA_HANDLE, *PLSA_HANDLE;
```



## <a name="remarks"></a>Bemerkungen

Bevor Sie die lokale Richtlinien-API verwenden können, muss Ihre Anwendung ein Handle für ein [**Richtlinien**](policy-object.md) Objekt öffnen. Nennen Sie hierzu [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy). Diese Funktion gibt ein Handle zurück, das von der Anwendung in nachfolgenden LSA-Richtlinien Funktionsaufrufen angegeben werden kann.

Jedes Handle verfügt über einen zugeordneten Berechtigungs Satz, mit dem die Vorgänge bestimmt werden, die Ihre Anwendung mit dem Handle für das [**Richtlinien**](policy-object.md) Objekt ausführen kann. Die Anwendung kann jeweils mehr als ein Handle für das **Richtlinien** Objekt öffnen. Wenn ein Handle nicht mehr benötigt wird, sollte die Anwendung es durch Aufrufen von [**lsaclose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)schließen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntabcapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Lsaclose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)
</dt> <dt>

[**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)
</dt> </dl>

 

