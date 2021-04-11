---
description: Erstellt ein generisches Transaktions Objekt, das eine Transaktion startet.
ms.assetid: efaf1468-4973-472f-af91-85957a52b7df
title: Transaktioncontext-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContext
api_type:
- COM
ms.openlocfilehash: 595b5a3192b87420855eb43f1e1e33df37a45c23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214260"
---
# <a name="transactioncontext-class"></a><span data-ttu-id="75201-103">Transaktioncontext-Klasse</span><span class="sxs-lookup"><span data-stu-id="75201-103">TransactionContext class</span></span>

<span data-ttu-id="75201-104">Erstellt ein generisches Transaktions Objekt, das eine Transaktion startet.</span><span class="sxs-lookup"><span data-stu-id="75201-104">Creates a generic transactional object that begins a transaction.</span></span> <span data-ttu-id="75201-105">Indem Sie die Methoden dieser Klasse aufrufen, können Sie die Arbeit mehrerer COM-Objekte in einer einzelnen Transaktion verfassen und die Transaktion explizit Committe oder Abbrechen.</span><span class="sxs-lookup"><span data-stu-id="75201-105">By calling the methods of this class, you can compose the work of multiple COM objects in a single transaction and explicitly commit or abort the transaction.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="75201-106">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="75201-106">When to implement</span></span>

<span data-ttu-id="75201-107">Diese Klasse wird von com+ implementiert.</span><span class="sxs-lookup"><span data-stu-id="75201-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="75201-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75201-108">Requirement</span></span> | <span data-ttu-id="75201-109">Wert</span><span class="sxs-lookup"><span data-stu-id="75201-109">Value</span></span> |
|------------|----------------------------------------------------|
| <span data-ttu-id="75201-110">CLSID</span><span class="sxs-lookup"><span data-stu-id="75201-110">CLSID</span></span>      | <span data-ttu-id="75201-111">CLSID- \_ Transaktionskontext</span><span class="sxs-lookup"><span data-stu-id="75201-111">CLSID\_TransactionContext</span></span>                          |
| <span data-ttu-id="75201-112">ProgID</span><span class="sxs-lookup"><span data-stu-id="75201-112">ProgID</span></span>     | <span data-ttu-id="75201-113">L "txctx. transaktioncontext"</span><span class="sxs-lookup"><span data-stu-id="75201-113">L"TxCTx.TransactionContext"</span></span>                        |
| <span data-ttu-id="75201-114">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="75201-114">Interfaces</span></span> | [<span data-ttu-id="75201-115">**Itransaktioncontext**</span><span class="sxs-lookup"><span data-stu-id="75201-115">**ITransactionContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext) |



 

## <a name="when-to-use"></a><span data-ttu-id="75201-116">Verwendung</span><span class="sxs-lookup"><span data-stu-id="75201-116">When to use</span></span>

<span data-ttu-id="75201-117">Ein nicht transaktionaler Client verwendet diese Klasse, um eine Transaktion zu starten.</span><span class="sxs-lookup"><span data-stu-id="75201-117">A non-transactional client uses this class to begin a transaction.</span></span> <span data-ttu-id="75201-118">Mithilfe der Methoden dieser Klasse kann der Client zusätzliche com-Objekte abrufen, die, wenn Sie für die Teilnahme an einer Transaktion konfiguriert sind, innerhalb der Transaktions Begrenzung des Transaktionskontext Objekts ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="75201-118">Using the methods of this class, the client can call additional COM objects that, if configured to participate in a transaction, run within the transaction boundary of the transaction context object.</span></span> <span data-ttu-id="75201-119">Basierend auf der Geschäftslogik kann der Client den Commit für die Transaktion explizit durchsetzen oder Abbrechen.</span><span class="sxs-lookup"><span data-stu-id="75201-119">Based on its business logic, the client can explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="75201-120">Die **transaktioncontext** -Klasse schränkt die Wiederverwendung der Geschäftslogik ein, die die Transaktion steuert.</span><span class="sxs-lookup"><span data-stu-id="75201-120">The **TransactionContext** class limits reuse of the business logic driving the transaction.</span></span> <span data-ttu-id="75201-121">Aus diesem Grund wird empfohlen, dass Objekte, die von der **transaktioncontext** -Klasse instanziiert werden, sparsam verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="75201-121">For this reason, it is recommended that objects instantiated from the **TransactionContext** class be used sparingly.</span></span>

## <a name="remarks"></a><span data-ttu-id="75201-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75201-122">Remarks</span></span>

<span data-ttu-id="75201-123">Um dieses Objekt zu erstellen, rufen Sie [**IObjectContext:: kreateinstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)auf.</span><span class="sxs-lookup"><span data-stu-id="75201-123">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="75201-124">Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="75201-124">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="75201-125">Ein transaktioncontext-Objekt kann mithilfe von "COMSVCSLIB. transaktioncontext" als Klassenname deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="75201-125">A TransactionContext object can be declared using "COMSVCSLib.TransactionContext" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="75201-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75201-126">Requirements</span></span>



| <span data-ttu-id="75201-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75201-127">Requirement</span></span> | <span data-ttu-id="75201-128">Wert</span><span class="sxs-lookup"><span data-stu-id="75201-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="75201-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75201-129">Minimum supported client</span></span><br/> | <span data-ttu-id="75201-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75201-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="75201-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75201-131">Minimum supported server</span></span><br/> | <span data-ttu-id="75201-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75201-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="75201-133">Header</span><span class="sxs-lookup"><span data-stu-id="75201-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="75201-134"><dt>"Comsvcs. h"</dt></span><span class="sxs-lookup"><span data-stu-id="75201-134"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75201-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75201-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75201-136">Konfigurieren von Transaktionen</span><span class="sxs-lookup"><span data-stu-id="75201-136">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="75201-137">**Itransaktioncontext**</span><span class="sxs-lookup"><span data-stu-id="75201-137">**ITransactionContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext)
</dt> <dt>

[<span data-ttu-id="75201-138">**Transaction contextex**</span><span class="sxs-lookup"><span data-stu-id="75201-138">**TransactionContextEx**</span></span>](transactioncontextex.md)
</dt> </dl>

 

 




