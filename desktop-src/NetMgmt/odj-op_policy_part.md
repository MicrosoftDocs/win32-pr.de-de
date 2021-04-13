---
title: OP_POLICY_PART
description: OP_POLICY_PART IDL-Definition
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: ef0e3b96ce564ed7ff8e2ce0886e33ca474a1cf8
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104391172"
---
# <a name="op_policy_part-structure"></a><span data-ttu-id="93830-103">OP_POLICY_PART Struktur</span><span class="sxs-lookup"><span data-stu-id="93830-103">OP_POLICY_PART structure</span></span>

<span data-ttu-id="93830-104">Enthält ein Array von OP_POLICY_ELEMENT_LIST Strukturen.</span><span class="sxs-lookup"><span data-stu-id="93830-104">Contains an array of OP_POLICY_ELEMENT_LIST structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="93830-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="93830-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_PART
{
    ULONG                                       cElementLists;
    [size_is(cElementLists)]
                        POP_POLICY_ELEMENT_LIST pElementLists;
    OP_BLOB                                     Extension;
} OP_POLICY_PART, *POP_POLICY_PART;
```

## <a name="members"></a><span data-ttu-id="93830-106">Member</span><span class="sxs-lookup"><span data-stu-id="93830-106">Members</span></span>

### <a name="celementlists"></a><span data-ttu-id="93830-107">celementlists</span><span class="sxs-lookup"><span data-stu-id="93830-107">cElementLists</span></span>

<span data-ttu-id="93830-108">Enthält die Anzahl der Elemente in pelementlists.</span><span class="sxs-lookup"><span data-stu-id="93830-108">Contains the number of elements in pElementLists.</span></span>

### <a name="pelementlists"></a><span data-ttu-id="93830-109">pelementlists</span><span class="sxs-lookup"><span data-stu-id="93830-109">pElementLists</span></span>

<span data-ttu-id="93830-110">Enthält ein Array von OP_POLICY_ELEMENT_LIST Strukturen.</span><span class="sxs-lookup"><span data-stu-id="93830-110">Contains an array of OP_POLICY_ELEMENT_LIST structures.</span></span>

### <a name="extension"></a><span data-ttu-id="93830-111">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="93830-111">Extension</span></span>

<span data-ttu-id="93830-112">Für zukünftige Verwendung reserviert und muss alle Nullen enthalten.</span><span class="sxs-lookup"><span data-stu-id="93830-112">Reserved for future use and must contain all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="93830-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93830-113">See also</span></span>

[<span data-ttu-id="93830-114">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="93830-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="93830-115">**Liste der OP- \_ Richtlinien \_ Elemente \_**</span><span class="sxs-lookup"><span data-stu-id="93830-115">**OP\_POLICY\_ELEMENT\_LIST**</span></span>](odj-op_policy_element_list.md)
