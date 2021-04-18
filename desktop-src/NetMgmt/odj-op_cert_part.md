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
# <a name="op_cert_part-structure"></a><span data-ttu-id="7e83e-103">OP_CERT_PART Struktur</span><span class="sxs-lookup"><span data-stu-id="7e83e-103">OP_CERT_PART structure</span></span>

<span data-ttu-id="7e83e-104">Enthält serialisierte PFX-und Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="7e83e-104">Contains serialized PFX and certificate stores.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e83e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e83e-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="7e83e-106">Member</span><span class="sxs-lookup"><span data-stu-id="7e83e-106">Members</span></span>

### <a name="cpfxstores"></a><span data-ttu-id="7e83e-107">cpfxstores</span><span class="sxs-lookup"><span data-stu-id="7e83e-107">cPfxStores</span></span>

<span data-ttu-id="7e83e-108">Enthält die Anzahl der Elemente in ppfxstores.</span><span class="sxs-lookup"><span data-stu-id="7e83e-108">Contains the number of elements in pPfxStores.</span></span>

### <a name="ppfxstores"></a><span data-ttu-id="7e83e-109">ppfxstores</span><span class="sxs-lookup"><span data-stu-id="7e83e-109">pPfxStores</span></span>

<span data-ttu-id="7e83e-110">Enthält ein Array von OP_CERT_PFX_STORE Strukturen.</span><span class="sxs-lookup"><span data-stu-id="7e83e-110">Contains an array of OP_CERT_PFX_STORE structures.</span></span>

### <a name="csststores"></a><span data-ttu-id="7e83e-111">csststores</span><span class="sxs-lookup"><span data-stu-id="7e83e-111">cSstStores</span></span>

<span data-ttu-id="7e83e-112">Enthält die Anzahl der Elemente in psststores.</span><span class="sxs-lookup"><span data-stu-id="7e83e-112">Contains the number of elements in pSstStores.</span></span>

### <a name="psststores"></a><span data-ttu-id="7e83e-113">psststores</span><span class="sxs-lookup"><span data-stu-id="7e83e-113">pSstStores</span></span>

<span data-ttu-id="7e83e-114">Enthält ein Array von OP_CERT_SST_STORE Strukturen.</span><span class="sxs-lookup"><span data-stu-id="7e83e-114">Contains an array of OP_CERT_SST_STORE structures.</span></span>

### <a name="extension"></a><span data-ttu-id="7e83e-115">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="7e83e-115">Extension</span></span>

<span data-ttu-id="7e83e-116">Für zukünftige Verwendung reserviert und muss alle Nullen enthalten.</span><span class="sxs-lookup"><span data-stu-id="7e83e-116">Reserved for future use and must contain all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e83e-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e83e-117">See also</span></span>

[<span data-ttu-id="7e83e-118">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="7e83e-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="7e83e-119">**OP- \_ Zertifikat- \_ PFX- \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="7e83e-119">**OP\_CERT\_PFX\_STORE**</span></span>](odj-op_cert_pfx_store.md)

[<span data-ttu-id="7e83e-120">**Betriebs \_ Zertifikat- \_ SST- \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="7e83e-120">**OP\_CERT\_SST\_STORE**</span></span>](odj-op_cert_sst_store.md)

[<span data-ttu-id="7e83e-121">**OP- \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="7e83e-121">**OP\_BLOB**</span></span>](odj-op_blob.md)

