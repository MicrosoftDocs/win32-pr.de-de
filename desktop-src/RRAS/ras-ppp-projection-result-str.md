---
title: RAS_PPP_PROJECTION_RESULT Struktur (rassapi. h)
description: Die Ergebnis Struktur der RAS- \_ PPP- \_ Projektion \_ wird verwendet, um die Ergebnisse der verschiedenen PPP-Projektions Vorgänge für einen Port zu melden.
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS_PPP_PROJECTION_RESULT Struktur-RAS
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
ms.openlocfilehash: 6a9aa3aef828249b5c72f9e7cdd1bd3b69c96832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741793"
---
# <a name="ras_ppp_projection_result-structure"></a>\_ \_ \_ Ergebnis Struktur der RAS-PPP-Projektion

\[Die **Ergebnis Struktur der RAS- \_ PPP- \_ Projektion \_** wird ab Windows Vista nicht unterstützt.\]

Die **Ergebnis Struktur der RAS- \_ PPP- \_ Projektion \_** wird verwendet, um die Ergebnisse der verschiedenen PPP-Projektions Vorgänge für einen Port zu melden.

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

Eine [**RAS- \_ PPP- \_ NBFCP- \_ Ergebnis**](ras-ppp-nbfcp-result-str.md) Struktur, die das Ergebnis einer PPP-Pipeline mit NetBEUI Framer (NBF) meldet.

</dd> <dt>

**-**
</dt> <dd>

Eine [**RAS- \_ PPP- \_ IPCP- \_ Ergebnis**](ras-ppp-ipcp-result-str.md) Struktur, die das Ergebnis einer PPP-IP (Internet Protocol)-Projektions Operation meldet.

</dd> <dt>

**IPX**
</dt> <dd>

Eine [**RAS- \_ PPP- \_ IPXCP- \_ Ergebnis**](ras-ppp-ipxcp-result-str.md) Struktur, die das Ergebnis eines PPP-IPX-Projektions Vorgangs (Internetwork Packet Exchange) meldet.

</dd> <dt>

**at**
</dt> <dd>

Eine [**RAS- \_ PPP- \_ ATCP- \_ Ergebnis**](ras-ppp-atcp-result-str.md) Struktur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur meldet die Projektions Ergebnisse für NetBEUI-, TCP/IP-und IPX-Protokolle. Jede PPP-Struktur verfügt über einen **dwError** -Member, der angibt, ob die anderen Informationen in der Struktur gültig sind. Wenn **dwError** keinen \_ Fehler hat, sind die anderen Informationen gültig. Wenn **dwError** einer der Fehlercodes in WinError. h oder raserror. h ist, sind die anderen Informationen ungültig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remote Zugriffs Dienst (RAS) (Übersicht)](about-remote-access-service.md)
</dt> <dt>

[RAS-Server-Verwaltungsstrukturen](ras-server-administration-structures.md)
</dt> <dt>

[**RAS- \_ Port \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**Ergebnis des RAS- \_ PPP- \_ ATCP \_**](ras-ppp-atcp-result-str.md)
</dt> <dt>

[**Ergebnis des RAS- \_ PPP- \_ IPCP \_**](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[**Ergebnis der RAS- \_ PPP- \_ IPXCP \_**](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[**RAS- \_ PPP- \_ NBF- \_ Ergebnis**](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[**Rasadminportgetinfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





