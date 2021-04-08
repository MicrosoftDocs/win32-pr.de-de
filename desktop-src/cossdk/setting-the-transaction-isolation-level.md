---
description: Mithilfe des Verwaltungs Programms Komponenten Dienste können Sie die Transaktions Isolationsstufe von Komponenten manuell festlegen, oder Sie können die Transaktions Isolationsstufe für eine Komponente mithilfe der com+-Verwaltungs Schnittstellen Programm gesteuert konfigurieren.
ms.assetid: 3ef5b805-334d-4803-be67-00c9e35cdcc6
title: Festlegen der Transaktionsisolationsstufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b0447af2591c4f4b3e8e76c017157c02908367
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748841"
---
# <a name="setting-the-transaction-isolation-level"></a><span data-ttu-id="edf03-103">Festlegen der Transaktionsisolationsstufe</span><span class="sxs-lookup"><span data-stu-id="edf03-103">Setting the Transaction Isolation Level</span></span>

<span data-ttu-id="edf03-104">Mithilfe des Verwaltungs Programms Komponenten Dienste können Sie die Transaktions Isolationsstufe von Komponenten manuell festlegen, oder Sie können die Transaktions Isolationsstufe für eine Komponente mithilfe der [com+-Verwaltungs Schnittstellen](com--administration-interfaces.md)Programm gesteuert konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="edf03-104">You can manually set the transaction isolation level of components by using the Component Services administrative tool, or you can programmatically configure the transaction isolation level for a component by using the [COM+ administration interfaces](com--administration-interfaces.md).</span></span>

<span data-ttu-id="edf03-105">Weitere Informationen zu Transaktions Isolations Stufen finden Sie unter [Konfigurieren von Transaktions Isolations Stufen](configuring-transaction-isolation-levels.md).</span><span class="sxs-lookup"><span data-stu-id="edf03-105">For more on transaction isolation levels, see [Configuring Transaction Isolation Levels](configuring-transaction-isolation-levels.md).</span></span>

<span data-ttu-id="edf03-106">**So legen Sie die Transaktions Isolationsstufe mithilfe des Verwaltungs Tools "Komponenten Dienste" fest**</span><span class="sxs-lookup"><span data-stu-id="edf03-106">**To set the transaction isolation level by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="edf03-107">Klicken Sie in der Konsolen Struktur mit der rechten Maustaste auf die Komponente, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="edf03-107">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="edf03-108">Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Transaktionen** .</span><span class="sxs-lookup"><span data-stu-id="edf03-108">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="edf03-109">Wählen Sie unter **Transaktions Isolationsstufe** den gewünschten Wert aus dem Dropdown Feld aus.</span><span class="sxs-lookup"><span data-stu-id="edf03-109">Under **Transaction Isolation Level**, select the value you want from the drop-down box.</span></span> <span data-ttu-id="edf03-110">Der Standardwert für alle Komponenten wird **serialisiert**.</span><span class="sxs-lookup"><span data-stu-id="edf03-110">The default value for all components is **Serialized**.</span></span>

    > [!Note]  
    > <span data-ttu-id="edf03-111">Wenn unter **Transaktionsunterstützung** entweder **deaktiviert** oder **nicht unterstützt** ausgewählt ist, kann die Transaktions Isolationsstufe nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="edf03-111">If either **Disabled** or **Not Supported** is selected under **Transaction support**, you cannot set the transaction isolation level.</span></span>

     

4.  <span data-ttu-id="edf03-112">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="edf03-112">Click **OK**.</span></span>

<span data-ttu-id="edf03-113">Sie müssen dieses Verfahren für jede Komponente wiederholen.</span><span class="sxs-lookup"><span data-stu-id="edf03-113">You must repeat this procedure for each component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="edf03-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="edf03-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edf03-115">Konfigurieren von Transaktions Isolations Stufen</span><span class="sxs-lookup"><span data-stu-id="edf03-115">Configuring Transaction Isolation Levels</span></span>](configuring-transaction-isolation-levels.md)
</dt> </dl>

 

 



