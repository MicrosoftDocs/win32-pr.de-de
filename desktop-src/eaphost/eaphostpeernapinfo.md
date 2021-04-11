---
title: Eaphosteternapinfo-Struktur (eaphostpeer-APIs. h)
description: Enthält die Netzwerk Zugriffsschutz-Informationen (Network Access Protection, NAP) für einen EAP-Supplicant.
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- Eaphosteternapinfo-Struktur EAPHost
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
ms.openlocfilehash: 3221f40dea9e84e410a1a643bbbcdc94e9039b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040924"
---
# <a name="eaphostpeernapinfo-structure"></a>Eaphostpeer-Napinfo-Struktur

Die **eaphostpeernapinfo** -Struktur enthält die Netzwerk Zugriffsschutz-Informationen (Network Access Protection, NAP) für einen EAP-Supplicant.

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

**isolationstate**
</dt> <dd>

Eine [**Isolations \_ Zustands**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) Struktur, die den NAP-Isolations Status eines Computers angibt. Der Isolations Zustand bestimmt die Ebene des gewährten Netzwerk Zugriffs.

</dd> <dt>

**probationtime**
</dt> <dd>

Eine **probationtime** -Struktur, die die Zeit angibt, die benötigt wird, um die Verbindung außerhalb der Quarantäne zu stellen, nach der die Verbindung getrennt wird. Eine **probationtime** -Struktur ist mit einer [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur identisch.

</dd> <dt>

**stringcorrelationidlength**
</dt> <dd>

Die Länge (in Byte) der NAP- [stringcorrelationid](/windows/desktop/NAP/nap-datatypes) , die dieser Struktur folgt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **eaphostpeer-Napinfo** -Struktur ist der NAP- [stringcorrelationid](/windows/desktop/NAP/nap-datatypes) des Datentyps **WCHAR** im RPC-Bytestream vorangestellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                      |
| Header<br/>                   | <dl> <dt>Eaphostpeer-APIs. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost-Supplicant-Strukturen](eap-host-supplicant-structures.md)
</dt> <dt>

[**Eaphostpeergetauthstatus**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[**Eaphostpeer-methodauthparametriams**](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

