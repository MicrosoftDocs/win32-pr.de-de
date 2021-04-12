---
title: ODJ_WIN7BLOB
description: ODJ_WIN7BLOB IDL-Definition
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 2083648636bd58c64314ba22852839f89ed4461d
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104316706"
---
# <a name="odj_win7blob-structure"></a>ODJ_WIN7BLOB Struktur

Enthält die grundlegenden Informationen, die erforderlich sind, um einen Client einer Domäne hinzuzufügen.

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

### <a name="lpdomain"></a>lpdomain

Muss auf den Domänen Namen festgelegt werden.

### <a name="lpmachinename"></a>lpmachinename

Muss auf den Computernamen festgelegt werden.

### <a name="lpmachinepassword"></a>lpmachinepassword

Muss auf ein Klartext-Kennwort für das Computer Konto festgelegt werden, das von lpmachinename identifiziert wird.

### <a name="dnsdomaininfo"></a>Dnsdomaininfo

Enthält Informationen über die Domäne, die verknüpft wird.

### <a name="dcinfo"></a>Dcinfo

Enthält Benennungs-und Adressierungs Informationen über den Domänen Controller, der zum Erstellen des Computer Kontos Active Directory verwendet wurde.

### <a name="options"></a>Optionen

Muss auf 0 (null) festgelegt werden.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)

[**ODJ- \_ Richtlinie \_ DNS- \_ Domänen \_ Informationen**](odj-odj_policy_dns_domain_info.md)

[**DOMAIN_CONTROLLER_INFOW**](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)



