---
title: RAS_PPP_ATCP_RESULT-Struktur (Rassapi.h)
description: Die \_ RASCP \_ ATCP \_ RESULT-Struktur wird verwendet, um das Ergebnis eines AppleTalk-Protokollprojektionsvorgangs für einen Port zu melden.
ms.assetid: ac9df618-f79c-4066-a37e-f92e64e951dd
keywords:
- RAS_PPP_ATCP_RESULT Struktur von RAS
topic_type:
- apiref
api_name:
- RAS_PPP_ATCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa3122026613ba5012f950a98a615dbb8c9ef34133a2a24249fca545eaa2060
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789634"
---
# <a name="ras_ppp_atcp_result-structure"></a>RASCP \_ \_ ATCP \_ RESULT-Struktur

\[Die **\_ RASCP \_ ATCP \_ RESULT-Struktur** wird ab Windows Vista nicht unterstützt.\]

Die **\_ RASCP \_ ATCP \_ RESULT-Struktur** wird verwendet, um das Ergebnis eines AppleTalk-Protokollprojektionsvorgangs für einen Port zu melden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _RAS_PPP_ATCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_ATADDRESSLEN + 1];
} RAS_PPP_ATCP_RESULT;
```



## <a name="members"></a>Member

<dl> <dt>

**dwError**
</dt> <dd>

Gibt einen Wert an, der die Ergebnisse des AppleTalk-Projektionsvorgangs angibt. Der Wert NO \_ ERROR gibt den Erfolg an. In diesem Fall ist der **wszAddress-Member** gültig. Wenn der Projektionsvorgang nicht erfolgreich ist, ist **dwError** ein Fehlercode aus Winerror.h oder Raserror.h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Gibt eine auf NULL endende Unicode-Zeichenfolge an, die die dem Remoteclient zugewiesene IP-Adresse angibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Remotezugriffsdienst (RAS) – Übersicht](about-remote-access-service.md)
</dt> <dt>

[RAS-Serververwaltungsstrukturen](ras-server-administration-structures.md)
</dt> <dt>

[**\_ \_ RAS-PROJEKTIONSERGEBNIS \_**](ras-ppp-projection-result-str.md)
</dt> </dl>

 

 





