---
title: UUID
description: Stellt eine eindeutige Bezeichnung eines Objekts bereit, z. B. einer Schnittstelle, eines Manager-Einstiegspunktvektors oder eines Clientobjekts.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 31ff8eb22a234020e0da5b5ebb5799d5ddb0c8d1dca7bc094394f79a5ceb0c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925947"
---
# <a name="uuid-structure"></a>UUID-Struktur

Die **UUID-Struktur** definiert einen UUID (Universally Unique Identifier). Eine **UUID** stellt eine eindeutige Bezeichnung eines Objekts bereit, z. B. einer Schnittstelle, eines Manager-Einstiegspunktvektors oder eines Clientobjekts.

Die **UUID-Struktur** ist ein `typedef` 'd Synonym für die [GUID-Struktur.](/windows/win32/api/guiddef/ns-guiddef-guid)

## <a name="syntax"></a>Syntax

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a>Hinweise

Die RPC-Laufzeitbibliotheken verwenden **UUID-Dateien,** um die Kompatibilität zwischen Clients und Servern zu überprüfen und zwischen mehreren Implementierungen einer Schnittstelle auszuwählen.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | Definiert in rpcdce.h; include rpc.h |

## <a name="see-also"></a>Weitere Informationen

[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 [UUID \_ VECTOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)