---
title: OP_CERT_PART
description: OP_CERT_PART IDL-Definition
ms.assetid: 30492801-f26e-447f-bcbf-d1108e7ae524
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: feb4f05171204442085f7d69691aa010d13e6042
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "106340541"
---
# <a name="op_cert_part-structure"></a>OP_CERT_PART Struktur

Enthält serialisierte PFX-und Zertifikat Speicher.

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

### <a name="cpfxstores"></a>cpfxstores

Enthält die Anzahl der Elemente in ppfxstores.

### <a name="ppfxstores"></a>ppfxstores

Enthält ein Array von OP_CERT_PFX_STORE Strukturen.

### <a name="csststores"></a>csststores

Enthält die Anzahl der Elemente in psststores.

### <a name="psststores"></a>psststores

Enthält ein Array von OP_CERT_SST_STORE Strukturen.

### <a name="extension"></a>Durchwahl

Für zukünftige Verwendung reserviert und muss alle Nullen enthalten.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)

[**OP- \_ Zertifikat- \_ PFX- \_ Speicher**](odj-op_cert_pfx_store.md)

[**Betriebs \_ Zertifikat- \_ SST- \_ Speicher**](odj-op_cert_sst_store.md)

[**OP- \_ BLOB**](odj-op_blob.md)

