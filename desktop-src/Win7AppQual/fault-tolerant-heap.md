---
description: .
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Fehlertoleranter Heap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349c8c3d6d066de3d563880c169c8dde2e062370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352578"
---
# <a name="fault-tolerant-heap"></a><span data-ttu-id="f0dd2-103">Fehlertoleranter Heap</span><span class="sxs-lookup"><span data-stu-id="f0dd2-103">Fault Tolerant Heap</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="f0dd2-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="f0dd2-104">Affected Platforms</span></span>

<span data-ttu-id="f0dd2-105">**Clients:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="f0dd2-105">**Clients -** Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="f0dd2-106">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="f0dd2-106">Feature Impact</span></span>

 <span data-ttu-id="f0dd2-107">**Schweregrad:** Mittelalter</span><span class="sxs-lookup"><span data-stu-id="f0dd2-107">**Severity -** Medium</span></span>  
<span data-ttu-id="f0dd2-108">**Häufigkeit:** Preis</span><span class="sxs-lookup"><span data-stu-id="f0dd2-108">**Frequency -** Low</span></span>  


## <a name="description"></a><span data-ttu-id="f0dd2-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0dd2-109">Description</span></span>

<span data-ttu-id="f0dd2-110">Der Fault-tolerante Heap (Fth) ist ein Subsystem von Windows 7, das für die Überwachung von Anwendungs abstürzen und das autonome Anwenden von entschärfungen verantwortlich ist, um zukünftige Abstürze auf Anwendungs Basis zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-110">The Fault Tolerant Heap (FTH) is a subsystem of Windows 7 responsible for monitoring application crashes and autonomously applying mitigations to prevent future crashes on a per application basis.</span></span> <span data-ttu-id="f0dd2-111">Bei den meisten Benutzern funktioniert Fth ohne Eingriff oder Änderung an Ihrem Teil.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-111">For the vast majority of users, FTH will function with no need for intervention or change on their part.</span></span> <span data-ttu-id="f0dd2-112">In einigen Fällen müssen Anwendungsentwickler und Software Tester das Standardverhalten dieses Systems jedoch möglicherweise außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-112">However, in some cases, application developers and software testers may need to override the default behavior of this system.</span></span>

## <a name="solution"></a><span data-ttu-id="f0dd2-113">Lösung</span><span class="sxs-lookup"><span data-stu-id="f0dd2-113">Solution</span></span>

<span data-ttu-id="f0dd2-114">**Anzeigen der fehlertoleranten Heap Aktivität**</span><span class="sxs-lookup"><span data-stu-id="f0dd2-114">**Viewing Fault Tolerant Heap activity**</span></span>

<span data-ttu-id="f0dd2-115">Der fehlertolerante Heap protokolliert Informationen, wenn der Dienst die Probleme für eine neue Anwendung startet, beendet oder damit beginnt.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-115">Fault Tolerant Heap logs information when the service starts, stops, or starts mitigating problems for a new application.</span></span> <span data-ttu-id="f0dd2-116">Führen Sie die folgenden Schritte aus, um diese Informationen anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="f0dd2-116">To view this information, follow these steps:</span></span>

1.  <span data-ttu-id="f0dd2-117">Klicken Sie auf das Startmenü.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-117">Click the Start menu.</span></span>
2.  <span data-ttu-id="f0dd2-118">Klicken Sie mit der rechten Maustaste auf **Computer** , **und klicken Sie**</span><span class="sxs-lookup"><span data-stu-id="f0dd2-118">Right-click **Computer** and click **Manage**.</span></span>
3.  <span data-ttu-id="f0dd2-119">Klicken Sie auf **Ereignisanzeige**  >  **Anwendungs-und Dienst Protokolle**  >  **Microsoft**  >  **Windows > Fault-toleranter Heap**</span><span class="sxs-lookup"><span data-stu-id="f0dd2-119">Click **Event Viewer** > **Applications and Services Logs** > **Microsoft** > **Windows > Fault-Tolerant-Heap**</span></span>
4.  <span data-ttu-id="f0dd2-120">Anzeigen von Fth-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-120">View FTH Events.</span></span>

