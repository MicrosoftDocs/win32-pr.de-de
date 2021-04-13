---
title: Kontingent Verwaltung für Remote Shells
description: Die Kontingent Verwaltung ermöglicht es Benutzern, Systemressourcen effizienter zu verwalten.
ms.assetid: 6651a500-a95a-45a1-b46a-27b2e9b36a1c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1310efd37b913ae0bf8394015f6df792711ac6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310920"
---
# <a name="quota-management-for-remote-shells"></a><span data-ttu-id="aa972-103">Kontingent Verwaltung für Remote Shells</span><span class="sxs-lookup"><span data-stu-id="aa972-103">Quota Management for Remote Shells</span></span>

<span data-ttu-id="aa972-104">Die Kontingent Verwaltung ermöglicht es Benutzern, Systemressourcen effizienter zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="aa972-104">Quota management allows users to manage system resources more efficiently.</span></span> <span data-ttu-id="aa972-105">Windows-Remoteverwaltung (WinRM) hat einen bestimmten Satz von Kontingenten hinzugefügt, die eine bessere Dienst Qualität bieten, Denial-of-Service-Probleme verhindern und gleichzeitigen Benutzern Server Ressourcen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="aa972-105">Windows Remote Management (WinRM) has added a specific set of quotas that provide a better quality of service, help prevent denial of service issues, and allocate server resources to concurrent users.</span></span> <span data-ttu-id="aa972-106">Das festgelegte WinRM-Kontingent basiert auf der Kontingent Infrastruktur, die für den Internetinformationsdienste (IIS)-Dienst implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="aa972-106">The WinRM quota set is based on the quota infrastructure that is implemented for the Internet Information Services (IIS) service.</span></span>

<span data-ttu-id="aa972-107">Durch das Implementieren von Kontingenten werden Leistungseinbußen und Denial-of-Service-Probleme durch folgende Aktionen verhindert:</span><span class="sxs-lookup"><span data-stu-id="aa972-107">Implementing quotas will help to prevent performance degradation and denial of service issues by doing the following:</span></span>

-   <span data-ttu-id="aa972-108">Begrenzen der Anzahl von Shells und shellprozessen, die ein Benutzer erstellen kann</span><span class="sxs-lookup"><span data-stu-id="aa972-108">Limiting the number of shells and shell processes that a user can create</span></span>
-   <span data-ttu-id="aa972-109">Einschränken der maximalen Anzahl gleichzeitiger Benutzer</span><span class="sxs-lookup"><span data-stu-id="aa972-109">Limiting the maximum number of concurrent users</span></span>
-   <span data-ttu-id="aa972-110">Verwalten der Menge an Arbeitsspeicher, die einer Shell zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="aa972-110">Managing the amount of memory that is allocated to a shell</span></span>
-   <span data-ttu-id="aa972-111">Festlegen eines Timeouts für inaktive Shells</span><span class="sxs-lookup"><span data-stu-id="aa972-111">Setting a time-out for shells that are inactive</span></span>

## <a name="quota-settings"></a><span data-ttu-id="aa972-112">Kontingent Einstellungen</span><span class="sxs-lookup"><span data-stu-id="aa972-112">Quota Settings</span></span>

<span data-ttu-id="aa972-113">Die folgenden Kontingente müssen für die remoteshellverwaltung erzwungen werden.</span><span class="sxs-lookup"><span data-stu-id="aa972-113">The following quotas need to be enforced for remote shell management.</span></span> <span data-ttu-id="aa972-114">Diese Kontingente können über das WinRM-Hilfsprogramm oder über Gruppenrichtlinie Einstellungen konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="aa972-114">These quotas can be configured through the winrm utility or through Group Policy settings.</span></span> <span data-ttu-id="aa972-115">Von einem Gruppenrichtlinie konfigurierte Einstellungen ersetzen die durch das WinRM-Hilfsprogramm festgelegten Kontingente.</span><span class="sxs-lookup"><span data-stu-id="aa972-115">Settings configured by a Group Policy supersede the quotas set by the winrm utility.</span></span> <span data-ttu-id="aa972-116">Weitere Informationen zum Festlegen von Gruppenrichtlinien für WinRM finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="aa972-116">For more information about setting Group Policies for WinRM, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<dl> <dt>

<span data-ttu-id="aa972-117"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="aa972-117"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span></span>
</dt> <dd>

