---
description: Es gibt im wesentlichen keine Einschränkungen, wie eine Autorun-Start Anwendung geschrieben werden kann.
ms.assetid: 6D95E5F0-8D93-47A8-9D8C-49CBDCA150A7
title: Implementieren von Autorun-Start Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b553e102f574835103898b17558541000633412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959693"
---
# <a name="how-to-implement-autorun-startup-applications"></a><span data-ttu-id="d2c75-103">Implementieren von Autorun-Start Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d2c75-103">How to Implement AutoRun Startup Applications</span></span>

<span data-ttu-id="d2c75-104">Es gibt im wesentlichen keine Einschränkungen, wie eine Autorun-Start Anwendung geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="d2c75-104">There are essentially no constraints on how to write an AutoRun startup application.</span></span> <span data-ttu-id="d2c75-105">Sie können die Start Anwendung so implementieren, dass Sie alle erforderlichen Schritte zum Installieren, deinstallieren, konfigurieren oder Ausführen der Anwendung ausführen können.</span><span class="sxs-lookup"><span data-stu-id="d2c75-105">You can implement the startup application to do whatever you find necessary to install, uninstall, configure, or run your application.</span></span> <span data-ttu-id="d2c75-106">Die folgenden Tipps bieten jedoch einige Richtlinien für die Implementierung einer effektiven Autorun-Start Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d2c75-106">However, the following tips provide some guidelines to implementing an effective AutoRun startup application.</span></span>

## <a name="instructions"></a><span data-ttu-id="d2c75-107">Instructions</span><span class="sxs-lookup"><span data-stu-id="d2c75-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="d2c75-108">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="d2c75-108">Step 1:</span></span>

<span data-ttu-id="d2c75-109">Stellen Sie sicher, dass Benutzer Feedback so schnell wie möglich erhalten, nachdem Sie eine Autorun-CD in das Laufwerk eingefügt haben.</span><span class="sxs-lookup"><span data-stu-id="d2c75-109">Make sure that users receive feedback as soon as possible after they insert an AutoRun disc into the drive.</span></span> <span data-ttu-id="d2c75-110">Start Anwendungen sollten kleine Programme sein, die schnell geladen werden.</span><span class="sxs-lookup"><span data-stu-id="d2c75-110">Startup applications should be small programs that load quickly.</span></span> <span data-ttu-id="d2c75-111">Sie sollten die Anwendung eindeutig identifizieren und eine einfache Möglichkeit bereitstellen, um den Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="d2c75-111">They should clearly identify the application and provide an easy way to cancel the operation.</span></span>

### <a name="step-2"></a><span data-ttu-id="d2c75-112">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="d2c75-112">Step 2:</span></span>

<span data-ttu-id="d2c75-113">Überprüfen Sie, ob das Programm bereits installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d2c75-113">Check to see if the program is already installed.</span></span> <span data-ttu-id="d2c75-114">Wenn dies nicht der Fall ist, ist der nächste Schritt wahrscheinlich die Setup Prozedur.</span><span class="sxs-lookup"><span data-stu-id="d2c75-114">If not, the next step will probably be the setup procedure.</span></span> <span data-ttu-id="d2c75-115">Die Start Anwendung kann die Zeit nutzen, die der Benutzer beim Lesen des Dialog Felds verbringt, indem er einen anderen Thread startet, um mit dem Laden des Setup Codes zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="d2c75-115">The startup application can take advantage of the time the user spends reading the dialog box by starting another thread to begin loading the setup code.</span></span> <span data-ttu-id="d2c75-116">Wenn der Benutzer auf **OK** klickt, wird das Setup Programm bereits teilweise, wenn es nicht vollständig geladen ist, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2c75-116">By the time the user clicks **OK**, your setup program will already be partly if not fully loaded.</span></span> <span data-ttu-id="d2c75-117">Mit diesem Ansatz wird die Wahrnehmung des Benutzers für das Laden Ihrer Anwendung erheblich reduziert.</span><span class="sxs-lookup"><span data-stu-id="d2c75-117">This approach significantly reduces the user's perception of the amount of time it takes to load your application.</span></span>

> [!Note]  
> <span data-ttu-id="d2c75-118">Der erste Teil der Start Anwendung zeigt Benutzern in der Regel eine Benutzeroberfläche, z. b. ein Dialogfeld, in der Sie gefragt werden, wie Sie fortfahren möchten.</span><span class="sxs-lookup"><span data-stu-id="d2c75-118">Typically, the initial part of the startup application presents users with a user interface, such as a dialog box, asking them how they would like to proceed.</span></span>

 

### <a name="step-3"></a><span data-ttu-id="d2c75-119">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="d2c75-119">Step 3:</span></span>

