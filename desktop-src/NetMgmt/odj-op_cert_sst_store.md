---
title: OP_CERT_SST_STORE
description: OP_CERT_SST_STORE IDL-Definition
ms.assetid: 6c44756e-29f9-48fc-b678-d2b1f0fb90d4
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 294d21d730e1cce478088cddb43686706217ec5b
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104391300"
---
# <a name="op_cert_sst_store-structure"></a>OP_CERT_SST_STORE Struktur

Enthält einen serialisierten Zertifikat Speicher.

## <a name="syntax"></a>Syntax

```C++
typedef struct _OP_CERT_SST_STORE
{
    ULONG                       StoreLocation;
    [string] wchar_t            *pStoreName;
    ULONG                       cbSst;
    [size_is(cbSst)]    PBYTE   pSst;
} OP_CERT_SST_STORE, *POP_CERT_SST_STORE;
```

## <a name="members"></a>Member

### <a name="storelocation"></a>StoreLocation

Enthält einen Bezeichner für den Zertifikat Speicher der [**System Speicherorte**](../seccrypto/system-store-locations.md).

### <a name="pstorename"></a>pstorename

Enthält den Namen des Stores.

### <a name="cbsst"></a>cbsst

Enthält die Größe des Psst in Bytes.

### <a name="psst"></a>Psst

Enthält einen serialisierten Zertifikat Speicher (siehe [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)