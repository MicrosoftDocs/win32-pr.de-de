---
description: Sie können das Feature für automatische Ausführung für jede Methode aktivieren, die von einer Komponente verfügbar gemacht wird, für die die com+-JIT-Aktivierung aktiviert ist. Wenn die JIT-Aktivierung deaktiviert ist, ist die automatische Ausführung nicht verfügbar.
ms.assetid: d699b85c-441f-4ea6-8d03-d1fa9a8a357f
title: Aktivieren von "automatisch abgeschlossen" für eine Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130e5f8b2fde6c6755ef4174892aa35be8a24cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339701"
---
# <a name="enabling-auto-done-for-a-method"></a><span data-ttu-id="077b3-104">Aktivieren von "automatisch abgeschlossen" für eine Methode</span><span class="sxs-lookup"><span data-stu-id="077b3-104">Enabling Auto-Done for a Method</span></span>

<span data-ttu-id="077b3-105">Sie können das Feature für automatische Ausführung für jede Methode aktivieren, die von einer Komponente verfügbar gemacht wird, für die die com+-JIT-Aktivierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="077b3-105">You can enable the auto-done feature for any method exposed by a component for which COM+ JIT activation is enabled.</span></span> <span data-ttu-id="077b3-106">Wenn die JIT-Aktivierung deaktiviert ist, ist die automatische Ausführung nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="077b3-106">If JIT activation is disabled, auto-done is unavailable.</span></span>

<span data-ttu-id="077b3-107">Sie sollten die automatische Ausführung nur für eine Methode aktivieren, die absichtlich geschrieben wurde, um Sie zu nutzen, da dieses Feature potenziell das erwartete Verhalten der Methode ändern kann.</span><span class="sxs-lookup"><span data-stu-id="077b3-107">You should enable auto-done only for a method that has intentionally been written to take advantage of it because this feature can potentially change the expected behavior of the method.</span></span>

<span data-ttu-id="077b3-108">Wenn Sie die Option automatisch abgeschlossen aktivieren, ändern Sie das Standardverhalten der JIT-Aktivierung und der automatischen Transaktionen für diese Methode.</span><span class="sxs-lookup"><span data-stu-id="077b3-108">When you enable auto-done, you are changing the default behavior of both JIT activation and automatic transactions for that method.</span></span> <span data-ttu-id="077b3-109">Sie können diese Funktion verwenden, da Sie die Notwendigkeit der expliziten Deklaration von Konsistenz und Sicherheit entfernen kann.</span><span class="sxs-lookup"><span data-stu-id="077b3-109">You may want to use this feature because it can remove the necessity to explicitly declare consistency and doneness.</span></span> <span data-ttu-id="077b3-110">Dies kann stattdessen erfolgen, indem einfach ein HRESULT zurückgegeben wird, wenn die automatische Ausführung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="077b3-110">This can instead be done by simply returning an HRESULT when auto-done is enabled.</span></span> <span data-ttu-id="077b3-111">Wenn Sie das automatische ausführen aktivieren, weisen Sie com+ im Wesentlichen an, Folgendes durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="077b3-111">Essentially, when you enable auto-done, you are instructing COM+ to do the following:</span></span>

-   <span data-ttu-id="077b3-112">Legen Sie das done-Bit standardmäßig für den Kontext fest, in dem das-Objekt ausgeführt wird, wenn diese Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="077b3-112">Set the done bit to True by default on the context in which the object runs whenever this method is called.</span></span>
-   <span data-ttu-id="077b3-113">Überprüfen Sie das von der-Methode zurückgegebene HRESULT. Wenn Sie Erfolg oder Fehler angibt, legen Sie das Konsistenz Bit entsprechend fest.</span><span class="sxs-lookup"><span data-stu-id="077b3-113">Inspect the HRESULT returned by the method; if it indicates SUCCESS or FAILURE, set the consistency bit accordingly.</span></span> <span data-ttu-id="077b3-114">Dies kann zu einem automatischen Aufrufen von [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) oder [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)führen, je nachdem, was die Methode intern tut.</span><span class="sxs-lookup"><span data-stu-id="077b3-114">This can result in an automatic call to [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) or [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), depending also on what the method does internally.</span></span>

<span data-ttu-id="077b3-115">**So aktivieren Sie die automatische Ausführung für eine Methode**</span><span class="sxs-lookup"><span data-stu-id="077b3-115">**To enable auto-done for a method**</span></span>

1.  <span data-ttu-id="077b3-116">Klicken Sie im Detailbereich des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die Methode, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="077b3-116">In the details pane of the Component Services administrative tool, right-click the method that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="077b3-117">Klicken Sie im Dialogfeld Eigenschaften der Methode auf die Registerkarte **Allgemein** .</span><span class="sxs-lookup"><span data-stu-id="077b3-117">In the method properties dialog box, click the **General** tab.</span></span>

3.  <span data-ttu-id="077b3-118">Aktivieren Sie das Kontrollkästchen **dieses Objekt automatisch deaktivieren, wenn diese Methode zurück** gegeben wird, um die automatische Durchführung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="077b3-118">To enable auto-done, select the **Automatically deactivate this object when this method returns** check box.</span></span> <span data-ttu-id="077b3-119">Wenn das Kontrollkästchen nicht verfügbar ist, müssen Sie zunächst die JIT-Aktivierung für die Komponente aktivieren.</span><span class="sxs-lookup"><span data-stu-id="077b3-119">If the check box is unavailable, you must first enable JIT Activation for the component.</span></span> <span data-ttu-id="077b3-120">(Ausführliche Anweisungen finden Sie unter[Aktivieren der JIT-Aktivierung für eine Komponente](enabling-jit-activation-for-a-component.md) .)</span><span class="sxs-lookup"><span data-stu-id="077b3-120">(See[Enabling JIT Activation for a Component](enabling-jit-activation-for-a-component.md) for detailed instructions.)</span></span>

4.  <span data-ttu-id="077b3-121">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="077b3-121">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="077b3-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="077b3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="077b3-123">Konzepte für die Just-in-Time-Aktivierung in com+</span><span class="sxs-lookup"><span data-stu-id="077b3-123">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="077b3-124">Aktivieren der JIT-Aktivierung für eine Komponente</span><span class="sxs-lookup"><span data-stu-id="077b3-124">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="077b3-125">Festlegen des done-Bits</span><span class="sxs-lookup"><span data-stu-id="077b3-125">Setting the Done Bit</span></span>](setting-the-done-bit.md)
</dt> </dl>

 

 



