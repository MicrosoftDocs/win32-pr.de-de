---
title: RPC_STATUS (rpcdce. h)
description: Der RPC-Status des Datentyps \_ stellt einen plattformspezifischen Status Codetyp dar.
ms.assetid: 0f929916-f3aa-477f-9c61-742f3fbbab29
keywords:
- RPC_STATUS
- RPC_STATUS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066022ce33676caadcf25a6814f3b4974701998e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040574"
---
# <a name="rpc_status"></a><span data-ttu-id="f8c41-105">RPC- \_ Status</span><span class="sxs-lookup"><span data-stu-id="f8c41-105">RPC\_STATUS</span></span>

<span data-ttu-id="f8c41-106">Der RPC- **\_ Status** des Datentyps stellt einen plattformspezifischen Status Codetyp dar.</span><span class="sxs-lookup"><span data-stu-id="f8c41-106">The data type **RPC\_STATUS** represents a platform-specific status code type.</span></span>


```C++
typedef long RPC_STATUS;
typedef unsigned short RPC_STATUS;
```



## <a name="remarks"></a><span data-ttu-id="f8c41-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8c41-107">Remarks</span></span>

<span data-ttu-id="f8c41-108">Der **RPC- \_ statentyp** wird von den meisten RPC-Funktionen zurückgegeben und ist Teil der [**\_ \_ INQ \_ FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) -Funktionstyp Definition für das RPC-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f8c41-108">The **RPC\_STATUS** type is returned by most RPC functions and is part of the [**RPC\_OBJECT\_INQ\_FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) function type definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8c41-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8c41-109">Requirements</span></span>



| <span data-ttu-id="f8c41-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8c41-110">Requirement</span></span> | <span data-ttu-id="f8c41-111">Wert</span><span class="sxs-lookup"><span data-stu-id="f8c41-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c41-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8c41-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f8c41-113">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8c41-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f8c41-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8c41-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f8c41-115">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8c41-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f8c41-116">Header</span><span class="sxs-lookup"><span data-stu-id="f8c41-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8c41-117"><dt>Rpcdce. h (Include RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8c41-117"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8c41-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8c41-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8c41-119">**RPC- \_ Objekt \_ INQ \_ FN**</span><span class="sxs-lookup"><span data-stu-id="f8c41-119">**RPC\_OBJECT\_INQ\_FN**</span></span>](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)
</dt> </dl>

 

 





