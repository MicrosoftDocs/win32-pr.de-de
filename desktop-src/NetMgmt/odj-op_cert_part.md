---
title: OP_CERT_PART
description: OP_CERT_PART IDL-Definition
ms.assetid: 30492801-f26e-447f-bcbf-d1108e7ae524
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 6b8b2bf6a7ebeb8eacdd426d1c8b8bf4ebf22040acffdbcda159a041989d59fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983431"
---
# <a name="op_cert_part-structure"></a>OP_CERT_PART-Struktur

Enthält serialisierte PFX- und Zertifikatspeicher.

## <a name="syntax"></a>Syntax

```C++
typedef struct _OP_CERT_PART
{
    ULONG                                       cPfxStores;
    [size_is(cPfxStores)]   POP_CERT_PFX_STORE  pPfxStores;
    ULONG                                       cSstStores;
    [size_is(cSstStores)]   POP_CERT_SST_STORE  pSstStores;
    OP_BLOB                                     Extension;
} OP_CERT_PART, *POP_CERT_PART;
```

## <a name="members"></a>Member

### <a name="cpfxstores"></a>cPfxStores

Enthält die Anzahl der Elemente in pPfxStores.

### <a name="ppfxstores"></a>pPfxStores

Enthält ein Array von OP_CERT_PFX_STORE Strukturen.

### <a name="csststores"></a>cSstStores

Enthält die Anzahl der Elemente in pSstStores.

### <a name="psststores"></a>pSstStores

Enthält ein Array von OP_CERT_SST_STORE Strukturen.

### <a name="extension"></a>Erweiterung

Für die zukünftige Verwendung reserviert und muss alle Nullen enthalten.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen für den Offlinedomänen-Join**](odj-idl.md)

[**OP \_ CERT \_ PFX \_ STORE**](odj-op_cert_pfx_store.md)

[**OP \_ CERT \_ SST \_ STORE**](odj-op_cert_sst_store.md)

[**\_OP-BLOB**](odj-op_blob.md)

