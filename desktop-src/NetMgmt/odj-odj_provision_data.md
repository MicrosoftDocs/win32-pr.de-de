---
title: ODJ_PROVISION_DATA
description: ODJ_PROVISION_DATA IDL-Definition
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f07d8c200103fa21afc080c60157645fe6730766
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "106339523"
---
# <a name="odj_provision_data-structure"></a><span data-ttu-id="9755c-103">ODJ_PROVISION_DATA Struktur</span><span class="sxs-lookup"><span data-stu-id="9755c-103">ODJ_PROVISION_DATA structure</span></span>

<span data-ttu-id="9755c-104">Gibt die äußerste Serialisierungsstruktur an, die von den Offline-Domänen Beitritt-APIs</span><span class="sxs-lookup"><span data-stu-id="9755c-104">Specifies the outermost serialization structure used by the offline domain join apis.</span></span>

## <a name="syntax"></a><span data-ttu-id="9755c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9755c-105">Syntax</span></span>

```C++
typedef struct _ODJ_PROVISION_DATA
{
    ULONG ulVersion;
    ULONG ulcBlobs;
    [size_is(ulcBlobs)] PODJ_BLOB pBlobs;
} ODJ_PROVISION_DATA;
```

## <a name="members"></a><span data-ttu-id="9755c-106">Member</span><span class="sxs-lookup"><span data-stu-id="9755c-106">Members</span></span>

### <a name="ulversion"></a><span data-ttu-id="9755c-107">ulversion</span><span class="sxs-lookup"><span data-stu-id="9755c-107">ulVersion</span></span>

<span data-ttu-id="9755c-108">Diese muss auf 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9755c-108">This must be set to 1.</span></span>

### <a name="ulcblobs"></a><span data-ttu-id="9755c-109">ulcblosb</span><span class="sxs-lookup"><span data-stu-id="9755c-109">ulcBlobs</span></span>

<span data-ttu-id="9755c-110">Dies muss auf die Anzahl der Elemente im pblobarray festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9755c-110">This must be set to the number of elements in the pBlobs array.</span></span>

### <a name="pblobs"></a><span data-ttu-id="9755c-111">pblobcontainer</span><span class="sxs-lookup"><span data-stu-id="9755c-111">pBlobs</span></span>

<span data-ttu-id="9755c-112">Verweist auf ein Array von ODJ_BLOB Strukturen.</span><span class="sxs-lookup"><span data-stu-id="9755c-112">Points to an array of ODJ_BLOB structures.</span></span>

## <a name="see-also"></a><span data-ttu-id="9755c-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9755c-113">See also</span></span>

[<span data-ttu-id="9755c-114">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="9755c-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="9755c-115">**ODJ- \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="9755c-115">**ODJ\_BLOB**</span></span>](odj-odj_blob.md)


