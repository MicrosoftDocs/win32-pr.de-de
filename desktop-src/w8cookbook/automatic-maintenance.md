---
title: Automatische Wartung (Compatibility Cookbook für Windows)
description: Automatische Wartung
ms.assetid: D3B61105-D118-42A4-8F3D-ED92EFAF597F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320625fa0ac8e56368396a7f1be88def0ac3c526
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104474501"
---
# <a name="automatic-maintenance"></a><span data-ttu-id="f2abe-103">Automatische Wartung</span><span class="sxs-lookup"><span data-stu-id="f2abe-103">Automatic Maintenance</span></span>

## <a name="platforms"></a><span data-ttu-id="f2abe-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="f2abe-104">Platforms</span></span>

<span data-ttu-id="f2abe-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="f2abe-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="f2abe-106">**Server** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2abe-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="f2abe-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2abe-107">Description</span></span>

<span data-ttu-id="f2abe-108">Windows ist abhängig von der Ausführung von Posteingang und der Wartung von Drittanbietern für einen Großteil des Werts: Add, einschließlich Windows Update und automatischer Datenträger Defragmentierung sowie von Antivirenaktualisierungen und-Scans.</span><span class="sxs-lookup"><span data-stu-id="f2abe-108">Windows depends on execution of inbox and third party maintenance activity for much of its value-add, including Windows Update, and automatic disk defragmentation, as well as antivirus updates and scans.</span></span> <span data-ttu-id="f2abe-109">Außerdem verwenden Unternehmen häufig Wartungsaktivitäten, z. b. NAP-Scans (Network Access Protection, Netzwerk Zugriffsschutz), um Sicherheitsstandards auf allen Unternehmens Arbeitsstationen zu erzwingen</span><span class="sxs-lookup"><span data-stu-id="f2abe-109">Additionally, enterprises frequently use maintenance activity such as Network Access Protection (NAP) scanning to help enforce security standards on all enterprise workstations.</span></span>

<span data-ttu-id="f2abe-110">Wartungsaktivitäten in Windows sind für die Ausführung im Hintergrund mit eingeschränkter Benutzerinteraktion und minimaler Auswirkung auf die Leistung und Energieeffizienz vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="f2abe-110">Maintenance activity in Windows is designed to run in the background with limited user interaction and minimal impact to performance and energy efficiency.</span></span> <span data-ttu-id="f2abe-111">In Windows 7 und früheren Versionen sind Leistung und Energieeffizienz jedoch weiterhin aufgrund des nicht deterministischen und sehr unterschiedlichen Zeitplans der verschiedenen Wartungsaktivitäten in Windows beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="f2abe-111">However, in Windows 7 and earlier versions, performance and energy efficiency are still impacted due to the non-deterministic and widely varied schedule of the multiple maintenance activities in Windows.</span></span> <span data-ttu-id="f2abe-112">Die Reaktionsfähigkeit für Benutzer wird verringert, wenn Wartungsaktivitäten ausgeführt werden, während Benutzer den Computer aktiv verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2abe-112">Responsiveness to users is reduced when maintenance activity runs while users are actively using the computer.</span></span> <span data-ttu-id="f2abe-113">Außerdem wird der Benutzer häufig aufgefordert, seine Software zu aktualisieren und die Hintergrund Wartung auszuführen und Benutzer an mehrere Benutzeroberflächen weiterzuleiten, einschließlich des Aktions Centers, der Systemsteuerung, der Windows Update, Taskplaner MMC-Snap-Ins und von Steuerelementen von Drittanbietern.</span><span class="sxs-lookup"><span data-stu-id="f2abe-113">Apps also frequently ask the user to update their software and run background maintenance, and direct users to multiple experiences, including Action Center, Control Panel, Windows Update, Task Scheduler MMC snap-in, and third-party controls.</span></span>

