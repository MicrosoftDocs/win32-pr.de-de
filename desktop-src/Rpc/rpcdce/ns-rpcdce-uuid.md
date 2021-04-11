---
title: UUID
description: Stellt eine eindeutige Bezeichnung für ein Objekt, z. b. eine Schnittstelle, einen Manager-Einstiegspunkt Vektor oder ein Client Objekt, bereit.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 95d2d420502a5d92af64c902ffa82c709639d872
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101062"
---
# <a name="uuid-structure"></a>UUID-Struktur

Die **UUID** -Struktur definiert einen universell eindeutigen Bezeichner (UUID). Eine **UUID** bietet eine eindeutige Bezeichnung für ein Objekt, z. b. eine Schnittstelle, einen Manager-Einstiegspunkt Vektor oder ein Client Objekt.

Die **UUID** -Struktur ist ein `typedef` Synonym für die [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) -Struktur.

## <a name="syntax"></a>Syntax

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a>Bemerkungen

Die RPC-Laufzeitbibliotheken verwenden **UUID** s, um die Kompatibilität zwischen Clients und Servern zu überprüfen und zwischen mehreren Implementierungen einer Schnittstelle auszuwählen.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | Definiert in rpcdce. h; RPC. h einschließen |

## <a name="see-also"></a>Siehe auch

[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 [UUID \_ Vektor](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)