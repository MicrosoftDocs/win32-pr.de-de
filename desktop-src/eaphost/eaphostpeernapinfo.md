---
title: EapHostPeerNapInfo-Struktur (Eaphostpeerapis.h)
description: Enthält die Informationen zum Netzwerkzugriffsschutz (Network Access Protection, NAP) zu einer EAP-Suppliplizierung.
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- EapHostPeerNapInfo-Struktur EAPHost
topic_type:
- apiref
api_name:
- EapHostPeerNapInfo
api_location:
- eaphostpeerapis.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fe91c88f633f2e42599938e45e1291c90f1ec9c08559a84f132f3af9269de39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274536"
---
# <a name="eaphostpeernapinfo-structure"></a>EapHostPeerNapInfo-Struktur

Die **EapHostPeerNapInfo-Struktur** enthält die Nap-Informationen (Network Access Protection) zu einer EAP-Supplizierung.

## <a name="syntax"></a>Syntax


```C++
typedef struct _tagEapHostPeerNapInfo {
  ISOLATION_STATE isolationState;
  ProbationTime   probationTime;
  UINT32          stringCorrelationIdLength;
} EapHostPeerNapInfo;
```



## <a name="members"></a>Member

<dl> <dt>

**isolationState**
</dt> <dd>

Eine [**ISOLATION \_ STATE-Struktur,**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) die den NAP-Isolationsstatus eines Computers angibt. Der Isolationszustand bestimmt die Ebene des gewährten Netzwerkzugriffs.

</dd> <dt>

**probationTime**
</dt> <dd>

Eine **ProbationTime-Struktur,** die die Zeit angibt, die erforderlich ist, damit die Verbindung aus der Quarantäne kommt, nach der die Verbindung getrennt wird. Eine **ProbationTime-Struktur** ist mit einer [FILETIME-Struktur](/windows/win32/api/minwinbase/ns-minwinbase-filetime) identisch.

</dd> <dt>

**stringCorrelationIdLength**
</dt> <dd>

Die Länge der [NAP-ZeichenfolgeCorrelationId](/windows/desktop/NAP/nap-datatypes) in Bytes, die dieser Struktur folgt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **EapHostPeerNapInfo-Struktur** geht der [NAP-ZeichenfolgeCorrelationId](/windows/desktop/NAP/nap-datatypes) des **WCHAR-Datentyps** im RPC-Bytestream voran.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                      |
| Header<br/>                   | <dl> <dt>Eaphostpeerapis.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost-Suppliplizierungsstrukturen](eap-host-supplicant-structures.md)
</dt> <dt>

[**EapHostPeerGetAuthStatus**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[**EapHostPeerMethodAuthParams**](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