<span data-ttu-id="f2abe-114">Das Ziel der automatischen Wartung besteht darin, alle Hintergrund Wartungsaktivitäten in Windows zu kombinieren und Entwicklern von Drittanbietern zu helfen, ihre Wartungsaktivitäten zu Windows hinzuzufügen, ohne dass sich dies negativ auf die Leistung und Energieeffizienz auswirkt.</span><span class="sxs-lookup"><span data-stu-id="f2abe-114">The goal of Automatic Maintenance is to combine all background maintenance activity in Windows and help third-party developers add their maintenance activity to Windows without negatively impacting performance and energy efficiency.</span></span> <span data-ttu-id="f2abe-115">Außerdem ermöglicht die automatische Wartung Benutzern und Unternehmen die Kontrolle über die Planung und Konfiguration von Wartungsaktivitäten.</span><span class="sxs-lookup"><span data-stu-id="f2abe-115">Additionally, Automatic Maintenance enables users as well as enterprises to be in control of maintenance activity scheduling and configuration.</span></span>

<span data-ttu-id="f2abe-116">**Wichtige Probleme**</span><span class="sxs-lookup"><span data-stu-id="f2abe-116">**Key problems**</span></span>

<span data-ttu-id="f2abe-117">Die automatische Wartung ist so konzipiert, dass diese Probleme mit Wartungsaktivitäten in Windows behoben werden:</span><span class="sxs-lookup"><span data-stu-id="f2abe-117">Automatic Maintenance is designed to address these problems with maintenance activity in Windows:</span></span>

-   <span data-ttu-id="f2abe-118">Frist Planung</span><span class="sxs-lookup"><span data-stu-id="f2abe-118">Deadline scheduling</span></span>
-   <span data-ttu-id="f2abe-119">Ressourcen Verwendungs Konflikte</span><span class="sxs-lookup"><span data-stu-id="f2abe-119">Resource utilization conflicts</span></span>
-   <span data-ttu-id="f2abe-120">Energieeffizienz</span><span class="sxs-lookup"><span data-stu-id="f2abe-120">Energy efficiency</span></span>
-   <span data-ttu-id="f2abe-121">Transparenz für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="f2abe-121">Transparency to the user</span></span>

## <a name="functionality"></a><span data-ttu-id="f2abe-122">Funktionalität</span><span class="sxs-lookup"><span data-stu-id="f2abe-122">Functionality</span></span>

<span data-ttu-id="f2abe-123">Durch die automatische Wartung wird die Effizienz im Leerlauf vereinfacht, und alle Aktivitäten können rechtzeitig und priorisiert ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f2abe-123">Automatic Maintenance facilitates idle efficiency and permits all activity to run in a timely and prioritized fashion.</span></span> <span data-ttu-id="f2abe-124">Außerdem ermöglicht Sie eine einheitliche Sichtbarkeit und Kontrolle über Wartungsaktivitäten und ermöglicht Entwicklern von Drittanbietern, ihre Wartungsaktivitäten zu Windows hinzuzufügen, ohne dass sich dies negativ auf die Leistung und Energieeffizienz auswirkt.</span><span class="sxs-lookup"><span data-stu-id="f2abe-124">It also helps enable unified visibility and control over maintenance activity, and allows third-party developers to add their maintenance activity to Windows without negatively impacting performance and energy efficiency.</span></span> <span data-ttu-id="f2abe-125">Zu diesem Zweck bietet es einen vollständig automatischen Modus, den Benutzer initiierten Modus, automatische Beendigung, Termine und Benachrichtigung sowie die Kontrolle über das Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="f2abe-125">To do this, it provides a fully automatic mode, user-initiated mode, automatic stop, deadlines and notification, and enterprise control.</span></span> <span data-ttu-id="f2abe-126">Diese werden nachfolgend beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f2abe-126">These are each described below.</span></span>

<span data-ttu-id="f2abe-127">**Vollständig automatischer Modus**</span><span class="sxs-lookup"><span data-stu-id="f2abe-127">**Fully automatic mode**</span></span>

<span data-ttu-id="f2abe-128">Dieser Standardmodus ermöglicht eine intelligente Zeitplanung während der Leerlaufzeit von PCs und zu geplanten Zeiten – das Ausführen und automatische Anhalten von Wartungsaktivitäten ohne Benutzereingriff.</span><span class="sxs-lookup"><span data-stu-id="f2abe-128">This default mode enables intelligent scheduling during PC idle-time and at scheduled times—the execution and automatic pausing of maintenance activity without any user intervention.</span></span> <span data-ttu-id="f2abe-129">Der Benutzer kann einen wöchentlichen oder einen täglichen Zeitplan festlegen.</span><span class="sxs-lookup"><span data-stu-id="f2abe-129">The user can set a weekly or daily schedule.</span></span> <span data-ttu-id="f2abe-130">Alle Wartungsaktivitäten sind nicht interaktiv und werden automatisch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2abe-130">All maintenance activity is non-interactive and executes silently.</span></span>

