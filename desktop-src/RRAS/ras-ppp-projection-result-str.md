---
title: RAS_PPP_PROJECTION_RESULT-Struktur (Rassapi.h)
description: Die \_ \_ RAS-PROJEKTIONSPROJEKTIONSERGEBNIS-Struktur \_ wird verwendet, um die Ergebnisse der verschiedenen PROJEKTIONSIONS-Projektionsvorgänge für einen Port zu melden.
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS_PPP_PROJECTION_RESULT Struktur von RAS
topic_type:
- apiref
api_name:
- RAS_PPP_PROJECTION_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce1bb82b34490f8a1f3734225cbde1e761c575a2019a30db7790bfc7fa3c169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789584"
---
# <a name="ras_ppp_projection_result-structure"></a>\_ \_ \_ RAS-PROJEKTIONSERGEBNISSTRUKTUR

\[Die **\_ RAS-PROJEKTIONSPROJEKTIONSERGEBNIS-Struktur \_ \_** wird ab Windows Vista nicht unterstützt.\]

Die **\_ RAS-PROJEKTIONSPROJEKTIONSERGEBNIS-Struktur \_ \_** wird verwendet, um die Ergebnisse der verschiedenen PROJEKTIONSIONS-Projektionsvorgänge für einen Port zu melden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _RAS_PPP_PROJECTION_RESULT {
  RAS_PPP_NBFCP_RESULT nbf;
  RAS_PPP_IPCP_RESULT  ip;
  RAS_PPP_IPXCP_RESULT ipx;
  RAS_PPP_ATCP_RESULT  at;
} RAS_PPP_PROJECTION_RESULT;
```



## <a name="members"></a>Member

<dl> <dt>

**nbf**
</dt> <dd>

Eine [**RAS \_ \_ NBFCP NBFCP \_ RESULT-Struktur,**](ras-ppp-nbfcp-result-str.md) die das Ergebnis eines NBF-Projektionsvorgangs (ABC NetBEUI Framer) meldet.

</dd> <dt>

**Ip**
</dt> <dd>

Eine [**RAS \_ CSV \_ IPCP \_ RESULT-Struktur,**](ras-ppp-ipcp-result-str.md) die das Ergebnis eines IP-Projektionsvorgangs (INTERNET Protocol) meldet.

</dd> <dt>

**Ipx**
</dt> <dd>

Eine [**\_ \_ RASCP IPXCP \_ RESULT-Struktur,**](ras-ppp-ipxcp-result-str.md) die das Ergebnis eines IPX-Projektionsvorgangs (INTERNETWORK Packet Exchange) meldet.

</dd> <dt>

**at**
</dt> <dd>

EINE [**\_ \_ RAS-ATCP-ATCP-ERGEBNISstruktur. \_**](ras-ppp-atcp-result-str.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur meldet die Projektionsergebnisse für die Protokolle NetBEUI, TCP/IP und IPX. Jede ELEMENTS-Struktur verfügt über einen **dwError-Member,** der angibt, ob die anderen Informationen in der Struktur gültig sind. Wenn **dwError** NO \_ ERROR ist, sind die anderen Informationen gültig. Wenn **dwError** einer der Fehlercodes in Winerror.h oder Raserror.h ist, sind die anderen Informationen ungültig.

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

[**\_RAS-PORT \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_ \_ RAS-PPS-ATCP-ERGEBNIS \_**](ras-ppp-atcp-result-str.md)
</dt> <dt>

[**\_ \_ RAS-CP-IPCP-ERGEBNIS \_**](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[**\_ \_ RAS-IPXCP-ERGEBNIS \_**](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[**\_ \_ RAS-NBFCP-ERGEBNIS \_**](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





