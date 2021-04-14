---
title: RAS_PPP_IPCP_RESULT Struktur (rassapi. h)
description: Die RAS \_ \_ -PPP-IPCP \_ -Ergebnis Struktur wird verwendet, um das Ergebnis einer PPP-IP (Internet Protocol)-Projektions Operation für einen Port zu melden.
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
ms.openlocfilehash: eedcd7c7390e01849371eee2cbb24ffa2593900d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517879"
---
# <a name="ras_ppp_ipcp_result-structure"></a>RAS- \_ PPP- \_ IPCP- \_ Ergebnis Struktur

\[Die **RAS- \_ PPP- \_ IPCP- \_ Ergebnis** Struktur wird ab Windows Vista nicht unterstützt.\]

Die **RAS- \_ PPP- \_ IPCP- \_ Ergebnis** Struktur wird verwendet, um das Ergebnis einer PPP-IP (Internet Protocol)-Projektions Operation für einen Port zu melden.

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

Gibt die Ergebnisse des IP-Projektions Vorgangs an. Der Wert kein \_ Fehler gibt einen Erfolg an. in diesem Fall ist der Member **wszaddress** gültig. Wenn der Projektions Vorgang nicht erfolgreich war, ist **dwError** ein Fehlercode aus "Winerror. h" oder "raserror. h".

</dd> <dt>

**wszaddress**
</dt> <dd>

Eine NULL-terminierte Unicode-Zeichenfolge, die die dem Remote Client zugewiesene IP-Adresse angibt. Diese Zeichenfolge hat die Form *a ***.** _b_* _._ *_c_*_._ * _d_.

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

 

 