<span data-ttu-id="f2abe-131">Wenn das System wahrscheinlich nicht in Gebrauch ist, wird der Computer automatisch wieder in den Standbymodus versetzt, und die Energie Verwaltungs Richtlinie, bei der es sich um Laptops handelt, wird standardmäßig nur aktiviert, wenn es sich um eine Stromversorgung handelt.</span><span class="sxs-lookup"><span data-stu-id="f2abe-131">The computer automatically is resumed from sleep when the system is not likely to be in use, respecting the Power Management policy, which in the case of laptops, defaults to allow wake-up only if it is on AC power.</span></span> <span data-ttu-id="f2abe-132">Vollständige Systemressourcen mit hoher Leistung werden verwendet, um die Wartungs Aktivität so schnell wie möglich abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f2abe-132">Full system resources at high power are used to complete the maintenance activity as quickly as possible.</span></span> <span data-ttu-id="f2abe-133">Wenn das System für die automatische Wartung aus dem Standbymodus wieder aufgenommen wurde, wird es in den Standbymodus versetzt.</span><span class="sxs-lookup"><span data-stu-id="f2abe-133">If the system was resumed from sleep for Automatic Maintenance, it is requested to return to sleep.</span></span>

<span data-ttu-id="f2abe-134">Alle erforderlichen Benutzerinteraktionen im Zusammenhang mit Aktivitäten, z. b. der Konfiguration, werden außerhalb der automatischen Wartungs Ausführung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2abe-134">Any required user interactions related to activities such as configuration are performed outside of Automatic Maintenance execution.</span></span>

<span data-ttu-id="f2abe-135">**Vom Benutzer initiierter Modus**</span><span class="sxs-lookup"><span data-stu-id="f2abe-135">**User-initiated mode**</span></span>

<span data-ttu-id="f2abe-136">Wenn Benutzer sich für eine längere Zeit vorbereiten müssen und sich für eine längere Zeit mit der Akkuleistung ausarbeiten möchten, können Sie die automatische Wartung bei Bedarf initiieren.</span><span class="sxs-lookup"><span data-stu-id="f2abe-136">If users need to prepare for travel, expect to be on battery power for a prolonged time, or wish to optimize for performance and responsiveness, they have the option of initiating Automatic Maintenance on demand.</span></span> <span data-ttu-id="f2abe-137">Benutzer können automatische Wartungs Attribute konfigurieren, einschließlich des automatischen Lauf Zeit Zeitplans.</span><span class="sxs-lookup"><span data-stu-id="f2abe-137">Users can configure Automatic Maintenance attributes, including the automatic run schedule.</span></span> <span data-ttu-id="f2abe-138">Sie können den aktuellen Status der automatischen Wartungs Ausführung anzeigen und die automatische Wartung bei Bedarf abbrechen.</span><span class="sxs-lookup"><span data-stu-id="f2abe-138">They can view the current status of Automatic Maintenance execution, and they can stop Automatic Maintenance if needed.</span></span>

<span data-ttu-id="f2abe-139">**Automatisches Abbrechen**</span><span class="sxs-lookup"><span data-stu-id="f2abe-139">**Automatic stop**</span></span>

<span data-ttu-id="f2abe-140">Durch die automatische Wartung werden die derzeit laufenden Wartungsaktivitäten automatisch beendet, wenn der Benutzer mit der Interaktion mit dem Computer beginnt.</span><span class="sxs-lookup"><span data-stu-id="f2abe-140">Automatic Maintenance automatically stops currently running maintenance activities if the user starts interacting with the computer.</span></span> <span data-ttu-id="f2abe-141">Wartungsaktivitäten werden fortgesetzt, wenn das System in den Leerlauf Status zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="f2abe-141">Maintenance activity will resume when the system returns to idle status.</span></span>

> [!Note]  
> <span data-ttu-id="f2abe-142">Alle Aktivitäten bei der automatischen Wartung müssen das Beenden in zwei Sekunden oder weniger unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f2abe-142">All activities in Automatic Maintenance must support stopping in 2 seconds or less.</span></span> <span data-ttu-id="f2abe-143">Der Benutzer sollte benachrichtigt werden, dass die Aktivität beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f2abe-143">The user should be notified that the activity has been stopped.</span></span>

 

<span data-ttu-id="f2abe-144">**Termine und Benachrichtigungen**</span><span class="sxs-lookup"><span data-stu-id="f2abe-144">**Deadlines and notification**</span></span>

<span data-ttu-id="f2abe-145">Eine kritische Wartungs Aktivität muss innerhalb eines vordefinierten Zeitfensters ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f2abe-145">Critical maintenance activity must execute within a pre-defined time window.</span></span> <span data-ttu-id="f2abe-146">Wenn wichtige Tasks nicht innerhalb der vorgesehenen Zeit ausgeführt werden konnten, wird die automatische Wartung automatisch mit der nächsten verfügbaren System Leerlauf Chance gestartet.</span><span class="sxs-lookup"><span data-stu-id="f2abe-146">If critical tasks have not been able to run within their designated time, Automatic Maintenance will automatically start executing at the next available system idle opportunity.</span></span> <span data-ttu-id="f2abe-147">Wenn sich der Task Status jedoch hinter dem Stichtag befindet, benachrichtigt die automatische Wartung den Benutzer über die Aktivität und stellt eine Option für die manuelle Durchführung der automatischen Wartung bereit.</span><span class="sxs-lookup"><span data-stu-id="f2abe-147">However, if the task state remains behind deadline, Automatic Maintenance will notify the user about the activity and provide an option for a manual run of Automatic Maintenance.</span></span> <span data-ttu-id="f2abe-148">Alle Tasks, die für die Wartung geplant sind, werden ausgeführt, obwohl die am meisten gestarteten Tasks Vorrang haben.</span><span class="sxs-lookup"><span data-stu-id="f2abe-148">All tasks scheduled for maintenance will run, although the most starved tasks take precedence.</span></span> <span data-ttu-id="f2abe-149">Diese Aktivität kann sich auf die Reaktionsfähigkeit und Leistung des Systems auswirken. Daher wird der Benutzer durch die automatische Wartung benachrichtigt, dass eine kritische Wartungs Aktivität ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2abe-149">This activity may impact system responsiveness and performance; therefore, Automatic Maintenance will notify the user that critical maintenance activity is executing.</span></span>

<span data-ttu-id="f2abe-150">**Unternehmenssteuerung**</span><span class="sxs-lookup"><span data-stu-id="f2abe-150">**Enterprise control**</span></span>

<span data-ttu-id="f2abe-151">IT-Experten in Unternehmen sollten ermitteln können, wann die automatische Wartung auf Ihren Windows-Systemen ausgeführt wird, diesen Zeitplan über standardisierte Verwaltungs Schnittstellen erzwingen und Ereignisdaten zum Status der automatischen Wartungs Ausführung abrufen.</span><span class="sxs-lookup"><span data-stu-id="f2abe-151">Enterprise IT professionals should be able to determine when Automatic Maintenance executes on their Windows systems, enforce that schedule via standardized management interfaces, and retrieve event data about the status of Automatic Maintenance execution attempts.</span></span> <span data-ttu-id="f2abe-152">Außerdem sollten IT-Experten in der Lage sein, bestimmte automatische Wartungsaktivitäten Remote über Standard Verwaltungs Schnittstellen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f2abe-152">Additionally, IT professionals should be able to invoke specific Automatic Maintenance activity remotely via standard management interfaces.</span></span> <span data-ttu-id="f2abe-153">Jedes Mal, wenn die automatische Wartung ausgeführt wird, wird die Status Berichterstattung, einschließlich Benachrichtigungen, wenn die automatische Wartung nicht ausgeführt werden konnte, da der Benutzer die Aktivität manuell angehalten hat, ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2abe-153">Each time Automatic Maintenance executes, status reporting, including notifications when Automatic Maintenance could not be executed because the user has manually paused the activity, runs.</span></span> <span data-ttu-id="f2abe-154">IT-Experten sollten erwägen, Anmelde Skripts in die automatische Wartung zu verschieben, um die Anmeldung des Benutzers zu beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="f2abe-154">IT professionals should consider moving logon scripts to Automatic Maintenance to help make the user’s logon experience quicker.</span></span>

## <a name="creating-an-automatic-maintenance-task"></a><span data-ttu-id="f2abe-155">Erstellen eines automatischen Wartungs Tasks</span><span class="sxs-lookup"><span data-stu-id="f2abe-155">Creating an Automatic Maintenance task</span></span>

<span data-ttu-id="f2abe-156">In diesem Abschnitt wird erläutert, wie Entwickler eine Aufgabe mit einer Aufgabendefinition in XML-oder C-Sprache erstellen können.</span><span class="sxs-lookup"><span data-stu-id="f2abe-156">This section details how developers can create a task using a task definition in XML or C language.</span></span> <span data-ttu-id="f2abe-157">Beachten Sie, dass die Wartungs Aktivität keine Benutzeroberfläche starten sollte, die eine Benutzerinteraktion erfordert, da die automatische Wartung vollständig abläuft und ausgeführt wird, wenn der Benutzer nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f2abe-157">Keep in mind that maintenance activity should not launch any user interface that requires user interaction, as Automatic Maintenance is completely silent and runs when the user is not present.</span></span> <span data-ttu-id="f2abe-158">Wenn der Benutzer während der automatischen Wartung mit dem Computer interagiert, werden alle Aufgaben, die in Bearbeitung sind, bis zum nächsten Leerlauf Zeitraum beendet.</span><span class="sxs-lookup"><span data-stu-id="f2abe-158">Indeed, if the user interacts with the computer during Automatic Maintenance, any tasks in process will be ended until the next idle period.</span></span>

<span data-ttu-id="f2abe-159">**Verwenden von XML**</span><span class="sxs-lookup"><span data-stu-id="f2abe-159">**Using XML**</span></span>

<span data-ttu-id="f2abe-160">Taskplaner enthält ein integriertes Befehlszeilen Tool schtasks.exe, mit dem eine Aufgabendefinition im XML-Format importiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f2abe-160">Task Scheduler includes a built-in command-line tool, schtasks.exe, that can import a task definition in XML format.</span></span> <span data-ttu-id="f2abe-161">Das Schema für die Aufgabendefinition ist unter dokumentiert https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx .</span><span class="sxs-lookup"><span data-stu-id="f2abe-161">The schema for task definition is documented at https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx.</span></span> <span data-ttu-id="f2abe-162">Im folgenden finden Sie ein Beispiel für einen automatischen Wartungs Task, der in XML definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f2abe-162">Below is an example of an Automatic Maintenance task defined in XML.</span></span>


```
<?xml version="1.0" encoding="UTF-16"?>
<Task version="1.4" xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
  <RegistrationInfo>
    <Date>2011-07-01T11:34:31</Date>
    <Author>IT Deptartment</Author>
  </RegistrationInfo>
  <Principals>
    <Principal id="Author">
      <RunLevel>LeastPrivilege</RunLevel>
      <GroupId>NT AUTHORITY\SYSTEM</GroupId>
    </Principal>
  </Principals>
  <Settings>
    <MultipleInstancesPolicy>IgnoreNew</MultipleInstancesPolicy>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
    <AllowHardTerminate>true</AllowHardTerminate>
    <StartWhenAvailable>false</StartWhenAvailable>
    <RunOnlyIfNetworkAvailable>false</RunOnlyIfNetworkAvailable>
    <MaintenanceSettings>
      <Period>P2D</Period>
      <Deadline>P14D</Deadline>
    </MaintenanceSettings>
    <AllowStartOnDemand>true</AllowStartOnDemand>
    <Enabled>true</Enabled>
    <Hidden>false</Hidden>
    <RunOnlyIfIdle>false</RunOnlyIfIdle>
    <DisallowStartOnRemoteAppSession>false</DisallowStartOnRemoteAppSession>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
    <WakeToRun>false</WakeToRun>
    <ExecutionTimeLimit>P3D</ExecutionTimeLimit>
    <Priority>7</Priority>
  </Settings>
  <Actions Context="Author">
    <Exec>
      <Command>cmd</Command>
      <Arguments>/c timeout -t 60</Arguments>
    </Exec>
  </Actions>
</Task> 
```



<span data-ttu-id="f2abe-163">Speichern Sie den obigen XML-Code als Textdatei, und verwenden Sie die folgende Befehlszeile, um die Aufgabe auf einem Windows-Computer zu speichern:</span><span class="sxs-lookup"><span data-stu-id="f2abe-163">To save the task on a Windows computer, save the above XML as a text file and use this command line:</span></span>

`Schtasks.exe /create /tn <task name> /xml <text file name>`

<span data-ttu-id="f2abe-164">**Verwenden von C**</span><span class="sxs-lookup"><span data-stu-id="f2abe-164">**Using C**</span></span>

<span data-ttu-id="f2abe-165">Eine automatische Wartungs Aufgabe kann auch mithilfe von C-Code erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f2abe-165">An Automatic Maintenance task also can be created using C code.</span></span> <span data-ttu-id="f2abe-166">Im folgenden finden Sie ein Codebeispiel, das zum Konfigurieren der automatischen Wartungs Einstellungen eines Tasks verwendet werden kann:</span><span class="sxs-lookup"><span data-stu-id="f2abe-166">Below is a code sample that can be used to configure a task’s Automatic Maintenance settings:</span></span>


```
/********************************************************************
This sample creates a maintenance task to start cmd window during maintenance opportunities with periodicity of 2 days and deadline 0f 14 days.
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
#include <wincred.h>
//  Include the task header file.
#include <taskschd.h>
//#pragma comment(lib, "taskschd.lib")
//#pragma comment(lib, "comsupp.lib")

int __cdecl 
MainteanceTask( )
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr;

    //  ------------------------------------------------------
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"MaintenanceTask";

    ITaskService *pService = NULL;
    ITaskFolder *pRootFolder = NULL;
    ITaskDefinition *pTask = NULL;
    ITaskSettings *pSettings = NULL;
    IRegistrationInfo *pRegInfo= NULL;
    IPrincipal *pPrincipal = NULL;
    ITaskSettings3 *pSettings3 = NULL;
    IMaintenanceSettings* pMaintenanceSettings = NULL;
    IActionCollection *pActionCollection = NULL;
    IAction *pAction = NULL;
    IExecAction *pExecAction = NULL;
    IRegisteredTask *pRegisteredTask = NULL;

    wprintf(L"\nCreate Maintenance Task %ws", wszTaskName );

    hr = CoInitializeEx( NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        wprintf(L"\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity( NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL,
        0,
        NULL);

    if( FAILED(hr) )
    {
        wprintf(L"\nCoInitializeSecurity failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to create an instance of ITaskService: %x", hr);
        goto CleanUp;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(), _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        wprintf(L"\nITaskService::Connect failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.  This folder will hold the
    //  new task that is registered.
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Root folder pointer: %x", hr );
        goto CleanUp;
    }
    
    //  If the same task exists, remove it.
    ( void ) pRootFolder->DeleteTask( _bstr_t(wszTaskName), 0  );
    
    //  Create the task definition object to create the task.
    hr = pService->NewTask( 0, &pTask );
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to CoCreate an instance of the TaskService class: %x", hr);
        goto CleanUp;
    }
        
    //  ------------------------------------------------------
    //  Get the registration info for setting the identification.
    hr = pTask->get_RegistrationInfo( &pRegInfo );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get identification pointer: %x", hr );
        goto CleanUp;
    }
    
    hr = pRegInfo->put_Author( _bstr_t(L"Author Name") );    
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put identification info: %x", hr );
        goto CleanUp;
    }

    // The task needs to grant explicit FRFX to LOCAL SERVICE (A;;FRFX;;;LS)
    hr = pRegInfo->put_SecurityDescriptor( _variant_t(L"D:P(A;;FA;;;BA)(A;;FA;;;SY)(A;;FRFX;;;LS)") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put security descriptor: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create the principal for the task - these credentials
    //  are overwritten with the credentials passed to RegisterTaskDefinition
    hr = pTask->get_Principal( &pPrincipal );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get principal pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Set up principal logon type to interactive logon
    hr = pPrincipal->put_LogonType( TASK_LOGON_INTERACTIVE_TOKEN );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put principal info: %x", hr );
        goto CleanUp;
    }  

    //  ------------------------------------------------------
    //  Create the settings for the task
    hr = pTask->get_Settings( &pSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get settings pointer: %x", hr );
        goto CleanUp;
    }

    hr = pSettings->QueryInterface( __uuidof(ITaskSettings3), (void**) &pSettings3 );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot query ITaskSettings3 interface: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->put_UseUnifiedSchedulingEngine( VARIANT_TRUE );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_UseUnifiedSchedulingEngine: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->CreateMaintenanceSettings( &pMaintenanceSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot CreateMaintenanceSettings: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Period ( _bstr_t(L"P2D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Deadline ( _bstr_t(L"P14D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Add an action to the task. This task will execute notepad.exe.     
    //  Get the task action collection pointer.
    hr = pTask->get_Actions( &pActionCollection );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Task collection pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Create the action, specifying that it is an executable action.
    hr = pActionCollection->Create( TASK_ACTION_EXEC, &pAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot create the action: %x", hr );
        goto CleanUp;
    }

    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( IID_IExecAction, (void**) &pExecAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nQueryInterface call failed for IExecAction: %x", hr );
        goto CleanUp;
    }

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t(L"cmd") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put action path: %x", hr );
        goto CleanUp;
    }  
    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t(wszTaskName),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(), 
            _variant_t(), 
            TASK_LOGON_INTERACTIVE_TOKEN,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        wprintf(L"\nError saving the Task : %x", hr );
        goto CleanUp;
    }
    
    wprintf(L"\nSuccess!\n----------------------------------" );

CleanUp:

    if ( pService != NULL ) pService->Release();
    if ( pRootFolder != NULL ) pRootFolder->Release();
    if ( pTask != NULL ) pTask->Release();
    if ( pSettings != NULL ) pSettings->Release();
    if ( pRegInfo != NULL ) pRegInfo->Release();
    if ( pPrincipal != NULL ) pPrincipal->Release();
    if ( pSettings3 != NULL ) pSettings3->Release();
    if ( pMaintenanceSettings != NULL ) pMaintenanceSettings->Release();
    if ( pActionCollection != NULL ) pActionCollection->Release();
    if ( pAction != NULL ) pAction->Release();
    if ( pExecAction != NULL ) pExecAction->Release();
    if ( pRegisteredTask != NULL ) pRegisteredTask->Release();

    CoUninitialize();
    return SUCCEEDED ( hr ) ? 0 : 1;
}
```



