---
description: Sie können Objekt Statistiken überwachen, während eine Anwendung ausgeführt wird. Auf diese Weise können Sie die Eigenschaften des Objekt Pools optimieren, um das Gleichgewicht der Leistung und Ressourcen zu erzielen, die Sie nutzen möchten.
ms.assetid: 57987cc1-8bb5-4bbd-a425-fda2e5a8b597
title: Objekt Statistik überwachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f438bc7081546083f1930fe31f16a2198b09b48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342199"
---
# <a name="monitoring-object-statistics"></a><span data-ttu-id="af36f-104">Objekt Statistik überwachen</span><span class="sxs-lookup"><span data-stu-id="af36f-104">Monitoring Object Statistics</span></span>

<span data-ttu-id="af36f-105">Sie können Objekt Statistiken überwachen, während eine Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af36f-105">You can monitor object statistics as an application runs.</span></span> <span data-ttu-id="af36f-106">Auf diese Weise können Sie die Eigenschaften des Objekt Pools optimieren, um das Gleichgewicht der Leistung und Ressourcen zu erzielen, die Sie nutzen möchten.</span><span class="sxs-lookup"><span data-stu-id="af36f-106">By doing so, you can fine-tune the object pool characteristics to achieve the balance in performance and resources that you would like to have.</span></span>

<span data-ttu-id="af36f-107">Sie können den Status für alle Objekte überwachen, die für die Unterstützung von Objekt Statistiken und Ereignis Berichterstattung konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="af36f-107">You can monitor status for any objects that are configured to support object statistics and event reporting.</span></span> <span data-ttu-id="af36f-108">Die Aktivierung von Objekt Statistiken hat einen sehr geringen Leistungs Aufwand zur Folge.</span><span class="sxs-lookup"><span data-stu-id="af36f-108">Enabling object statistics has a very slight performance overhead.</span></span>

<span data-ttu-id="af36f-109">**So aktivieren Sie Objekt Statistiken**</span><span class="sxs-lookup"><span data-stu-id="af36f-109">**To enable object statistics**</span></span>

1.  <span data-ttu-id="af36f-110">Klicken Sie im Detailbereich des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die Komponente, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="af36f-110">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="af36f-111">Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Aktivierung** .</span><span class="sxs-lookup"><span data-stu-id="af36f-111">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="af36f-112">Aktivieren Sie zum Aktivieren von Objekt Statistiken für die Komponente unter **Aktivierungs Kontext** das Kontrollkästchen **Komponente unterstützt Ereignisse und Statistiken** .</span><span class="sxs-lookup"><span data-stu-id="af36f-112">To enable object statistics for the component, under **Activation Context**, select the **Component supports events and statistics** check box.</span></span>

<span data-ttu-id="af36f-113">**So überwachen Sie den Objektstatus**</span><span class="sxs-lookup"><span data-stu-id="af36f-113">**To monitor object status**</span></span>

1.  <span data-ttu-id="af36f-114">Öffnen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste den Ordner für die Anwendung, die die Komponenten enthält, die Sie überwachen möchten.</span><span class="sxs-lookup"><span data-stu-id="af36f-114">In the console tree of the Component Services administrative tool, open the folder for the application that includes the components you want to monitor.</span></span>

2.  <span data-ttu-id="af36f-115">Klicken Sie mit der rechten Maustaste auf den Ordner **Komponenten** , zeigen Sie auf **anzeigen**, und klicken Sie dann auf **Status Ansicht**.</span><span class="sxs-lookup"><span data-stu-id="af36f-115">Right-click the **Components** folder, point to **View**, and then click **Status View**.</span></span> <span data-ttu-id="af36f-116">Im Detailbereich wird nun die Statusansicht für alle Komponenten in der Anwendung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="af36f-116">The details pane now displays the status view for all components in the application.</span></span> <span data-ttu-id="af36f-117">In der folgenden Tabelle werden die sechs Spalten in der Statusansicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="af36f-117">The following table describes the six columns in the status view.</span></span>

    

    | <span data-ttu-id="af36f-118">Column</span><span class="sxs-lookup"><span data-stu-id="af36f-118">Column</span></span>                        | <span data-ttu-id="af36f-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af36f-119">Description</span></span>                                                                                                                                                                                                                |
    |-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="af36f-120">**ProgID**</span><span class="sxs-lookup"><span data-stu-id="af36f-120">**ProgID**</span></span><br/>         | <span data-ttu-id="af36f-121">Identifiziert eine bestimmte Komponente.</span><span class="sxs-lookup"><span data-stu-id="af36f-121">Identifies a specific component.</span></span><br/>                                                                                                                                                                                |
    | <span data-ttu-id="af36f-122">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="af36f-122">**Objects**</span></span><br/>        | <span data-ttu-id="af36f-123">Zeigt die Anzahl der Objekte an, die zurzeit von Client verweisen aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="af36f-123">Shows the number of objects that are currently held by client references.</span></span><br/>                                                                                                                                       |
    | <span data-ttu-id="af36f-124">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="af36f-124">**Activated**</span></span><br/>      | <span data-ttu-id="af36f-125">Zeigt die Anzahl der Objekte an, die derzeit aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="af36f-125">Shows the number of objects that are currently activated.</span></span> <br/>                                                                                                                                                      |
    | <span data-ttu-id="af36f-126">**Pool**</span><span class="sxs-lookup"><span data-stu-id="af36f-126">**Pooled**</span></span><br/>         | <span data-ttu-id="af36f-127">Zeigt die Gesamtanzahl der Objekte, die vom Pool erstellt wurden, einschließlich verwenener Objekte und deaktivierter Objekte.</span><span class="sxs-lookup"><span data-stu-id="af36f-127">Shows the total number of objects created by the pool, including objects that are in use and objects that are deactivated.</span></span><br/>                                                                                      |
    | <span data-ttu-id="af36f-128">**Im-Befehl**</span><span class="sxs-lookup"><span data-stu-id="af36f-128">**In Call**</span></span><br/>        | <span data-ttu-id="af36f-129">Identifiziert Objekte im-Befehl.</span><span class="sxs-lookup"><span data-stu-id="af36f-129">Identifies objects in call.</span></span><br/>                                                                                                                                                                                     |
    | <span data-ttu-id="af36f-130">**Aufruf Zeit (MS)**</span><span class="sxs-lookup"><span data-stu-id="af36f-130">**Call Time (ms)**</span></span><br/> | <span data-ttu-id="af36f-131">Zeigt die durchschnittliche Aufruf Dauer (in Millisekunden) der in den letzten 20 Sekunden (bis zu 20 aufrufen) erfolgten Methodenaufrufe an.</span><span class="sxs-lookup"><span data-stu-id="af36f-131">Shows the average call duration (in milliseconds) of method calls made in the last 20 seconds (up to 20 calls).</span></span> <span data-ttu-id="af36f-132">Die Aufruf Zeit wird beim Objekt gemessen und umfasst nicht die Zeit, die zum Durchlaufen des Netzwerks verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="af36f-132">Call time is measured at the object and does not include the time used to traverse the network.</span></span><br/> |

    

     

## <a name="related-topics"></a><span data-ttu-id="af36f-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af36f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af36f-134">Konfigurieren einer Komponente, die in einem Pool zusammengefasst werden soll</span><span class="sxs-lookup"><span data-stu-id="af36f-134">Configuring a Component to Be Pooled</span></span>](configuring-a-component-to-be-pooled.md)
</dt> </dl>

 

 