<span data-ttu-id="aa972-118">Die maximale Zeit in Millisekunden, bevor eine inaktive Remoteshell gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="aa972-118">The maximum time in milliseconds before an inactive remote shell is deleted.</span></span> <span data-ttu-id="aa972-119">Der Standardwert ist 180000 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="aa972-119">The default is 180000 milliseconds.</span></span> <span data-ttu-id="aa972-120">Die minimale Zeit beträgt 1000 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="aa972-120">The minimum time is 1000 milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="aa972-121"><span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>Maxprocessespershell</span><span class="sxs-lookup"><span data-stu-id="aa972-121"><span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell</span></span>
</dt> <dd>

<span data-ttu-id="aa972-122">Die maximal zulässige Anzahl von Prozessen Pro Shell, einschließlich der untergeordneten Prozesse der Shell.</span><span class="sxs-lookup"><span data-stu-id="aa972-122">The maximum number of processes allowed per shell, including the shell's child processes.</span></span> <span data-ttu-id="aa972-123">Der Standard ist 25.</span><span class="sxs-lookup"><span data-stu-id="aa972-123">The default is 25.</span></span>

</dd> <dt>

<span data-ttu-id="aa972-124"><span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>Maxmemorypershellmb</span><span class="sxs-lookup"><span data-stu-id="aa972-124"><span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB</span></span>
</dt> <dd>

<span data-ttu-id="aa972-125">Die maximale Menge an Arbeitsspeicher, die Pro Shell zugeordnet ist, einschließlich der untergeordneten Prozesse der Shell.</span><span class="sxs-lookup"><span data-stu-id="aa972-125">The maximum amount of memory allocated per shell, including the shell's child processes.</span></span> <span data-ttu-id="aa972-126">Der Standardwert ist 1024 MB.</span><span class="sxs-lookup"><span data-stu-id="aa972-126">The default is 1024 MB.</span></span>

> [!Note]  
> <span data-ttu-id="aa972-127">Das Verhalten wird nicht unterstützt, wenn maxmemorypershellmb auf einen Wert festgelegt ist, der kleiner als der Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="aa972-127">The behavior is unsupported if the MaxMemoryPerShellMB is set to a value that is less than the default.</span></span>

 

</dd> <dt>

<span data-ttu-id="aa972-128"><span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser</span><span class="sxs-lookup"><span data-stu-id="aa972-128"><span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser</span></span>
</dt> <dd>

<span data-ttu-id="aa972-129">Die maximale Anzahl von Shells pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="aa972-129">The maximum number of shells per user.</span></span> <span data-ttu-id="aa972-130">Der Standardwert ist 30.</span><span class="sxs-lookup"><span data-stu-id="aa972-130">The default is 30.</span></span>

</dd> <dt>

<span data-ttu-id="aa972-131"><span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers</span><span class="sxs-lookup"><span data-stu-id="aa972-131"><span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers</span></span>
</dt> <dd>

<span data-ttu-id="aa972-132">Die maximale Anzahl gleichzeitiger Benutzer, die Shells öffnen können.</span><span class="sxs-lookup"><span data-stu-id="aa972-132">The maximum number of concurrent users who can open shells.</span></span> <span data-ttu-id="aa972-133">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="aa972-133">The default is 10.</span></span>

</dd> </dl>

## <a name="deprecated-quotas"></a><span data-ttu-id="aa972-134">Veraltete Kontingente</span><span class="sxs-lookup"><span data-stu-id="aa972-134">Deprecated Quotas</span></span>

<span data-ttu-id="aa972-135">WinRM 2,0 legt das maxshellruntime-Kontingent auf schreibgeschützt fest.</span><span class="sxs-lookup"><span data-stu-id="aa972-135">WinRM 2.0 sets the MaxShellRunTime quota to read-only.</span></span> <span data-ttu-id="aa972-136">Das Ändern des Werts für dieses Kontingent hat keine Auswirkung auf die Remote Shells.</span><span class="sxs-lookup"><span data-stu-id="aa972-136">Changing the value for this quota will have no effect on the remote shells.</span></span>

## <a name="retrieving-quota-configuration-information"></a><span data-ttu-id="aa972-137">Informationen zur Kontingent Konfiguration werden abgerufen.</span><span class="sxs-lookup"><span data-stu-id="aa972-137">Retrieving Quota Configuration Information</span></span>

<span data-ttu-id="aa972-138">Um die Einstellungen für die Kontingent Konfiguration zu überprüfen, geben Sie **WinRM Get WinRM/config** ein.</span><span class="sxs-lookup"><span data-stu-id="aa972-138">To check the quota configuration settings, type **winrm get winrm/config**.</span></span>