<span data-ttu-id="d2c75-120">Starten Sie einen weiteren Thread, um das Laden des Anwendungs Codes zu beginnen, um die Wartezeit für den Benutzer zu verkürzen.</span><span class="sxs-lookup"><span data-stu-id="d2c75-120">Start another thread to begin loading application code to shorten the waiting time for the user.</span></span> <span data-ttu-id="d2c75-121">Wenn die Anwendung bereits installiert wurde, wurde der Datenträger vom Benutzer wahrscheinlich zum Ausführen der Anwendung eingefügt.</span><span class="sxs-lookup"><span data-stu-id="d2c75-121">If the application has already been installed, the user probably inserted the disk to run the application.</span></span>

### <a name="step-4"></a><span data-ttu-id="d2c75-122">Schritt 4:</span><span class="sxs-lookup"><span data-stu-id="d2c75-122">Step 4:</span></span>

<span data-ttu-id="d2c75-123">Verwenden Sie die folgenden Hinweise, um die Festplattennutzung zu minimieren:</span><span class="sxs-lookup"><span data-stu-id="d2c75-123">Use the following hints to minimize hard disk usage:</span></span>

-   <span data-ttu-id="d2c75-124">Halten Sie die Anzahl der Dateien, die sich auf der Festplatte befinden müssen, auf einen minimalen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="d2c75-124">Keep the number of files that must be on the hard disk to a minimum.</span></span> <span data-ttu-id="d2c75-125">Sie sollten auf Dateien beschränkt werden, die für die Ausführung des Programms von entscheidender Bedeutung sind, oder die einen unzulässigen Zeitaufwand für das Lesen von Medien benötigen.</span><span class="sxs-lookup"><span data-stu-id="d2c75-125">They should be restricted to files that are essential to running the program or that would take an unacceptably large amount of time to read from the media.</span></span>
-   <span data-ttu-id="d2c75-126">In vielen Fällen ist es nicht erforderlich, nicht erforderliche Dateien auf der Festplatte zu installieren, bietet jedoch möglicherweise Vorteile, z. b. eine bessere Leistung.</span><span class="sxs-lookup"><span data-stu-id="d2c75-126">In many cases, installing nonessential files on the hard disk is not necessary, but might provide benefits such as increased performance.</span></span> <span data-ttu-id="d2c75-127">Geben Sie dem Benutzer die Möglichkeit, zu entscheiden, wie Sie den Kompromiss zwischen den Kosten und den Vorteilen der Festplatten Speicherung treffen möchten.</span><span class="sxs-lookup"><span data-stu-id="d2c75-127">Give the user the option of deciding how to make the trade-off between the costs and benefits of hard disk storage.</span></span>
-   <span data-ttu-id="d2c75-128">Bietet eine Möglichkeit, alle Komponenten zu deinstallieren, die auf der Festplatte platziert wurden.</span><span class="sxs-lookup"><span data-stu-id="d2c75-128">Provide a way to uninstall any components that were placed on the hard disk.</span></span>
-   <span data-ttu-id="d2c75-129">Wenn Ihre Anwendung Daten zwischenspeichert, können Sie dem Benutzer eine gewisse Kontrolle über die Anwendung einräumen.</span><span class="sxs-lookup"><span data-stu-id="d2c75-129">If your application caches data, give the user some control over it.</span></span> <span data-ttu-id="d2c75-130">Schließen Sie Optionen in die Start Anwendung ein, z. b. das Festlegen einer Beschränkung für die maximale Menge an zwischengespeicherten Daten, die auf der Festplatte gespeichert werden, oder das Verwerfen von zwischengespeicherten Daten durch die Anwendung, wenn diese beendet wird.</span><span class="sxs-lookup"><span data-stu-id="d2c75-130">Include options in the startup application such as setting a limit on the maximum amount of cached data that will be stored on the hard disk, or having the application discard any cached data when it terminates.</span></span>

### <a name="step-5"></a><span data-ttu-id="d2c75-131">Schritt 5:</span><span class="sxs-lookup"><span data-stu-id="d2c75-131">Step 5:</span></span>

<span data-ttu-id="d2c75-132">Deaktivieren Sie bei Bedarf Autorun.</span><span class="sxs-lookup"><span data-stu-id="d2c75-132">Disable Autorun if needed.</span></span> <span data-ttu-id="d2c75-133">Autorun kann entweder Programm gesteuert oder vollständig mit der Registrierung unterdrückt werden, auch wenn ein Medium über eine Autorun. inf-Datei verfügt.</span><span class="sxs-lookup"><span data-stu-id="d2c75-133">AutoRun can be suppressed programmatically or disabled entirely with the registry, even when a medium has an Autorun.inf file.</span></span> <span data-ttu-id="d2c75-134">Weitere Informationen finden Sie unter [aktivieren und Deaktivieren von Autorun](autoplay-reg.md) .</span><span class="sxs-lookup"><span data-stu-id="d2c75-134">See [Enabling and Disabling AutoRun](autoplay-reg.md) for more information.</span></span>

 

 



