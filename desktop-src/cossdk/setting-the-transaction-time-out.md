---
description: Sie können das Timeout für Transaktionen manuell mithilfe des Verwaltungs Tools Komponenten Dienste festlegen, oder Sie können das Timeout mithilfe der com+-Verwaltungs Schnittstellen Programm gesteuert konfigurieren.
ms.assetid: f7a35bdf-ea6d-40ea-b3c0-c2a3ae2276c4
title: Festlegen der Transaktions Time-Out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b002448ca21e97e2e4996679d87a4b6a7680161f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483782"
---
# <a name="setting-the-transaction-time-out"></a><span data-ttu-id="439eb-103">Festlegen der Transaktions Time-Out</span><span class="sxs-lookup"><span data-stu-id="439eb-103">Setting the Transaction Time-Out</span></span>

<span data-ttu-id="439eb-104">Sie können das Timeout für Transaktionen manuell mithilfe des Verwaltungs Tools Komponenten Dienste festlegen, oder Sie können das Timeout mithilfe der [com+-Verwaltungs Schnittstellen](com--administration-interfaces.md)Programm gesteuert konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="439eb-104">You can manually set the time-out for transactions by using the Component Services administrative tool, or you can programmatically configure the time-out by using the [COM+ administration interfaces](com--administration-interfaces.md).</span></span> <span data-ttu-id="439eb-105">Das Timeout kann auf der Ebene des lokalen Computers und auch für einzelne Komponenten konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="439eb-105">The time-out can be configured at the local computer level and also for individual components.</span></span>

<span data-ttu-id="439eb-106">**So legen Sie das Transaktions Timeout für den lokalen Computer mithilfe des Verwaltungs Tools "Komponenten Dienste" fest**</span><span class="sxs-lookup"><span data-stu-id="439eb-106">**To set the transaction time-out for the local computer by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="439eb-107">Klicken Sie in der Konsolen Struktur mit der rechten Maustaste auf den lokalen Computer, den Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="439eb-107">In the console tree, right-click the local computer you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="439eb-108">Klicken Sie im Dialogfeld Computer Eigenschaften auf die Registerkarte **Optionen** .</span><span class="sxs-lookup"><span data-stu-id="439eb-108">In the computer properties dialog box, click the **Options** tab.</span></span>

3.  <span data-ttu-id="439eb-109">Geben Sie unter **Transaktions Timeout** den Transaktions Timeout in Sekunden ein.</span><span class="sxs-lookup"><span data-stu-id="439eb-109">Under **Transaction Timeout**, enter the transaction time-out in seconds.</span></span> <span data-ttu-id="439eb-110">Der Standardwert für das Timeout beträgt 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="439eb-110">The default time-out is 60 seconds.</span></span>

4.  <span data-ttu-id="439eb-111">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="439eb-111">Click **OK**.</span></span>

<span data-ttu-id="439eb-112">**So legen Sie das Transaktions Timeout für eine Komponente mithilfe des Verwaltungs Tools "Komponenten Dienste" fest**</span><span class="sxs-lookup"><span data-stu-id="439eb-112">**To set the transaction time-out for a component by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="439eb-113">Klicken Sie in der Konsolen Struktur mit der rechten Maustaste auf die Komponente, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="439eb-113">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="439eb-114">Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Transaktionen** .</span><span class="sxs-lookup"><span data-stu-id="439eb-114">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="439eb-115">Aktivieren Sie das Kontrollkästchen mit der Bezeichnung **globalen Transaktions Timeout Wert überschreiben**.</span><span class="sxs-lookup"><span data-stu-id="439eb-115">Check the box labeled **Override global transaction timeout value**.</span></span>

    > [!Note]  
    > <span data-ttu-id="439eb-116">Sie können das Kontrollkästchen nicht aktivieren, um den Timeout Wert für die globale Transaktion zu überschreiben, wenn die **Transaktionsunterstützung** auf **deaktiviert**, **nicht unterstützt** oder **unterstützt** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="439eb-116">You cannot check the box to override the global transaction time-out value if the **Transaction support** is set to **Disabled**, **Not Supported**, or **Supported**.</span></span>

     

4.  <span data-ttu-id="439eb-117">Geben Sie unter **Transaktions Timeout** den Transaktions Timeout in Sekunden ein.</span><span class="sxs-lookup"><span data-stu-id="439eb-117">Under **Transaction Timeout**, enter the transaction time-out in seconds.</span></span> <span data-ttu-id="439eb-118">Der Standardwert für das Timeout beträgt 0 Sekunden. Dies bedeutet, dass die Komponente niemals ein Timeout für die Transaktion verursacht.</span><span class="sxs-lookup"><span data-stu-id="439eb-118">The default time-out is 0 seconds, which means that the component will never cause the transaction to time out.</span></span>

5.  <span data-ttu-id="439eb-119">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="439eb-119">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="439eb-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="439eb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="439eb-121">Verwalten von automatischen Transaktionen in com+</span><span class="sxs-lookup"><span data-stu-id="439eb-121">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



