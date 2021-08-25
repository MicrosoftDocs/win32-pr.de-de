---
title: ODJ_WIN7BLOB
description: ODJ_WIN7BLOB IDL-Definition
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: ab6f6582b23d6e65866ba1380b696fab6d8313578fab47ad5dda999b09a1caa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911594"
---
# <a name="odj_win7blob-structure"></a>ODJ_WIN7BLOB-Struktur

Enthält die grundlegenden Informationen, die zum Hinzufügen eines Clients zu einer Domäne erforderlich sind.

## <a name="syntax"></a>Syntax

```C++
typedef struct _ODJ_WIN7BLOB
{
    [string] wchar_t *lpDomain;
    [string] wchar_t *lpMachineName;
    [string] wchar_t *lpMachinePassword;
    ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
    DOMAIN_CONTROLLER_INFOW DcInfo;
    DWORD Options;
} ODJ_WIN7BLOB;
```

## <a name="members"></a>Member

### <a name="lpdomain"></a>lpDomain

Muss auf den Domänennamen festgelegt werden.

### <a name="lpmachinename"></a>lpMachineName

Muss auf den Computernamen festgelegt werden.

### <a name="lpmachinepassword"></a>lpMachinePassword

Muss auf ein Klartextkennwort für das computerkonto festgelegt werden, das durch lpMachineName identifiziert wird.

### <a name="dnsdomaininfo"></a>DnsDomainInfo

Enthält Informationen über die Domäne, die verknüpft wird.

### <a name="dcinfo"></a>DcInfo

Enthält Benennungs- und Adressierungsinformationen zum Domänencontroller, der zum Erstellen des Computerkontos Active Directory verwendet wurde.

### <a name="options"></a>Optionen

Muss auf 0 (null) festgelegt werden.

## <a name="see-also"></a>Weitere Informationen

[**IDL-Definitionen für Den Offlinedomänen join**](odj-idl.md)

[**\_ \_ DNS-DOMÄNENINFORMATIONEN DER ODJ-RICHTLINIE \_ \_**](odj-odj_policy_dns_domain_info.md)

[**DOMAIN_CONTROLLER_INFOW**](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)



