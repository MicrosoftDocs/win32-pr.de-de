---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: ODJ_POLICY_DNS_DOMAIN_INFO IDL-Definition
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: d0a83ccade72a11449ca0cc9b35b9fc58e9c53d48f8248a9f6074cdb087cc0c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911595"
---
# <a name="odj_policy_dns_domain_info-structure"></a>ODJ_POLICY_DNS_DOMAIN_INFO Struktur

Enthält Informationen über die Domäne und Gesamtstruktur, mit der ein Client verknüpft werden soll.

## <a name="syntax"></a>Syntax

```C++
typedef struct _ODJ_POLICY_DNS_DOMAIN_INFO
{
    ODJ_UNICODE_STRING Name;
    ODJ_UNICODE_STRING DnsDomainName;
    ODJ_UNICODE_STRING DnsForestName;
    GUID DomainGuid;
    PODJ_SID Sid;
} ODJ_POLICY_DNS_DOMAIN_INFO;
```

## <a name="members"></a>Member

### <a name="name"></a>name

Muss auf einen Netbios-Domänennamen festgelegt werden.

### <a name="dnsdomainname"></a>DnsDomainName

Muss auf einen Domänennamen im DNS-Format festgelegt werden.

### <a name="dnsforestname"></a>DnsForestName

Muss auf einen Gesamtstrukturnamen im DNS-Format festgelegt werden.

### <a name="domainguid"></a>DomainGuid

Muss auf die Domänen-GUID festgelegt werden.

### <a name="sid"></a>Sid

Muss auf die Domänen-SID festgelegt werden.

## <a name="see-also"></a>Weitere Informationen

[**IDL-Definitionen für Den Offlinedomänen join**](odj-idl.md)

[**ODJ \_ UNICODE \_ STRING**](odj-odj_unicode_string.md)

[**\_ODJ-SID**](odj-odj_sid.md)