<span data-ttu-id="f0dd2-121">Die Dienst-und Start Ereignisse enthalten keine zusätzlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-121">The service stop and start events contain no additional data.</span></span> <span data-ttu-id="f0dd2-122">Das Ereignis "Fth-aktiviert" enthält die Prozess-ID (PID), den Prozess Image Namen und die Startzeit der Prozess Instanz.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-122">The FTH Enabled event contains the Process ID (PID), the process image name, and the process instance start time.</span></span>

<span data-ttu-id="f0dd2-123">**Deaktivieren des fehlertoleranten Heaps**</span><span class="sxs-lookup"><span data-stu-id="f0dd2-123">**Disabling Fault Tolerant Heap**</span></span>

<span data-ttu-id="f0dd2-124">**Vorsicht** Schwerwiegende Probleme können auftreten, wenn Sie die Registrierung falsch ändern, indem Sie den Registrierungs-Editor oder eine andere Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-124">**Caution** Serious problems may occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="f0dd2-125">Diese Probleme müssen möglicherweise eine Neuinstallation des Betriebssystems erforderlich machen.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-125">These problems may require you to reinstall the operating system.</span></span> <span data-ttu-id="f0dd2-126">Microsoft garantiert nicht, dass diese Probleme behoben werden können.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-126">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="f0dd2-127">Das Bearbeiten der Registrierung erfolgt auf eigenes Risiko.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-127">Modify the registry at your own risk.</span></span>  
 <span data-ttu-id="f0dd2-128">Um den fehlertoleranten Heap vollständig auf einem System zu deaktivieren, legen Sie den reg \_ DWORD-Wert **HKLM \\ Software \\ Microsoft \\ Fth \\ aktiviert** auf **0** fest.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-128">To disable Fault Tolerant Heap entirely on a system, set the REG\_DWORD value **HKLM\\Software\\Microsoft\\FTH\\Enabled** to **0**.</span></span>

<span data-ttu-id="f0dd2-129">Nachdem Sie diesen Wert geändert haben, starten Sie das System neu.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-129">After changing this value, restart the system.</span></span> <span data-ttu-id="f0dd2-130">Fth wird für neue Anwendungen nicht mehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-130">FTH will no longer activate for new applications.</span></span>

<span data-ttu-id="f0dd2-131">**Zurücksetzen der Liste der von Fth verfolgten Anwendungen**</span><span class="sxs-lookup"><span data-stu-id="f0dd2-131">**Resetting the list of applications tracked by FTH**</span></span>

<span data-ttu-id="f0dd2-132">Der fehlertolerante Heap ist selbst verwalterlos und wird autonom angehalten, wenn die entschärfungen für eine bestimmte Anwendung nicht wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-132">Fault Tolerant heap is self-managing and will autonomously stop applying in the case that mitigations are not effective for a given application.</span></span> <span data-ttu-id="f0dd2-133">Wenn Sie jedoch die Liste der Anwendungen zurücksetzen müssen, für die bei der Verwendung von Fth Probleme auftreten (z. b. Wenn Sie eine Anwendung testen und einen Absturz reproduzieren müssen, der von Fth verringert wird), können Sie den folgenden Befehl an einer Eingabeaufforderung mit erhöhten Rechten ausführen:  **Rundll32.exe fthsvc.dll, fthsyspree pspezialisiert**</span><span class="sxs-lookup"><span data-stu-id="f0dd2-133">However, if you need to reset the list of applications for which FTH is mitigating problems (for example, if you are testing an application and need to reproduce a crash that FTH is mitigating), you can run the following command from an elevated command prompt:  **Rundll32.exe fthsvc.dll,FthSysprepSpecialize**</span></span>  
<span data-ttu-id="f0dd2-134">**Vorsicht** Wenn Sie diesen Befehl ausführen, werden alle Fth-Anwendungen gelöscht, sodass Anwendungen, die zurzeit ordnungsgemäß funktionieren, nach dem Ausführen dieses Befehls wieder abstürzen können.</span><span class="sxs-lookup"><span data-stu-id="f0dd2-134">**Caution** Running this command will clear all FTH applications, so applications that are currently functioning properly may begin to crash again after running this command.</span></span>  

 

 



