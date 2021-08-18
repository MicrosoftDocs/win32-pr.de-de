---
title: RAS_PPP_IPCP_RESULT -Struktur (Rassapi.h)
description: Die RAS HK IPCP RESULT-Struktur wird verwendet, um das Ergebnis eines IP-Projektionsvorgang \_ \_ \_ (INTERNET Protocol, INTERNET PROTOCOL) für einen Port zu melden.
ms.assetid: edbdc8f2-ba56-4d34-8908-f7eccc2ebf61
keywords:
- RAS_PPP_IPCP_RESULT Struktur-RAS
topic_type:
- apiref
api_name:
- RAS_PPP_IPCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa0425289b7ffd686f0d908f9789a2c24606978f37e05dfada5b937b8ce05b21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789614"
---
# <a name="ras_ppp_ipcp_result-structure"></a>\_RAS-HK \_ IPCP \_ RESULT-Struktur

\[Die **\_ RAS-IPCP-IPCP \_ \_ RESULT-Struktur** wird ab Windows Vista nicht unterstützt.\]

Die **RAS \_ HK \_ IPCP \_ RESULT-Struktur** wird verwendet, um das Ergebnis eines IP-Projektionsvorgang (INTERNET Protocol, INTERNET PROTOCOL) für einen Port zu melden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _RAS_PPP_IPCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPADDRESSLEN + 1];
} RAS_PPP_IPCP_RESULT;
```



## <a name="members"></a>Member

<dl> <dt>

**dwError**
</dt> <dd>

Gibt die Ergebnisse des IP-Projektionsvorgang an. Der Wert NO ERROR gibt den Erfolg an. In diesem Fall \_ ist das **wszAddress-Member** gültig. Wenn der Projektionsvorgang nicht erfolgreich war, **ist dwError** ein Fehlercode von Winerror.h oder Raserror.h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Eine auf NULL terminierte Unicode-Zeichenfolge, die die IP-Adresse angibt, die dem Remoteclient zugewiesen ist. Diese Zeichenfolge hat das Formular *a***.** _b_* _._ *_c_*_._ * _d_.

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

 

 





