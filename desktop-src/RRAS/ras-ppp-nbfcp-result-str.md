---
title: RAS_PPP_NBFCP_RESULT Struktur (rassapi. h)
description: Die RAS- \_ PPP- \_ NBFCP- \_ Ergebnis Struktur wird verwendet, um das Ergebnis einer PPP-NetBEUI Framer (NBF)-Projektions Operation für einen Port zu melden.
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS_PPP_NBFCP_RESULT Struktur-RAS
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
ms.openlocfilehash: ddcb1cfe28a72e390cedbcc35fa299dddbfb8634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104000"
---
# <a name="ras_ppp_nbfcp_result-structure"></a>RAS- \_ PPP- \_ NBF- \_ Ergebnis Struktur

\[Die **RAS- \_ PPP- \_ NBS-Ergebnisstruktur \_** wird ab Windows Vista nicht unterstützt.\]

Die **RAS- \_ PPP- \_ NBFCP- \_ Ergebnis** Struktur wird verwendet, um das Ergebnis einer PPP-NetBEUI Framer (NBF)-Projektions Operation für einen Port zu melden.

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

Gibt die Ergebnisse der NBF-Projektions Operation an. Der Wert kein \_ Fehler weist auf einen Erfolg hin. in diesem Fall enthält das Element **wszwksta** den Namen des Remote Computers. Wenn der Projektions Vorgang nicht erfolgreich war, ist **dwError** ein Fehlercode aus "Winerror. h" oder "raserror. h".

</dd> <dt>

**dwnetbioserror**
</dt> <dd>

Diesen Member auf dem Server ignorieren; Sie ist nur auf dem Client relevant.

</dd> <dt>

**szName**
</dt> <dd>

Diesen Member auf dem Server ignorieren; Sie ist nur auf dem Client relevant.

</dd> <dt>

**wszwksta**
</dt> <dd>

Eine NULL-terminierte Unicode-Zeichenfolge, die den NetBIOS-Namen der RAS-Client Arbeitsstation angibt.

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

 

 





