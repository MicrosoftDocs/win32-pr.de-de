---
title: Rpctryschließlich (RPC. h)
description: Die rpctryschluss-Anweisung stellt eine strukturierte Abbruch Behandlung bereit.
ms.assetid: e9ed748a-db15-4c91-b8a4-b510f99042d8
keywords:
- Rpctryschließlich RPC
topic_type:
- apiref
api_name:
- RpcTryFinally
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 909d65013fb3fb83ffb926fea6a6b3f30980a3b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477505"
---
# <a name="rpctryfinally"></a><span data-ttu-id="31a49-104">Rpctryschließlich</span><span class="sxs-lookup"><span data-stu-id="31a49-104">RpcTryFinally</span></span>

<span data-ttu-id="31a49-105">Die **rpctryschluss** -Anweisung stellt eine strukturierte Abbruch Behandlung bereit.</span><span class="sxs-lookup"><span data-stu-id="31a49-105">The **RpcTryFinally** statement provides structured termination handling.</span></span> <span data-ttu-id="31a49-106">Es tritt eine Ausnahme während der Ausführungs Anweisungen des Codeblocks auf, der der **rpctryendlich** -Anweisung zugeordnet ist. die Anweisungen im Codeblock, die der [**rpcletzenanweisung**](/previous-versions/aa375699(v=vs.80)) zugeordnet sind, werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31a49-106">It an exception occurs during the execution statements of the code block associated with the **RpcTryFinally** statement, the statements in the code block associated with the [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) statement are executed.</span></span> <span data-ttu-id="31a49-107">Alle **rpctryend** -Anweisungen müssen durch eine [**rpcendendlich**](/previous-versions/aa375634(v=vs.80)) -Anweisung beendet werden.</span><span class="sxs-lookup"><span data-stu-id="31a49-107">All **RpcTryFinally** statements must be terminated by an [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) statement.</span></span>

<span data-ttu-id="31a49-108">Weitere Informationen finden Sie unter [**rpcschließlich**](/previous-versions/aa375699(v=vs.80)).</span><span class="sxs-lookup"><span data-stu-id="31a49-108">For more information, see [**RpcFinally**](/previous-versions/aa375699(v=vs.80)).</span></span>

## <a name="requirements"></a><span data-ttu-id="31a49-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31a49-109">Requirements</span></span>



| <span data-ttu-id="31a49-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31a49-110">Requirement</span></span> | <span data-ttu-id="31a49-111">Wert</span><span class="sxs-lookup"><span data-stu-id="31a49-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="31a49-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31a49-112">Minimum supported client</span></span><br/> | <span data-ttu-id="31a49-113">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31a49-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="31a49-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31a49-114">Minimum supported server</span></span><br/> | <span data-ttu-id="31a49-115">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31a49-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="31a49-116">Header</span><span class="sxs-lookup"><span data-stu-id="31a49-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="31a49-117"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="31a49-117"><dt>Rpc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31a49-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31a49-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="31a49-119">[**Rpcschließlich**](/previous-versions/aa375699(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="31a49-119">[**RpcFinally**](/previous-versions/aa375699(v=vs.80))</span></span>
</dt> <dt>

<span data-ttu-id="31a49-120">[**Rpcendendlich**](/previous-versions/aa375634(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="31a49-120">[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))</span></span>
</dt> </dl>

 

