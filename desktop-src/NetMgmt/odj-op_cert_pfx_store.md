---
title: OP_CERT_PFX_STORE
description: OP_CERT_PFX_STORE IDL-Definition
ms.assetid: 10773feb-623c-4256-a973-f006ed66d936
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 28e8b9e1a6d73f3d93e1700f812b21a0edf21982b7d5b9c927f4e7391b961850
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911540"
---
# <a name="op_cert_pfx_store-structure"></a>OP_CERT_PFX_STORE-Struktur

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

### <a name="ptemplatename"></a>pTemplateName

Muss auf den Namen der Zertifikatvorlage festgelegt werden, die zum Erstellen des Zertifikats verwendet wird.

### <a name="ulprivatekeyexportpolicy"></a>ulPrivateKeyExportPolicy

Enthält einen Wert aus der [**X509PrivateKeyExportFlags-Enumeration.**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags)

### <a name="ppolicyserverurl"></a>pPolicyServerUrl

Muss die URL des Richtlinienservers festgelegt werden.

### <a name="ulpolicyserverurlflags"></a>ulPolicyServerUrlFlags

Enthält einen Wert aus der [**PolicyServerUrlFlags-Enumeration.**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags)

### <a name="ppolicyserverid"></a>pPolicyServerId

Enthält eine Zeichenfolge, die den Richtlinienserver eindeutig identifiziert.

### <a name="cbpfx"></a>cbPfx

Enthält die Größe von pPfx in Bytes.

### <a name="ppfx"></a>pPfx

Enthält eine serialisierte PFX-Struktur (siehe [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).

## <a name="see-also"></a>Weitere Informationen

[**IDL-Definitionen für den Offlinedomänen-Join**](odj-idl.md)
