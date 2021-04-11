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
# <a name="uuid-structure"></a><span data-ttu-id="2fb2a-103">UUID-Struktur</span><span class="sxs-lookup"><span data-stu-id="2fb2a-103">UUID structure</span></span>

<span data-ttu-id="2fb2a-104">Die **UUID** -Struktur definiert einen universell eindeutigen Bezeichner (UUID).</span><span class="sxs-lookup"><span data-stu-id="2fb2a-104">The **UUID** structure defines a Universally Unique Identifier (UUID).</span></span> <span data-ttu-id="2fb2a-105">Eine **UUID** bietet eine eindeutige Bezeichnung für ein Objekt, z. b. eine Schnittstelle, einen Manager-Einstiegspunkt Vektor oder ein Client Objekt.</span><span class="sxs-lookup"><span data-stu-id="2fb2a-105">A **UUID** provides a unique designation of an object such as an interface, a manager entry-point vector, or a client object.</span></span>

<span data-ttu-id="2fb2a-106">Die **UUID** -Struktur ist ein `typedef` Synonym für die [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2fb2a-106">The **UUID** structure is a `typedef`'d synonym for the [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fb2a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fb2a-107">Syntax</span></span>

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a><span data-ttu-id="2fb2a-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fb2a-108">Remarks</span></span>

<span data-ttu-id="2fb2a-109">Die RPC-Laufzeitbibliotheken verwenden **UUID** s, um die Kompatibilität zwischen Clients und Servern zu überprüfen und zwischen mehreren Implementierungen einer Schnittstelle auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="2fb2a-109">The RPC run-time libraries use **UUID** s to check for compatibility between clients and servers, and to select among multiple implementations of an interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fb2a-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fb2a-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2fb2a-111">**Header**</span><span class="sxs-lookup"><span data-stu-id="2fb2a-111">**Header**</span></span> | <span data-ttu-id="2fb2a-112">Definiert in rpcdce. h; RPC. h einschließen</span><span class="sxs-lookup"><span data-stu-id="2fb2a-112">Defined in rpcdce.h; include rpc.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="2fb2a-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fb2a-113">See also</span></span>

<span data-ttu-id="2fb2a-114">[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 [UUID \_ Vektor](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)</span><span class="sxs-lookup"><span data-stu-id="2fb2a-114">[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)
[UUID\_VECTOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)</span></span>