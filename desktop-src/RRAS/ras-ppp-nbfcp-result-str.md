---
title: RAS_PPP_NBFCP_RESULT -Struktur (Rassapi.h)
description: Die RAS NBFCP RESULT-Struktur wird verwendet, um das Ergebnis eines NBF-Projektionsvorgang \_ \_ \_ (HK NetBEUI Framer) für einen Port zu melden.
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS_PPP_NBFCP_RESULT-Struktur
topic_type:
- apiref
api_name:
- RAS_PPP_NBFCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e415e6aea75dcf78d19d776e4df0a6edf704db473eacf0c8ddbb366ffbf65947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789594"
---
# <a name="ras_ppp_nbfcp_result-structure"></a>RAS \_ \_ NBFCP \_ RESULT-Struktur

\[Die **RAS \_ \_ NBFCP \_ RESULT-Struktur** wird ab vista Windows unterstützt.\]

Die **RAS \_ \_ NBFCP \_ RESULT-Struktur** wird verwendet, um das Ergebnis eines NBF-Projektionsvorgang (HK NetBEUI Framer) für einen Port zu melden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _RAS_PPP_NBFCP_RESULT {
  DWORD dwError;
  DWORD dwNetBiosError;
  CHAR  szName[NETBIOS_NAME_LEN + 1];
  WCHAR wszWksta[NETBIOS_NAME_LEN + 1];
} RAS_PPP_NBFCP_RESULT;
```



## <a name="members"></a>Member

<dl> <dt>

**dwError**
</dt> <dd>

Gibt die Ergebnisse des NBF-Projektionsvorgang an. Der Wert NO ERROR gibt den Erfolg an. In diesem Fall enthält das \_ **wszWksta-Member** den Namen des Remotecomputers. Wenn der Projektionsvorgang nicht erfolgreich war, **ist dwError** ein Fehlercode von Winerror.h oder Raserror.h.

</dd> <dt>

**dwNetBiosError**
</dt> <dd>

Ignorieren Sie diesen Member auf dem Server. sie ist nur auf dem Client relevant.

</dd> <dt>

**Szname**
</dt> <dd>

Ignorieren Sie diesen Member auf dem Server. sie ist nur auf dem Client relevant.

</dd> <dt>

**wszWksta**
</dt> <dd>

Eine auf NULL beendete Unicode-Zeichenfolge, die den NetBIOS-Namen der RAS-Clientarbeitsstation angibt.

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

[Ras-Dienst (RAS): Übersicht](about-remote-access-service.md)
</dt> <dt>

[RAS-Serververwaltungsstrukturen](ras-server-administration-structures.md)
</dt> <dt>

[**\_RAS-PORT \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_ \_ RAS-PROJEKTIONSERGEBNIS \_**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





