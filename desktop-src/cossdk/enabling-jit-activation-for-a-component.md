---
description: Aktivieren der JIT-Aktivierung für eine Komponente
ms.assetid: ccf7c98b-8b1a-431d-b417-83f79734f691
title: Aktivieren der JIT-Aktivierung für eine Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f61cc5c79270a926bb50e3408766df63f4484c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346237"
---
# <a name="enabling-jit-activation-for-a-component"></a><span data-ttu-id="ea05c-103">Aktivieren der JIT-Aktivierung für eine Komponente</span><span class="sxs-lookup"><span data-stu-id="ea05c-103">Enabling JIT Activation for a Component</span></span>

<span data-ttu-id="ea05c-104">Sie sollten eine Komponente so konfigurieren, dass Sie JIT nur dann aktiviert wird, wenn Sie ordnungsgemäß für die Unterstützung des com+ Just-in-time (JIT)-Aktivierungs Dienstanbieter geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="ea05c-104">You should configure a component to be JIT activated only when it is correctly written to support the COM+ Just-in-Time (JIT) Activation service.</span></span> <span data-ttu-id="ea05c-105">Wenn eine Komponente zwischen Methoden aufrufen deaktiviert wird, verliert sie jeden zugeordneten Zustand.</span><span class="sxs-lookup"><span data-stu-id="ea05c-105">If a component is deactivated between method calls, it will lose any associated state.</span></span> <span data-ttu-id="ea05c-106">Aufgrund des Standard Verhaltens der JIT-Aktivierung tritt dies wahrscheinlich nicht auf, wenn Sie es nicht erwarten, aber Sie sollten die Anforderungen einer Komponente beachten, bevor Sie die Konfiguration und die Erwartungen von Clients ändern, die die Komponente aufrufen werden.</span><span class="sxs-lookup"><span data-stu-id="ea05c-106">Given the default behavior of JIT Activation, this is unlikely to occur when you don't expect it to, but you should be aware of a component's requirements prior to changing its configuration and of the expectations of clients that will be calling the component.</span></span>

> [!Note]  
> <span data-ttu-id="ea05c-107">Wenn eine Komponente so konfiguriert ist, dass Transaktionen erforderlich sind, wird der com+-JIT-Aktivierungs Dienst automatisch aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ea05c-107">If a component is configured to require transactions, the COM+ JIT Activation service is enabled automatically.</span></span> <span data-ttu-id="ea05c-108">Sie können Sie in diesem Fall nicht deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ea05c-108">You cannot disable it in this case.</span></span> <span data-ttu-id="ea05c-109">Weitere Details finden Sie unter [Konfigurieren von Transaktionen](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="ea05c-109">For more detail, see [Configuring Transactions](configuring-transactions.md).</span></span>

 

<span data-ttu-id="ea05c-110">Wenn Sie die JIT-Aktivierung für eine Komponente aktivieren, wird das Synchronisierungs Attribut für diese Komponente auf Required festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ea05c-110">When you enable JIT Activation for a component, its synchronization attribute is set to required for that component.</span></span> <span data-ttu-id="ea05c-111">In diesem Fall können Sie die Synchronisierungs Einstellung nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="ea05c-111">You cannot change the synchronization setting in this case.</span></span> <span data-ttu-id="ea05c-112">Weitere Details finden Sie unter [Synchronisierungs Abhängigkeiten](synchronization-dependencies.md).</span><span class="sxs-lookup"><span data-stu-id="ea05c-112">For more detail, see [Synchronization Dependencies](synchronization-dependencies.md).</span></span>

<span data-ttu-id="ea05c-113">**So aktivieren Sie die JIT-Aktivierung**</span><span class="sxs-lookup"><span data-stu-id="ea05c-113">**To enable JIT Activation**</span></span>

1.  <span data-ttu-id="ea05c-114">Klicken Sie im Detailbereich des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die Komponente, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="ea05c-114">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="ea05c-115">Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Aktivierung** .</span><span class="sxs-lookup"><span data-stu-id="ea05c-115">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="ea05c-116">Aktivieren Sie das Kontrollkästchen Just-in-Time- **Aktivierung aktivieren** , um die JIT-Aktivierung für die Komponente zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ea05c-116">To enable JIT activation for the component, select the **Enable Just In Time Activation** check box.</span></span>

4.  <span data-ttu-id="ea05c-117">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ea05c-117">Click **OK**.</span></span>

<span data-ttu-id="ea05c-118">Wenn Sie die JIT-Aktivierung für eine Komponente aktiviert haben, haben Sie die Möglichkeit, die Funktion für automatische Ausführung für jede Methode zu aktivieren, die von dieser Komponente verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="ea05c-118">When you have enabled JIT Activation for a component, you have the option of enabling the auto-done feature for any method exposed by that component.</span></span> <span data-ttu-id="ea05c-119">Weitere Informationen finden Sie unter [Aktivieren der automatischen Ausführung für eine Methode](enabling-auto-done-for-a-method.md) .</span><span class="sxs-lookup"><span data-stu-id="ea05c-119">See [Enabling Auto-Done for a Method](enabling-auto-done-for-a-method.md) for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea05c-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ea05c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea05c-121">Aktivieren von "automatisch abgeschlossen" für eine Methode</span><span class="sxs-lookup"><span data-stu-id="ea05c-121">Enabling Auto-Done for a Method</span></span>](enabling-auto-done-for-a-method.md)
</dt> <dt>

[<span data-ttu-id="ea05c-122">Festlegen des done-Bits</span><span class="sxs-lookup"><span data-stu-id="ea05c-122">Setting the Done Bit</span></span>](setting-the-done-bit.md)
</dt> </dl>

 

 



