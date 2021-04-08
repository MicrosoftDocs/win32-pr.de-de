---
description: Erstellt ein generisches Transaktions Objekt, das eine Transaktion startet. Indem Sie die Methoden dieser Klasse aufrufen, können Sie die Arbeit mehrerer COM-Objekte in einer einzelnen Transaktion verfassen und die Transaktion explizit Committe oder Abbrechen.
ms.assetid: 5f3f83e0-33fc-4c43-9327-59485c0d8bd3
title: Transaction contextex-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContextEx
api_type:
- COM
ms.openlocfilehash: 8cf5c3aaa7ffe126124a909498a7c54cfb012c65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748840"
---
# <a name="transactioncontextex-class"></a><span data-ttu-id="87ee2-104">Transaction contextex-Klasse</span><span class="sxs-lookup"><span data-stu-id="87ee2-104">TransactionContextEx class</span></span>

<span data-ttu-id="87ee2-105">Erstellt ein generisches Transaktions Objekt, das eine Transaktion startet.</span><span class="sxs-lookup"><span data-stu-id="87ee2-105">Creates a generic transactional object that begins a transaction.</span></span> <span data-ttu-id="87ee2-106">Indem Sie die Methoden dieser Klasse aufrufen, können Sie die Arbeit mehrerer COM-Objekte in einer einzelnen Transaktion verfassen und die Transaktion explizit Committe oder Abbrechen.</span><span class="sxs-lookup"><span data-stu-id="87ee2-106">By calling the methods of this class, you can compose the work of multiple COM objects in a single transaction and explicitly commit or abort the transaction.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="87ee2-107">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="87ee2-107">When to implement</span></span>

<span data-ttu-id="87ee2-108">Diese Klasse wird von com+ implementiert.</span><span class="sxs-lookup"><span data-stu-id="87ee2-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="87ee2-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87ee2-109">Requirement</span></span> | <span data-ttu-id="87ee2-110">Wert</span><span class="sxs-lookup"><span data-stu-id="87ee2-110">Value</span></span> |
|------------|--------------------------------------------------------|
| <span data-ttu-id="87ee2-111">CLSID</span><span class="sxs-lookup"><span data-stu-id="87ee2-111">CLSID</span></span>      | <span data-ttu-id="87ee2-112">CLSID \_ Transaction contextex</span><span class="sxs-lookup"><span data-stu-id="87ee2-112">CLSID\_TransactionContextEx</span></span>                            |
| <span data-ttu-id="87ee2-113">ProgID</span><span class="sxs-lookup"><span data-stu-id="87ee2-113">ProgID</span></span>     | <span data-ttu-id="87ee2-114">L "txctx. Transaction contextex"</span><span class="sxs-lookup"><span data-stu-id="87ee2-114">L"TxCTx.TransactionContextEx"</span></span>                          |
| <span data-ttu-id="87ee2-115">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="87ee2-115">Interfaces</span></span> | [<span data-ttu-id="87ee2-116">**ITransaction contextex**</span><span class="sxs-lookup"><span data-stu-id="87ee2-116">**ITransactionContextEx**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex) |



 

## <a name="when-to-use"></a><span data-ttu-id="87ee2-117">Verwendung</span><span class="sxs-lookup"><span data-stu-id="87ee2-117">When to use</span></span>

<span data-ttu-id="87ee2-118">Ein nicht transaktionaler Client verwendet diese Klasse, um eine Transaktion zu starten.</span><span class="sxs-lookup"><span data-stu-id="87ee2-118">A non-transactional client uses this class to begin a transaction.</span></span> <span data-ttu-id="87ee2-119">Mithilfe der Methoden dieser Klasse kann der Client zusätzliche com-Objekte abrufen, die, wenn Sie für die Teilnahme an einer Transaktion konfiguriert sind, innerhalb der Transaktions Begrenzung des Transaktionskontext Objekts ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="87ee2-119">Using the methods of this class, the client can call additional COM objects that, if configured to participate in a transaction, run within the transaction boundary of the transaction context object.</span></span> <span data-ttu-id="87ee2-120">Basierend auf der Geschäftslogik kann der Client den Commit für die Transaktion explizit durchsetzen oder Abbrechen.</span><span class="sxs-lookup"><span data-stu-id="87ee2-120">Based on its business logic, the client can explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="87ee2-121">Die **Transaction contextex** -Klasse schränkt die Wiederverwendung der Geschäftslogik ein, die die Transaktion steuert.</span><span class="sxs-lookup"><span data-stu-id="87ee2-121">The **TransactionContextEx** class limits reuse of the business logic driving the transaction.</span></span> <span data-ttu-id="87ee2-122">Aus diesem Grund wird empfohlen, dass Objekte, die von der **Transaction contextex** -Klasse instanziiert werden, sparsam verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87ee2-122">For this reason, it is recommended that objects instantiated from the **TransactionContextEx** class be used sparingly.</span></span>

## <a name="remarks"></a><span data-ttu-id="87ee2-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87ee2-123">Remarks</span></span>

<span data-ttu-id="87ee2-124">Um dieses Objekt zu erstellen, rufen Sie [**IObjectContext:: kreateinstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)auf.</span><span class="sxs-lookup"><span data-stu-id="87ee2-124">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="87ee2-125">Die **Transaction contextex** -Klasse wurde nicht für die Verwendung in Visual Basic konzipiert.</span><span class="sxs-lookup"><span data-stu-id="87ee2-125">The **TransactionContextEx** class was not designed to be used in Visual Basic.</span></span> <span data-ttu-id="87ee2-126">Verwenden Sie stattdessen die [**transaktioncontext**](transactioncontext.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="87ee2-126">Use the [**TransactionContext**](transactioncontext.md) class instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="87ee2-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87ee2-127">Requirements</span></span>



| <span data-ttu-id="87ee2-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87ee2-128">Requirement</span></span> | <span data-ttu-id="87ee2-129">Wert</span><span class="sxs-lookup"><span data-stu-id="87ee2-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="87ee2-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87ee2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="87ee2-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87ee2-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="87ee2-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87ee2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="87ee2-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87ee2-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="87ee2-134">Header</span><span class="sxs-lookup"><span data-stu-id="87ee2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="87ee2-135"><dt>"Comsvcs. h"</dt></span><span class="sxs-lookup"><span data-stu-id="87ee2-135"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87ee2-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87ee2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ee2-137">Konfigurieren von Transaktionen</span><span class="sxs-lookup"><span data-stu-id="87ee2-137">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="87ee2-138">**ITransaction contextex**</span><span class="sxs-lookup"><span data-stu-id="87ee2-138">**ITransactionContextEx**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex)
</dt> <dt>

[<span data-ttu-id="87ee2-139">**Transaktioncontext**</span><span class="sxs-lookup"><span data-stu-id="87ee2-139">**TransactionContext**</span></span>](transactioncontext.md)
</dt> </dl>

 

 