<span data-ttu-id="aa972-139">Der folgende Code Ausschnitt ist ein textbasiertes Beispiel für eine WinRM-Konfiguration mit den standardmäßigen Kontingent Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="aa972-139">The following snippet is a text-based example of a WinRM configuration with the default quota settings.</span></span>

``` syntax
Config

          ...         

          Winrs

                   AllowRemoteShellAccess = true

                   IdleTimeout = 7200000

                   MaxConcurrentUsers = 10

                   MaxProcessesPerShell = 25

                   MaxMemoryPerShellMB = 1024

                   MaxShellsPerUser = 30
```

## <a name="configuring-shell-quotas"></a><span data-ttu-id="aa972-140">Konfigurieren von shellkontingente</span><span class="sxs-lookup"><span data-stu-id="aa972-140">Configuring Shell Quotas</span></span>

<span data-ttu-id="aa972-141">Kontingente können über eine Gruppenrichtlinie Einstellung oder manuell festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="aa972-141">Quotas can be set through a Group Policy setting or manually.</span></span> <span data-ttu-id="aa972-142">Weitere Informationen zu bestimmten Konfigurationseinstellungen finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="aa972-142">For more information about specific configuration settings, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<span data-ttu-id="aa972-143">**So legen Sie ein Kontingent mit Gruppenrichtlinie fest**</span><span class="sxs-lookup"><span data-stu-id="aa972-143">**To set a quota with Group Policy**</span></span>

1.  <span data-ttu-id="aa972-144">Öffnen Sie ein Eingabeaufforderungsfenster als ein Administrator.</span><span class="sxs-lookup"><span data-stu-id="aa972-144">Open a Command Prompt window as an administrator.</span></span>
2.  <span data-ttu-id="aa972-145">Geben Sie an der Eingabeaufforderung **gpeer dit. msc** ein.</span><span class="sxs-lookup"><span data-stu-id="aa972-145">At the Command Prompt, type **gpedit.msc**.</span></span> <span data-ttu-id="aa972-146">Das **Gruppenrichtlinienobjekt-Editor** Fenster wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="aa972-146">The **Group Policy Object Editor** window opens.</span></span>
3.  <span data-ttu-id="aa972-147">Suchen Sie die **Windows-Remoteverwaltung** und **Windows remotesshell** Gruppenrichtlinie Objects (GPO) unter **Computer Konfiguration \\ Administrative Vorlagen \\ Windows-Komponenten**.</span><span class="sxs-lookup"><span data-stu-id="aa972-147">Find the **Windows Remote Management** and **Windows Remote Shell** Group Policy Objects (GPO) under **Computer Configuration\\Administrative Templates\\Windows Components**.</span></span>
4.  <span data-ttu-id="aa972-148">Wählen Sie auf der Registerkarte **erweitert** eine Einstellung aus, um eine Beschreibung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aa972-148">On the **Extended** tab, select a setting to see a description.</span></span> <span data-ttu-id="aa972-149">Doppelklicken Sie auf eine Einstellung, um Sie zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="aa972-149">Double click a setting to edit it.</span></span>

<span data-ttu-id="aa972-150">**So legen Sie ein Kontingent manuell fest**</span><span class="sxs-lookup"><span data-stu-id="aa972-150">**To set a quota manually**</span></span>

1.  <span data-ttu-id="aa972-151">Öffnen Sie ein Eingabeaufforderungsfenster als ein Administrator.</span><span class="sxs-lookup"><span data-stu-id="aa972-151">Open a Command Prompt window as an administrator.</span></span>
2.  <span data-ttu-id="aa972-152">Geben Sie an der Eingabeaufforderung **WinRM Set WinRM/config/Winrs ' @ { ***<Quota>*** = " ***<Value>*** "} "** ein.</span><span class="sxs-lookup"><span data-stu-id="aa972-152">At the Command Prompt, type **winrm set winrm/config/winrs '@{***<Quota>***="***<Value>***"}'**</span></span>

<span data-ttu-id="aa972-153">Wenn Sie z. b. die maximale Anzahl von Shells pro Benutzer von 5 auf 7 erhöhen möchten, geben Sie **WinRM Set WinRM/config/Winrs ' @ {maxshellsperuser = "7"}**"ein.</span><span class="sxs-lookup"><span data-stu-id="aa972-153">For example, to increase the maximum number of shells per user from 5 to 7, type **winrm set winrm/config/winrs '@{MaxShellsPerUser="7"}'**.</span></span>

 

 




