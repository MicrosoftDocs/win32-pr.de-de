---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: ODJ_POLICY_DNS_DOMAIN_INFO IDL-Definition
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 36b7759451811844a91b3ee66ff3460fa4c4db34
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "103734689"
---
# <a name="odj_policy_dns_domain_info-structure"></a>ODJ_POLICY_DNS_DOMAIN_INFO Struktur

Enthält Informationen über die Domäne und die Gesamtstruktur, mit denen ein Client verknüpft werden soll.

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

Muss auf einen NetBIOS-Domänen Namen festgelegt werden.

### <a name="dnsdomainname"></a>DnsDomainName

Muss auf einen Domänen Namen im DNS-Format festgelegt werden.

### <a name="dnsforestname"></a>DnsForestName

Muss im DNS-Format auf einen Gesamtstruktur Namen festgelegt werden.

### <a name="domainguid"></a>Domainguid

Muss auf die Domänen-GUID festgelegt werden.

### <a name="sid"></a>Sid

Muss auf die Domänen-SID festgelegt werden.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)

[**ODJ- \_ Unicode- \_ Zeichenfolge**](odj-odj_unicode_string.md)

[**ODJ- \_ sid**](odj-odj_sid.md)
