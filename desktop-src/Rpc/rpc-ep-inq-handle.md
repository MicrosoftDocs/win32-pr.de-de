---
title: RPC_EP_INQ_HANDLE (rpcasync. h)
description: Der \_ Datentyp des RPC EP- \_ INQ- \_ Handles deklariert ein Handle für einen Abfrage Kontext. RPC-Anwendungen verwenden Sie, um die in der Endpunkt Zuordnung gespeicherten Server Adressinformationen anzuzeigen.
ms.assetid: e18ce800-0110-4450-9a1b-a3f777d00f2d
keywords:
- RPC_EP_INQ_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c34c64b5601b31485808924fc57dbe3412b6009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392150"
---
# <a name="rpc_ep_inq_handle"></a><span data-ttu-id="e89b7-105">RPC- \_ EP- \_ INQ- \_ handle</span><span class="sxs-lookup"><span data-stu-id="e89b7-105">RPC\_EP\_INQ\_HANDLE</span></span>

<span data-ttu-id="e89b7-106">Der Datentyp des **RPC \_ EP- \_ INQ- \_ Handles** deklariert ein Handle für einen Abfrage Kontext.</span><span class="sxs-lookup"><span data-stu-id="e89b7-106">The **RPC\_EP\_INQ\_HANDLE** data type declares a handle for an inquiry context.</span></span> <span data-ttu-id="e89b7-107">RPC-Anwendungen verwenden Sie, um die in der Endpunkt Zuordnung gespeicherten Server Adressinformationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e89b7-107">RPC applications use it to view server address information stored in the endpoint map.</span></span>


```C++
typedef I_RPC_HANDLE* RPC_EP_INQ_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="e89b7-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e89b7-108">Requirements</span></span>



| <span data-ttu-id="e89b7-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e89b7-109">Requirement</span></span> | <span data-ttu-id="e89b7-110">Wert</span><span class="sxs-lookup"><span data-stu-id="e89b7-110">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e89b7-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e89b7-111">Minimum supported client</span></span><br/> | <span data-ttu-id="e89b7-112">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e89b7-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e89b7-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e89b7-113">Minimum supported server</span></span><br/> | <span data-ttu-id="e89b7-114">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e89b7-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="e89b7-115">Header</span><span class="sxs-lookup"><span data-stu-id="e89b7-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="e89b7-116"><dt>Rpcasync. h (Include RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e89b7-116"><dt>Rpcasync.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e89b7-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e89b7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e89b7-118">**RpcMgmtEpEltInqBegin**</span><span class="sxs-lookup"><span data-stu-id="e89b7-118">**RpcMgmtEpEltInqBegin**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)
</dt> <dt>

[<span data-ttu-id="e89b7-119">**RpcMgmtEpEltInqNext**</span><span class="sxs-lookup"><span data-stu-id="e89b7-119">**RpcMgmtEpEltInqNext**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)
</dt> <dt>

[<span data-ttu-id="e89b7-120">**RpcMgmtEpEltInqDone**</span><span class="sxs-lookup"><span data-stu-id="e89b7-120">**RpcMgmtEpEltInqDone**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone)
</dt> </dl>

 

 





