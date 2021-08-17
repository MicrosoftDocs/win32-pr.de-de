---
title: RAS_PPP_IPXCP_RESULT -Struktur (Rassapi.h)
description: Die RAS-STRUKTUR IPXCP RESULT wird verwendet, um das Ergebnis eines IPX-Projektionsvorgang \_ \_ (INTERNETWORK Packet Exchange) für einen Port \_ zu melden.
ms.assetid: e1236e1b-f0ef-46cf-a12f-35529215752c
keywords:
- RAS_PPP_IPXCP_RESULT-Struktur
topic_type:
- apiref
api_name:
- RAS_PPP_IPXCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc79b7700fc47176928688b517377f5e02903da04841b50949937448065086d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789604"
---
# <a name="ras_ppp_ipxcp_result-structure"></a>\_ \_ RAS-RAS-IPXCP-ERGEBNISstruktur \_

\[Die **\_ RAS-IPXCP \_ \_ RESULT-Struktur** wird ab vista Windows unterstützt.\]

Die **\_ RAS-STRUKTUR \_ IPXCP \_ RESULT** wird verwendet, um das Ergebnis eines IPX-Projektionsvorgang (INTERNETWORK Packet Exchange) von HK für einen Port zu melden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _RAS_PPP_IPXCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPXADDRESSLEN + 1];
} RAS_PPP_IPXCP_RESULT;
```



## <a name="members"></a>Member

<dl> <dt>

**dwError**
</dt> <dd>

Gibt die Ergebnisse des IPX-Projektionsvorganges an. Der Wert NO ERROR gibt den Erfolg an. In diesem Fall \_ ist das **wszAddress-Member** gültig. Wenn der Projektionsvorgang nicht erfolgreich war, **ist dwError** ein Fehlercode von Winerror.h oder Raserror.h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Eine auf NULL terminierte Unicode-Zeichenfolge, die die IPX-Adresse angibt, die dem Remoteclient zugewiesen ist. Diese Zeichenfolge verfügt über die *net***.** _Knotenformular._

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

 

 





