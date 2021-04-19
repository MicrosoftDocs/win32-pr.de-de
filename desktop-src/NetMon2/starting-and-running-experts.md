---
description: Wenn Sie im expertenfenster der Netzwerkmonitor-Benutzeroberfläche auf Experten ausführen klicken, werden die für die Erfassungs Datei ausgewählten Experten gestartet und die Run-Funktion aufgerufen. Wenn der Experte gestartet wird, analysiert er die Erfassungs Datei mithilfe mehrerer expertenframe-Funktionen.
ms.assetid: 6b8a66cb-d1d6-4e19-b668-049a03a40804
title: Starten und Ausführen von Experten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bd41472d286727541d26bade1942eb3b6b5c593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366298"
---
# <a name="starting-and-running-experts"></a><span data-ttu-id="5effe-104">Starten und Ausführen von Experten</span><span class="sxs-lookup"><span data-stu-id="5effe-104">Starting and Running Experts</span></span>

<span data-ttu-id="5effe-105">Wenn Sie im expertenfenster der Netzwerkmonitor-Benutzeroberfläche auf **Experten ausführen** klicken, werden die für die Erfassungs Datei ausgewählten Experten gestartet und die [**Run**](run.md) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5effe-105">Clicking **Run Experts** from the Experts window of the Network Monitor UI starts the experts selected for the capture file and calls the [**Run**](run.md) function.</span></span> <span data-ttu-id="5effe-106">Wenn der Experte gestartet wird, analysiert er die Erfassungs Datei mithilfe mehrerer expertenframe-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="5effe-106">When started, the expert analyzes the capture file by using several expert frame functions.</span></span>

<span data-ttu-id="5effe-107">Die Funktion " [**expertindikatestatus**](expertindicatestatus.md) " stellt Statusinformationen vom Experten bereit.</span><span class="sxs-lookup"><span data-stu-id="5effe-107">The [**ExpertIndicateStatus**](expertindicatestatus.md) function provides status information from the expert.</span></span> <span data-ttu-id="5effe-108">Wenn Sie einen Experten mit Netzwerkmonitor ausführen, zeigt das Fenster "expertenstatusansicht" regelmäßig aktualisierte Statusinformationen an (von 0 bis 100 Prozent).</span><span class="sxs-lookup"><span data-stu-id="5effe-108">When you run an expert with Network Monitor, the Expert Status View window displays periodically updated status information (from 0 to 100 percent completion).</span></span>

![Fenster "expertenstatusansicht"](images/exview.png)

<span data-ttu-id="5effe-110">Der Experte ist aktiv, bis die Daten durch die Erfassungs Datei abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="5effe-110">The expert is active until the data completes its pass though the capture file.</span></span> <span data-ttu-id="5effe-111">Wenn der Durchlauf abgeschlossen ist, wird ein Ereignisanzeige Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5effe-111">When the pass is complete, an Event Viewer window appears.</span></span> <span data-ttu-id="5effe-112">Die Informationen in diesem Fenster hängen von der Art des Experten ab, der die Daten analysiert hat.</span><span class="sxs-lookup"><span data-stu-id="5effe-112">The information in this window depends on the type of expert that analyzed the data.</span></span> <span data-ttu-id="5effe-113">Die folgende Abbildung zeigt eine Expertenansicht für die Eigenschaften Verteilung, in der die vom Experten analysierten Frame Daten zusammengefasst werden.</span><span class="sxs-lookup"><span data-stu-id="5effe-113">The following illustration shows a Property Distribution Expert view, which summarizes the frame data that the expert analyzed.</span></span>

![Expertenansicht für die Eigenschaften Verteilung](images/exview1.png)

<span data-ttu-id="5effe-115">Ein zweiter Bericht (nicht angezeigt) fasst die Ergebnisse der Übertragung des Transmission Control Protocol (TCP)-Neuübertragungs-Experten zusammen.</span><span class="sxs-lookup"><span data-stu-id="5effe-115">A second report (not shown), summarizes the results of the Transmission Control Protocol (TCP) Retransmit expert.</span></span>

<span data-ttu-id="5effe-116">Sie können außerdem:</span><span class="sxs-lookup"><span data-stu-id="5effe-116">You can also:</span></span>

-   <span data-ttu-id="5effe-117">Erstellen Sie einen Eintrag für eine Ereignis Referenzseite (ERP), die dem Benutzer die erkannten Bedingungen oder Probleme (wie im Analysefenster angezeigt) rät.</span><span class="sxs-lookup"><span data-stu-id="5effe-117">Create an entry for an event reference page (ERP) that advises the user of detected conditions or problems (as shown in the Analysis window).</span></span>
-   <span data-ttu-id="5effe-118">Erstellen Sie Einträge für vorgeschlagene Korrekturen oder erläuternde Daten, die zusätzliche Informationen bereitstellen (wie im Fenster Auflösung angezeigt).</span><span class="sxs-lookup"><span data-stu-id="5effe-118">Create entries for suggested fixes or explanatory data that provide additional information (as shown in the Resolution window).</span></span>

<span data-ttu-id="5effe-119">Nachdem der Experte seine Aufgabe abgeschlossen hat, Netzwerkmonitor den Experten aus dem aktiven Speicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="5effe-119">After the expert completes its task, Network Monitor removes the expert from active memory.</span></span> <span data-ttu-id="5effe-120">Experten sollten die geschützten Speicherfunktionen verwenden, die im Platform Software Development Kit (SDK) enthalten sind. Diese Funktionen bereinigen den Arbeitsspeicher, wenn die Experten während der Laufzeit fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="5effe-120">Experts should use the protected memory functions included in the Platform Software Development Kit (SDK); these functions clean up memory if the experts fail during run time.</span></span>

 

 



