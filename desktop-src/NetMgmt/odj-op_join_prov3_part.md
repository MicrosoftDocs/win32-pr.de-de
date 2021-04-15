---
title: OP_JOINPROV3_PART
description: OP_JOINPROV3_PART IDL-Definition
ms.assetid: 1d8bbfcf-c08e-4bc8-b569-0496703f2d67
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81c8f53f55a8d5a284f969cbde539b0c34406903
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104391169"
---
# <a name="op_joinprov3_part-structure"></a><span data-ttu-id="f5dea-103">OP_JOINPROV3_PART Struktur</span><span class="sxs-lookup"><span data-stu-id="f5dea-103">OP_JOINPROV3_PART structure</span></span>

<span data-ttu-id="f5dea-104">Enthält zusätzliche Informationen, die zum Konfigurieren eines Clients verwendet werden, der einer Domäne hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="f5dea-104">Contains additional information used for configuring a client joined to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5dea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5dea-105">Syntax</span></span>

```C++
typedef struct _OP_JOINPROV3_PART
{
    DWORD Rid;
    [string] wchar_t *lpSid;
} OP_JOINPROV3_PART, *POP_JOINPROV3_PART;
```

## <a name="members"></a><span data-ttu-id="f5dea-106">Member</span><span class="sxs-lookup"><span data-stu-id="f5dea-106">Members</span></span>

### <a name="rid"></a><span data-ttu-id="f5dea-107">Gesagt</span><span class="sxs-lookup"><span data-stu-id="f5dea-107">Rid</span></span>

<span data-ttu-id="f5dea-108">Muss auf den relativen Bezeichner der SID des Computer Kontos festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f5dea-108">Must be set to the Relative Identifier of the machine account’s SID</span></span>

### <a name="lpsid"></a><span data-ttu-id="f5dea-109">lpsid</span><span class="sxs-lookup"><span data-stu-id="f5dea-109">lpSid</span></span>

<span data-ttu-id="f5dea-110">Muss auf die SID des Computer Kontos in Form einer Zeichenfolge festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f5dea-110">Must be set to the SID of the machine account in string form.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5dea-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5dea-111">See also</span></span>

[<span data-ttu-id="f5dea-112">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="f5dea-112">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
