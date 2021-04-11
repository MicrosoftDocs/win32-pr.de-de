---
title: RAS_PPP_IPXCP_RESULT Struktur (rassapi. h)
description: Die RAS- \_ PPP- \_ IPXCP- \_ Ergebnis Struktur wird verwendet, um das Ergebnis einer PPP-IPX-Projektions Operation (Internetwork Packet Exchange) für einen Port zu melden.
ms.assetid: e1236e1b-f0ef-46cf-a12f-35529215752c
keywords:
- RAS_PPP_IPXCP_RESULT Struktur-RAS
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
ms.openlocfilehash: 5bb7ca4d006bd1a1df5a645799998b463c0b14f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040684"
---
# <a name="ras_ppp_ipxcp_result-structure"></a>RAS- \_ PPP- \_ IPXCP- \_ Ergebnis Struktur

\[Die **RAS- \_ PPP- \_ IPXCP- \_ Ergebnis** Struktur wird ab Windows Vista nicht unterstützt.\]

Die **RAS- \_ PPP- \_ IPXCP- \_ Ergebnis** Struktur wird verwendet, um das Ergebnis einer PPP-IPX-Projektions Operation (Internetwork Packet Exchange) für einen Port zu melden.

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

Gibt die Ergebnisse der IPX-Projektions Operation an. Der Wert kein \_ Fehler gibt einen Erfolg an. in diesem Fall ist der Member **wszaddress** gültig. Wenn der Projektions Vorgang nicht erfolgreich war, ist **dwError** ein Fehlercode aus "Winerror. h" oder "raserror. h".

</dd> <dt>

**wszaddress**
</dt> <dd>

Eine NULL-terminierte Unicode-Zeichenfolge, die die dem Remote Client zugewiesene IPX-Adresse angibt. Diese Zeichenfolge weist das * NET * auf **.** _Knoten_ Formular.

</dd> </dl>

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

[**Ergebnis der RAS- \_ PPP- \_ Projektion \_**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**Rasadminportgetinfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





