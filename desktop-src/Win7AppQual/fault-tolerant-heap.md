---
description: Fehlertoleranter Heap
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Fehlertoleranter Heap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17ab2630e6dc28cb84604e48be1aa60bf208a97
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088398"
---
# <a name="fault-tolerant-heap"></a><span data-ttu-id="cb781-103">Fehlertoleranter Heap</span><span class="sxs-lookup"><span data-stu-id="cb781-103">Fault Tolerant Heap</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="cb781-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="cb781-104">Affected Platforms</span></span>

<span data-ttu-id="cb781-105">**Clients:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="cb781-105">**Clients -** Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="cb781-106">Auswirkung von Features</span><span class="sxs-lookup"><span data-stu-id="cb781-106">Feature Impact</span></span>

 <span data-ttu-id="cb781-107">**Schweregrad:** Mittel</span><span class="sxs-lookup"><span data-stu-id="cb781-107">**Severity -** Medium</span></span>  
<span data-ttu-id="cb781-108">**Häufigkeit:** Niedrig</span><span class="sxs-lookup"><span data-stu-id="cb781-108">**Frequency -** Low</span></span>  


## <a name="description"></a><span data-ttu-id="cb781-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb781-109">Description</span></span>

<span data-ttu-id="cb781-110">Der fehlertolerante Heap (Fault Tolerant Heap, FTH) ist ein Subsystem von Windows 7, das für die Überwachung von Anwendungsabstürzen und die autonome Anwendung von Entschärfungen verantwortlich ist, um zukünftige Abstürze pro Anwendung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="cb781-110">The Fault Tolerant Heap (FTH) is a subsystem of Windows 7 responsible for monitoring application crashes and autonomously applying mitigations to prevent future crashes on a per application basis.</span></span> <span data-ttu-id="cb781-111">Für die überwiegende Mehrheit der Benutzer funktioniert FTH ohne Eingreifen oder Änderung.</span><span class="sxs-lookup"><span data-stu-id="cb781-111">For the vast majority of users, FTH will function with no need for intervention or change on their part.</span></span> <span data-ttu-id="cb781-112">In einigen Fällen müssen Anwendungsentwickler und Softwaretester jedoch möglicherweise das Standardverhalten dieses Systems außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="cb781-112">However, in some cases, application developers and software testers may need to override the default behavior of this system.</span></span>

## <a name="solution"></a><span data-ttu-id="cb781-113">Lösung</span><span class="sxs-lookup"><span data-stu-id="cb781-113">Solution</span></span>

<span data-ttu-id="cb781-114">**Anzeigen der Fehlertoleranten Heapaktivität**</span><span class="sxs-lookup"><span data-stu-id="cb781-114">**Viewing Fault Tolerant Heap activity**</span></span>

<span data-ttu-id="cb781-115">Fehlertoleranter Heap protokolliert Informationen, wenn der Dienst gestartet, beendet oder damit beginnt, Probleme für eine neue Anwendung zu beheben.</span><span class="sxs-lookup"><span data-stu-id="cb781-115">Fault Tolerant Heap logs information when the service starts, stops, or starts mitigating problems for a new application.</span></span> <span data-ttu-id="cb781-116">Führen Sie die folgenden Schritte aus, um diese Informationen anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="cb781-116">To view this information, follow these steps:</span></span>

1.  <span data-ttu-id="cb781-117">Klicken Sie auf das Startmenü.</span><span class="sxs-lookup"><span data-stu-id="cb781-117">Click the Start menu.</span></span>
2.  <span data-ttu-id="cb781-118">Klicken Sie mit der rechten **Maustaste auf Computer,** und klicken Sie **auf Verwalten.**</span><span class="sxs-lookup"><span data-stu-id="cb781-118">Right-click **Computer** and click **Manage**.</span></span>
3.  <span data-ttu-id="cb781-119">Klicken **Ereignisanzeige**  >  **auf Anwendungs- und Dienstprotokolle**  >  **Microsoft** Windows  >  **> Fehlertoleranter Heap**</span><span class="sxs-lookup"><span data-stu-id="cb781-119">Click **Event Viewer** > **Applications and Services Logs** > **Microsoft** > **Windows > Fault-Tolerant-Heap**</span></span>
4.  <span data-ttu-id="cb781-120">Zeigen Sie FTH-Ereignisse an.</span><span class="sxs-lookup"><span data-stu-id="cb781-120">View FTH Events.</span></span>

