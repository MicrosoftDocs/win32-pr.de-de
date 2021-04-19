---
title: OP_CERT_PFX_STORE
description: OP_CERT_PFX_STORE IDL-Definition
ms.assetid: 10773feb-623c-4256-a973-f006ed66d936
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: b07d0b8e5572763cc42fe2f5b19a4dde2cfe2157
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "106341566"
---
# <a name="op_cert_pfx_store-structure"></a>OP_CERT_PFX_STORE Struktur

Enthält eine serialisierte PFX-Struktur.

## <a name="syntax"></a>Syntax

```C++
typedef struct _OP_CERT_PFX_STORE
{
    [string] wchar_t            *pTemplateName;
    ULONG                       ulPrivateKeyExportPolicy;
    [string] wchar_t            *pPolicyServerUrl;
    ULONG                       ulPolicyServerUrlFlags;
    [string] wchar_t            *pPolicyServerId;
    ULONG                       cbPfx;
    [size_is(cbPfx)]    PBYTE   pPfx;
} OP_CERT_PFX_STORE, *POP_CERT_PFX_STORE;
```

## <a name="members"></a>Member

### <a name="ptemplatename"></a>ptemplatename

Muss auf den Namen der Zertifikat Vorlage festgelegt werden, die zum Erstellen des Zertifikats verwendet wurde.

### <a name="ulprivatekeyexportpolicy"></a>ulprivatekeyexportpolicy

Enthält einen Wert aus der [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) -Enumeration.

### <a name="ppolicyserverurl"></a>pPolicyServerUrl

Muss die URL des Richtlinien Servers festgelegt werden.

### <a name="ulpolicyserverurlflags"></a>ulPolicyServerUrlFlags

Enthält einen Wert aus der [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) -Enumeration.

### <a name="ppolicyserverid"></a>ppolicyserverid

Enthält eine Zeichenfolge, die den Richtlinien Server eindeutig identifiziert.

### <a name="cbpfx"></a>cbpfx

Enthält die Größe von ppfx in Bytes.

### <a name="ppfx"></a>ppfx

Enthält eine serialisierte PFX-Struktur (siehe [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)
