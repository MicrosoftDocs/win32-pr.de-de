---
title: OP_PACKAGE_PART_COLLECTION
description: OP_PACKAGE_PART_COLLECTION IDL-Definition
ms.assetid: a7abf011-0335-4869-b4d9-144b2f392241
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8eb61397045a382fe5933025a4eeda2f563e838
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104039795"
---
# <a name="op_package_part_collection-structure"></a><span data-ttu-id="9af3c-103">OP_PACKAGE_PART_COLLECTION Struktur</span><span class="sxs-lookup"><span data-stu-id="9af3c-103">OP_PACKAGE_PART_COLLECTION structure</span></span>

<span data-ttu-id="9af3c-104">Gibt eine-Struktur an, die ein Array von OP_PACKAGE_PART-Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="9af3c-104">Specifies a structure that contains an array of OP_PACKAGE_PART structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="9af3c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9af3c-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE_PART_COLLECTION
{
    ULONG                                 cParts;
    [size_is(cParts)]   POP_PACKAGE_PART  pParts;
    OP_BLOB                               Extension;
} OP_PACKAGE_PART_COLLECTION, *POP_PACKAGE_PART_COLLECTION;
```

## <a name="members"></a><span data-ttu-id="9af3c-106">Member</span><span class="sxs-lookup"><span data-stu-id="9af3c-106">Members</span></span>

### <a name="cparts"></a><span data-ttu-id="9af3c-107">cparts</span><span class="sxs-lookup"><span data-stu-id="9af3c-107">cParts</span></span>

<span data-ttu-id="9af3c-108">Enthält die Anzahl der Elemente in pparts.</span><span class="sxs-lookup"><span data-stu-id="9af3c-108">Contains the number of elements in pParts.</span></span>

### <a name="pparts"></a><span data-ttu-id="9af3c-109">pparts</span><span class="sxs-lookup"><span data-stu-id="9af3c-109">pParts</span></span>

<span data-ttu-id="9af3c-110">Enthält ein Array von OP_PACKAGE_PART Strukturen.</span><span class="sxs-lookup"><span data-stu-id="9af3c-110">Contains an array of OP_PACKAGE_PART structures.</span></span>

### <a name="extension"></a><span data-ttu-id="9af3c-111">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="9af3c-111">Extension</span></span>

<span data-ttu-id="9af3c-112">Für zukünftige Verwendung reserviert und muss auf alle Nullen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9af3c-112">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="9af3c-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9af3c-113">See also</span></span>

[<span data-ttu-id="9af3c-114">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="9af3c-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="9af3c-115">**OP \_ - \_ Paketteil**</span><span class="sxs-lookup"><span data-stu-id="9af3c-115">**OP\_PACKAGE\_PART**</span></span>](odj-op_package_part.md)

[<span data-ttu-id="9af3c-116">**OP- \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="9af3c-116">**OP\_BLOB**</span></span>](odj-op_blob.md)

