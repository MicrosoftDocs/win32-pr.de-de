---
title: Rpctryaußer (RPC. h)
description: Die rpctryaußer-Anweisung stellt eine strukturierte Ausnahmebehandlung für RPC-Anwendungen bereit.
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- Rpctryaußer RPC
topic_type:
- apiref
api_name:
- RpcTryExcept
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5876a3fe0b33f96a5e10a9c712bdcadcbfca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104378"
---
# <a name="rpctryexcept"></a><span data-ttu-id="56093-104">Rpctryaußer</span><span class="sxs-lookup"><span data-stu-id="56093-104">RpcTryExcept</span></span>

<span data-ttu-id="56093-105">Die **rpctryaußer** -Anweisung stellt eine strukturierte Ausnahmebehandlung für RPC-Anwendungen bereit.</span><span class="sxs-lookup"><span data-stu-id="56093-105">The **RpcTryExcept** statement provides structured exception handling for RPC applications.</span></span> <span data-ttu-id="56093-106">Wenn eine der Programm Anweisungen in **rpctryaußer** eine Ausnahme auslöst, werden die Anweisungen im Code Block " [**rpcaußer**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) " ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56093-106">If any of the program statements in the **RpcTryExcept** cause an exception, the statements in the [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) code block are executed.</span></span> <span data-ttu-id="56093-107">Alle **rpctryaußer** -Anweisungen müssen von der [**rpcendexcept**](/previous-versions/aa375629(v=vs.80)) -Anweisung beendet werden.</span><span class="sxs-lookup"><span data-stu-id="56093-107">All **RpcTryExcept** statements must be terminated by the [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) statement.</span></span>

<span data-ttu-id="56093-108">Weitere Informationen finden Sie unter [**rpcaußer**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span><span class="sxs-lookup"><span data-stu-id="56093-108">For more information, see [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span></span>

<span data-ttu-id="56093-109">**Windows Vista und höhere Versionen von Windows:**  [**rpcexceptionfilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) wird für die strukturierte Ausnahmebehandlung für die häufigsten Ausnahmen als Alternative zu benutzerdefinierten Filtern mit " [**rpcaußer**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)" empfohlen.</span><span class="sxs-lookup"><span data-stu-id="56093-109">**Windows Vista and later versions of Windows:**  [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) is recommended for structured exception handling for the most common exceptions as an alternative to custom filters with [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span></span>

## <a name="requirements"></a><span data-ttu-id="56093-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56093-110">Requirements</span></span>



| <span data-ttu-id="56093-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56093-111">Requirement</span></span> | <span data-ttu-id="56093-112">Wert</span><span class="sxs-lookup"><span data-stu-id="56093-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="56093-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56093-113">Minimum supported client</span></span><br/> | <span data-ttu-id="56093-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56093-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="56093-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56093-115">Minimum supported server</span></span><br/> | <span data-ttu-id="56093-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56093-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="56093-117">Header</span><span class="sxs-lookup"><span data-stu-id="56093-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="56093-118"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="56093-118"><dt>Rpc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56093-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56093-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56093-120">**Rpcaußer**</span><span class="sxs-lookup"><span data-stu-id="56093-120">**RpcExcept**</span></span>](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[<span data-ttu-id="56093-121">**Rpcexceptionfilter**</span><span class="sxs-lookup"><span data-stu-id="56093-121">**RpcExceptionFilter**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[<span data-ttu-id="56093-122">**Rpctryschließlich**</span><span class="sxs-lookup"><span data-stu-id="56093-122">**RpcTryFinally**</span></span>](rpctryfinally.md)
</dt> </dl>

 

