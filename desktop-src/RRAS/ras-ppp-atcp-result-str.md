---
title: RAS_PPP_ATCP_RESULT Struktur (rassapi. h)
description: Die RAS- \_ PPP- \_ ATCP- \_ Ergebnis Struktur wird verwendet, um das Ergebnis einer AppleTalk-Protokoll Projektions Operation für einen Port zu melden.
ms.assetid: ac9df618-f79c-4066-a37e-f92e64e951dd
keywords:
- RAS_PPP_ATCP_RESULT Struktur-RAS
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
ms.openlocfilehash: 66f3f950af9d5bdde8feef085457a895212ad04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956574"
---
# <a name="ras_ppp_atcp_result-structure"></a>RAS- \_ PPP- \_ ATCP- \_ Ergebnis Struktur

\[Die **RAS- \_ PPP- \_ ATCP- \_ Ergebnis** Struktur wird ab Windows Vista nicht unterstützt.\]

Die **RAS- \_ PPP- \_ ATCP- \_ Ergebnis** Struktur wird verwendet, um das Ergebnis einer AppleTalk-Protokoll Projektions Operation für einen Port zu melden.

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

Gibt einen Wert an, der die Ergebnisse der AppleTalk-Projektions Operation angibt. Der Wert kein \_ Fehler gibt einen Erfolg an. in diesem Fall ist der Member **wszaddress** gültig. Wenn der Projektions Vorgang nicht erfolgreich ist, ist **dwError** ein Fehlercode von "Winerror. h" oder "raserror. h".

</dd> <dt>

**wszaddress**
</dt> <dd>

Gibt eine NULL-terminierte Unicode-Zeichenfolge an, die die dem Remote Client zugewiesene IP-Adresse angibt.

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

[**Ergebnis der RAS- \_ PPP- \_ Projektion \_**](ras-ppp-projection-result-str.md)
</dt> </dl>

 

 





