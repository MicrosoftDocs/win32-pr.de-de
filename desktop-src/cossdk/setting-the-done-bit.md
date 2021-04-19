---
description: Festlegen des done-Bits
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: Festlegen des done-Bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a53368377016c88633d91d942cde1970d979563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344220"
---
# <a name="setting-the-done-bit"></a><span data-ttu-id="766c8-103">Festlegen des done-Bits</span><span class="sxs-lookup"><span data-stu-id="766c8-103">Setting the Done Bit</span></span>

<span data-ttu-id="766c8-104">Com+ deaktiviert ein JIT-aktiviertes Objekt basierend auf dem Status einer Kontext Eigenschaft, dem done-Bit, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="766c8-104">COM+ will deactivate a JIT-activated object based on the status of a context property, the done bit, as follows:</span></span>

-   <span data-ttu-id="766c8-105">Wenn das done-Bit auf true festgelegt ist, deaktiviert com+ das Objekt, wenn der aktuelle Methoden Aufrufwert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="766c8-105">When the done bit is set to True, COM+ deactivates the object when the current method call returns.</span></span>
-   <span data-ttu-id="766c8-106">Wenn das done-Bit auf false festgelegt ist, bleibt das Objekt aktiv, wenn der aktuelle Methoden Aufrufwert zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="766c8-106">When the done bit is set to False, the object remains active when the current method call returns.</span></span>

<span data-ttu-id="766c8-107">Standardmäßig ist das done-Bit auf false festgelegt, wenn ein Objekt erstellt und der Kontext initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="766c8-107">By default, the done bit is set to False when an object is created and its context initialized.</span></span> <span data-ttu-id="766c8-108">(Jedes JIT-aktivierte Objekt wird in einem eigenen Kontext erstellt, sodass es ein eigenes done-Bit festgelegt werden kann.) Sie können diese Standardeinstellung jedoch für jede Methode ändern, indem Sie die Auto-done-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="766c8-108">(Any JIT-activated object is created in its own context so that it has its own done bit to set.) However, you can change this default setting on a per-method basis by using the auto-done property.</span></span> <span data-ttu-id="766c8-109">Sie können das done-Bit auf folgende Weise festlegen:</span><span class="sxs-lookup"><span data-stu-id="766c8-109">You can set the done bit in the following ways:</span></span>

-   <span data-ttu-id="766c8-110">Verwenden von [ **IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span><span class="sxs-lookup"><span data-stu-id="766c8-110">Using [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span></span>
-   <span data-ttu-id="766c8-111">Verwenden von [ **IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span><span class="sxs-lookup"><span data-stu-id="766c8-111">Using [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span></span>
-   <span data-ttu-id="766c8-112">Verwenden der Auto-done-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="766c8-112">Using the auto-done property</span></span>

## <a name="using-icontextstate"></a><span data-ttu-id="766c8-113">Verwenden von IContextState</span><span class="sxs-lookup"><span data-stu-id="766c8-113">Using IContextState</span></span>

<span data-ttu-id="766c8-114">Sie können [**IContextState:: setde activateonreturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) verwenden, um das done-Bit auf true oder false festzulegen.</span><span class="sxs-lookup"><span data-stu-id="766c8-114">You can use [**IContextState::SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) to set the done bit to True or False.</span></span>

<span data-ttu-id="766c8-115">Sie können [**IContextState:: getdeactivateonreturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) verwenden, um den aktuellen Status des done-Bits aus dem Objekt Kontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="766c8-115">You can use [**IContextState::GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) to get the current status of the done bit from the object context.</span></span>

## <a name="using-iobjectcontext"></a><span data-ttu-id="766c8-116">Verwenden von IObjectContext</span><span class="sxs-lookup"><span data-stu-id="766c8-116">Using IObjectContext</span></span>

<span data-ttu-id="766c8-117">Mit den folgenden Methoden für [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) können Sie das done-Bit festlegen und gleichzeitig das konsistente Bit festlegen, das für die Abstimmung in Transaktionen verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="766c8-117">You can use the following methods on [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) to set the done bit while simultaneously setting the consistent bit used for voting in transactions:</span></span>

-   <span data-ttu-id="766c8-118">[**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) signalisiert Ihnen, dass Sie fertig sind, und dass Sie abstimmen, um für die aktuelle Transaktion ein Commit auszuführen.</span><span class="sxs-lookup"><span data-stu-id="766c8-118">[**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) signals both that you are done and that you vote to commit the current transaction.</span></span> <span data-ttu-id="766c8-119">Sowohl das done-Bit als auch das konsistente Bit werden auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="766c8-119">It sets both the done bit and the consistent bit to True.</span></span>
-   <span data-ttu-id="766c8-120">" [**Abtabort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) " signalisiert, dass Sie abgeschlossen sind, und Dooms die aktuelle Transaktion.</span><span class="sxs-lookup"><span data-stu-id="766c8-120">[**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) signals that you are done and dooms the current transaction.</span></span> <span data-ttu-id="766c8-121">Dabei wird das done-Bit auf true und das konsistente Bit auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="766c8-121">It sets the done bit to True and the consistent bit to False.</span></span>
-   <span data-ttu-id="766c8-122">[**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) signalisiert, dass Sie nicht abgeschlossen sind, aber dass Sie für die Transaktion ein Commit durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="766c8-122">[**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) signals that you are not done but that you vote to commit the transaction.</span></span> <span data-ttu-id="766c8-123">Dabei wird das done-Bit auf false und das konsistente Bit auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="766c8-123">It sets the done bit to False and the consistent bit to True.</span></span>
-   <span data-ttu-id="766c8-124">[**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) signalisiert, dass Sie nicht ausgeführt werden, und dass Sie die Transaktion zu diesem Zeitpunkt nicht committen müssen, normalerweise weil der Status inkonsistent ist.</span><span class="sxs-lookup"><span data-stu-id="766c8-124">[**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) signals that you are not done and that you vote not to commit the transaction at this time, usually because the state is inconsistent.</span></span> <span data-ttu-id="766c8-125">Sowohl das done-Bit als auch das konsistente Bit werden auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="766c8-125">It sets both the done bit and the consistent bit to False.</span></span>

## <a name="related-topics"></a><span data-ttu-id="766c8-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="766c8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="766c8-127">Konzepte für die Just-in-Time-Aktivierung in com+</span><span class="sxs-lookup"><span data-stu-id="766c8-127">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="766c8-128">Aktivieren der JIT-Aktivierung für eine Komponente</span><span class="sxs-lookup"><span data-stu-id="766c8-128">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="766c8-129">Objekt Pooling und com+-JIT-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="766c8-129">Object Pooling and COM+ JIT Activation</span></span>](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[<span data-ttu-id="766c8-130">Transaktionen und com+-JIT-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="766c8-130">Transactions and COM+ JIT Activation</span></span>](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



