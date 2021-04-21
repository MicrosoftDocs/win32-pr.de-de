---
UID: NS:directml.DML_SCALAR_UNION
title: DML_SCALAR_UNION
description: Eine Vereinigung von skalaren Typen.
helpviewer_keywords:
- DML_SCALAR_UNION
- DML_SCALAR_UNION structure
- direct3d12.dml_scalar_union
- directml/DML_SCALAR_UNION
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
ms.keywords: DML_SCALAR_UNION, DML_SCALAR_UNION structure, direct3d12.dml_scalar_union, directml/DML_SCALAR_UNION
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_SCALAR_UNION
- directml/DML_SCALAR_UNION
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_SCALAR_UNION
ms.openlocfilehash: d53ec7025d3da5a07a648849e366d436755ad3f1
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803945"
---
# <a name="dml_scalar_union-union-directmlh"></a>DML_SCALAR_UNION Union (directml.h)
Eine Vereinigung von skalaren Typen.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

## <a name="syntax"></a>Syntax
```cpp
union DML_SCALAR_UNION {
  BYTE   Bytes[8];
  INT8   Int8;
  UINT8  UInt8;
  INT16  Int16;
  UINT16 UInt16;
  INT32  Int32;
  UINT32 UInt32;
  INT64  Int64;
  UINT64 UInt64;
  FLOAT  Float32;
  DOUBLE Float64;
};
```



## <a name="members"></a>Member

`Bytes`

Ein 8-Byte-Array.


`Int8`

Eine 8-Bit-Ganzzahl mit Vorzeichen.


`UInt8`

Eine 8-Bit-Ganzzahl ohne Vorzeichen.


`Int16`

Eine 16-Bit-Ganzzahl mit Vorzeichen.


`UInt16`

Eine 16-Bit-Ganzzahl ohne Vorzeichen.


`Int32`

Eine 32-Bit-Ganzzahl mit Vorzeichen.


`UInt32`

Eine 32-Bit-Ganzzahl ohne Vorzeichen.


`Int64`

Eine 64-Bit-Ganzzahl mit Vorzeichen.


`UInt64`

Eine 64-Bit-Ganzzahl ohne Vorzeichen.


`Float32`

Eine Gleitkommazahl mit einfacher Genauigkeit.


`Float64`

Eine Gleitkommazahl mit doppelter Genauigkeit.



## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |