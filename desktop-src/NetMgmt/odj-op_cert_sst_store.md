---
title: OP_CERT_SST_STORE
description: OP_CERT_SST_STORE IDL-Definition
ms.assetid: 6c44756e-29f9-48fc-b678-d2b1f0fb90d4
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 4104635ea845394251f28eea48a2b3c67063826f98dd4da71a8f9adda8fd14a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911550"
---
# <a name="op_cert_sst_store-structure"></a>OP_CERT_SST_STORE Struktur

Enthält einen serialisierten Zertifikatspeicher.

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

Enthält einen Bezeichner für den Zertifikatspeicher aus [**System Store Speicherorte.**](../seccrypto/system-store-locations.md)

### <a name="pstorename"></a>pStoreName

Enthält den Namen des Speichers.

### <a name="cbsst"></a>cbSst

Enthält die Größe von pSst in Bytes.

### <a name="psst"></a>Psst

Enthält einen serialisierten Zertifikatspeicher (siehe [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).

## <a name="see-also"></a>Weitere Informationen

[**IDL-Definitionen für Den Offlinedomänen join**](odj-idl.md)