<span data-ttu-id="cb781-121">Die Ereignisse zum Beenden und Starten des Diensts enthalten keine zusätzlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="cb781-121">The service stop and start events contain no additional data.</span></span> <span data-ttu-id="cb781-122">Das FTH Enabled-Ereignis enthält die Prozess-ID (PID), den Prozessimagenamen und die Startzeit der Prozessinstanz.</span><span class="sxs-lookup"><span data-stu-id="cb781-122">The FTH Enabled event contains the Process ID (PID), the process image name, and the process instance start time.</span></span>

<span data-ttu-id="cb781-123">**Deaktivieren des fehlertoleranten Heaps**</span><span class="sxs-lookup"><span data-stu-id="cb781-123">**Disabling Fault Tolerant Heap**</span></span>

<span data-ttu-id="cb781-124">**Vorsicht** Schwerwiegende Probleme können auftreten, wenn Sie die Registrierung falsch ändern, indem Sie den Registrierungs-Editor oder eine andere Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="cb781-124">**Caution** Serious problems may occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="cb781-125">Diese Probleme erfordern möglicherweise, dass Sie das Betriebssystem neu installieren.</span><span class="sxs-lookup"><span data-stu-id="cb781-125">These problems may require you to reinstall the operating system.</span></span> <span data-ttu-id="cb781-126">Microsoft garantiert nicht, dass diese Probleme behoben werden können.</span><span class="sxs-lookup"><span data-stu-id="cb781-126">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="cb781-127">Das Bearbeiten der Registrierung erfolgt auf eigenes Risiko.</span><span class="sxs-lookup"><span data-stu-id="cb781-127">Modify the registry at your own risk.</span></span>  
 <span data-ttu-id="cb781-128">Um den fehlertoleranten Heap vollständig auf einem System zu deaktivieren, legen Sie den REG \_ DWORD-Wert **HKLM \\ Software Microsoft \\ \\ FTH \\ Enabled** auf **0** fest.</span><span class="sxs-lookup"><span data-stu-id="cb781-128">To disable Fault Tolerant Heap entirely on a system, set the REG\_DWORD value **HKLM\\Software\\Microsoft\\FTH\\Enabled** to **0**.</span></span>

<span data-ttu-id="cb781-129">Starten Sie das System nach dem Ändern dieses Werts neu.</span><span class="sxs-lookup"><span data-stu-id="cb781-129">After changing this value, restart the system.</span></span> <span data-ttu-id="cb781-130">Die FTH wird für neue Anwendungen nicht mehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cb781-130">FTH will no longer activate for new applications.</span></span>

<span data-ttu-id="cb781-131">**Zurücksetzen der Liste der anwendungen, die von der FTH nachverfolgt werden**</span><span class="sxs-lookup"><span data-stu-id="cb781-131">**Resetting the list of applications tracked by FTH**</span></span>

<span data-ttu-id="cb781-132">Der fehlertolerante Heap verwaltet sich selbst und beendet die Anwendung autonom, falls entschärfte Maßnahmen für eine bestimmte Anwendung nicht wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="cb781-132">Fault Tolerant heap is self-managing and will autonomously stop applying in the case that mitigations are not effective for a given application.</span></span> <span data-ttu-id="cb781-133">Wenn Sie jedoch die Liste der Anwendungen zurücksetzen müssen, für die die FTH Probleme mindert (z. B. wenn Sie eine Anwendung testen und einen Absturz reproduzieren müssen, den die FTH mindert), können Sie den folgenden Befehl an einer Eingabeaufforderung mit erhöhten Rechten ausführen:  **Rundll32.exe fthsvc.dll,FthSysprepSpecialize**</span><span class="sxs-lookup"><span data-stu-id="cb781-133">However, if you need to reset the list of applications for which FTH is mitigating problems (for example, if you are testing an application and need to reproduce a crash that FTH is mitigating), you can run the following command from an elevated command prompt:  **Rundll32.exe fthsvc.dll,FthSysprepSpecialize**</span></span>  
<span data-ttu-id="cb781-134">**Vorsicht** Wenn Sie diesen Befehl ausführen, werden alle FTH-Anwendungen gelöscht, sodass Anwendungen, die derzeit ordnungsgemäß funktionieren, nach dem Ausführen dieses Befehls möglicherweise erneut abstürzt.</span><span class="sxs-lookup"><span data-stu-id="cb781-134">**Caution** Running this command will clear all FTH applications, so applications that are currently functioning properly may begin to crash again after running this command.</span></span>  

 

 