## <a name="validating-tasks"></a><span data-ttu-id="f2abe-167">Validieren von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="f2abe-167">Validating tasks</span></span>

<span data-ttu-id="f2abe-168">Überprüfen Sie, ob die Aufgabe erfolgreich erstellt wurde und im Rahmen der Wartung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2abe-168">Validate that the task has been created successfully and runs as part of maintenance.</span></span>

<span data-ttu-id="f2abe-169">**Die Task Erstellung wird überprüft.**</span><span class="sxs-lookup"><span data-stu-id="f2abe-169">**Validating task creation**</span></span>

<span data-ttu-id="f2abe-170">Verwenden Sie diese Befehlszeile, um die Aufgabendefinition in eine Datei zu exportieren und sicherzustellen, dass die Aufgabendefinition erwartungsgemäß lautet:</span><span class="sxs-lookup"><span data-stu-id="f2abe-170">Use this command line to export the task definition to a file and ensure that the task definition is as expected:</span></span>

`Schtasks.exe /Query /tn<task name> /xml <text file name>`

<span data-ttu-id="f2abe-171">**Validieren der Task Ausführung**</span><span class="sxs-lookup"><span data-stu-id="f2abe-171">**Validating task execution**</span></span>

<span data-ttu-id="f2abe-172">Führen Sie diese Befehlszeile aus, um die Aufgabe zu starten und zu überprüfen, ob die Taskplaner Benutzeroberfläche (taskschd. msc) anzeigt, dass die Aufgabe ausgeführt wurde</span><span class="sxs-lookup"><span data-stu-id="f2abe-172">Run this command line to launch the task and validate that the Task Scheduler UI (taskschd.msc) shows the task has run:</span></span>

`Schtasks.exe /Run /tn<task name>`

## <a name="resources"></a><span data-ttu-id="f2abe-173">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f2abe-173">Resources</span></span>

-   <span data-ttu-id="f2abe-174">[Aufgaben Zeitplan 2,0](/previous-versions/bb756979(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="f2abe-174">[Task Schedule 2.0](/previous-versions/bb756979(v=msdn.10))</span></span>

 

 