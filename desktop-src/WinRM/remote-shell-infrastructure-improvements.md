---
title: Verbesserungen der Remoteshell
description: Windows-Remoteverwaltung Version 2,0 (WinRM 2,0) bietet viele Verbesserungen der remoteshellinfrastruktur.
ms.assetid: b22693ba-fa43-44bb-9b2d-0c64fad6e3cc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c67752222f1ca969ea254164a25144168d1eb3
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/24/2020
ms.locfileid: "104038473"
---
# <a name="remote-shell-infrastructure-improvements"></a><span data-ttu-id="e783f-103">Verbesserungen der Remoteshell</span><span class="sxs-lookup"><span data-stu-id="e783f-103">Remote Shell Infrastructure Improvements</span></span>

<span data-ttu-id="e783f-104">Windows-Remoteverwaltung Version 2,0 (WinRM 2,0) bietet viele Verbesserungen der remoteshellinfrastruktur.</span><span class="sxs-lookup"><span data-stu-id="e783f-104">Windows Remote Management version 2.0 (WinRM 2.0) offers many remote shell infrastructure improvements.</span></span> <span data-ttu-id="e783f-105">In den folgenden Themen werden diese Verbesserungen detailliert beschrieben:</span><span class="sxs-lookup"><span data-stu-id="e783f-105">The following topics describe these improvements in detail:</span></span>

-   [<span data-ttu-id="e783f-106">Unterstützung für mehrere Hops</span><span class="sxs-lookup"><span data-stu-id="e783f-106">Multi-Hop Support</span></span>](multi-hop-support.md)
-   [<span data-ttu-id="e783f-107">Kontingent Verwaltung für Remote Shells</span><span class="sxs-lookup"><span data-stu-id="e783f-107">Quota Management for Remote Shells</span></span>](quotas.md)

<span data-ttu-id="e783f-108">Zu den Verbesserungen der WinRM-remoteshellinfrastruktur gehört das Hinzufügen eines robusteren shellmanagers, der benutzerspezifische Shellinformationen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e783f-108">One of the improvements to the WinRM remote shell infrastructure is the addition of a more robust shell manager that maintains user-specific shell information.</span></span> <span data-ttu-id="e783f-109">WinRM-Benutzer können Shells auf Remote Computern erstellen, um Befehle oder Skripts auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e783f-109">WinRM users can create shells on remote computers to run commands or scripts.</span></span> <span data-ttu-id="e783f-110">Außerdem können Benutzer mehrere Shells auf einem Computer erstellen.</span><span class="sxs-lookup"><span data-stu-id="e783f-110">In addition, users can create multiple shells on a computer.</span></span> <span data-ttu-id="e783f-111">Benutzer und Administratoren benötigen beide die Möglichkeit, Shells zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="e783f-111">Users and administrators both need the ability to manage shells.</span></span> <span data-ttu-id="e783f-112">Benutzer können die von Ihnen erstellten Shells aufzählen, löschen und löschen.</span><span class="sxs-lookup"><span data-stu-id="e783f-112">Users can enumerate, get, and delete the shells that they have created.</span></span> <span data-ttu-id="e783f-113">Administratoren können alle aktiven Shells aufzählen und Details zu bestimmten Shells auf einem lokalen oder Remote Host abrufen.</span><span class="sxs-lookup"><span data-stu-id="e783f-113">Administrators can enumerate over all active shells and retrieve details about specific shells on a local or remote host.</span></span> <span data-ttu-id="e783f-114">Administratoren können auch alle aktiven Shells auf einem lokalen oder Remote Host löschen.</span><span class="sxs-lookup"><span data-stu-id="e783f-114">Administrators can also delete any active shells on a local or remote host.</span></span>

<span data-ttu-id="e783f-115">Wenn ein Benutzer oder Administrator die aktiven Shells aufzählt, können vom WinRM-Dienst die folgenden Informationen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e783f-115">When a user or administrator enumerates the active shells, the following information can be returned by the WinRM service.</span></span>

<dl> <dt>

<span data-ttu-id="e783f-116"><span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>Shellid</span><span class="sxs-lookup"><span data-stu-id="e783f-116"><span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId</span></span>
</dt> <dd>

<span data-ttu-id="e783f-117">Gibt den eindeutigen Bezeichner für die Shell an.</span><span class="sxs-lookup"><span data-stu-id="e783f-117">Specifies the unique identifier for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="e783f-118"><span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Umgebungsvariablen</span><span class="sxs-lookup"><span data-stu-id="e783f-118"><span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Environment variables</span></span>
</dt> <dd>

<span data-ttu-id="e783f-119">Gibt alle vom Benutzer festgelegten Umgebungsvariablen an.</span><span class="sxs-lookup"><span data-stu-id="e783f-119">Specifies any environment variables set by the user.</span></span>

</dd> <dt>

<span data-ttu-id="e783f-120"><span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory</span><span class="sxs-lookup"><span data-stu-id="e783f-120"><span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory</span></span>
</dt> <dd>

<span data-ttu-id="e783f-121">Gibt das Start Verzeichnis für die Shell an.</span><span class="sxs-lookup"><span data-stu-id="e783f-121">Specifies the starting directory for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="e783f-122"><span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI</span><span class="sxs-lookup"><span data-stu-id="e783f-122"><span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI</span></span>
</dt> <dd>

<span data-ttu-id="e783f-123">Gibt den Ressourcen-URI für den shellvorgang an.</span><span class="sxs-lookup"><span data-stu-id="e783f-123">Specifies the resource URI for the shell operation.</span></span> <span data-ttu-id="e783f-124">Der Ressourcen-URI kann verwendet werden, um die für die Shellinstanz spezifische Plug-in-Konfiguration abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e783f-124">The resource URI can be used to retrieve plug-in configuration that is specific to the shell instance.</span></span>

</dd> <dt>

<span data-ttu-id="e783f-125"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="e783f-125"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span></span>
</dt> <dd>

<span data-ttu-id="e783f-126">Gibt die maximale Dauer (in Millisekunden) an, die die Shell ohne Anforderung geöffnet bleibt.</span><span class="sxs-lookup"><span data-stu-id="e783f-126">Specifies the maximum duration, in milliseconds, that the shell will stay open without any request.</span></span>

</dd> <dt>

<span data-ttu-id="e783f-127"><span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>Inputstreams</span><span class="sxs-lookup"><span data-stu-id="e783f-127"><span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams</span></span>
</dt> <dd>

<span data-ttu-id="e783f-128">Gibt die Eingabedaten Ströme für die Shell an.</span><span class="sxs-lookup"><span data-stu-id="e783f-128">Specifies the input streams for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="e783f-129"><span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>Outputstreams</span><span class="sxs-lookup"><span data-stu-id="e783f-129"><span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams</span></span>
</dt> <dd>

<span data-ttu-id="e783f-130">Gibt die Ausgabestreams für die Shell an.</span><span class="sxs-lookup"><span data-stu-id="e783f-130">Specifies the output streams for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="e783f-131"><span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Shellerstellungs Zeit</span><span class="sxs-lookup"><span data-stu-id="e783f-131"><span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Shell creation time</span></span>
</dt> <dd>

<span data-ttu-id="e783f-132">Gibt den Erstellungszeit Stempel für die Shell an.</span><span class="sxs-lookup"><span data-stu-id="e783f-132">Specifies the creation timestamp for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="e783f-133"><span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime</span><span class="sxs-lookup"><span data-stu-id="e783f-133"><span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime</span></span>
</dt> <dd>

<span data-ttu-id="e783f-134">Gibt die Dauer (in Millisekunden) an, in der sich die Shell im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="e783f-134">Specifies the duration, in milliseconds, that the shell has been idle.</span></span>

</dd> <dt>

<span data-ttu-id="e783f-135"><span id="UserId"></span><span id="userid"></span><span id="USERID"></span>UserID</span><span class="sxs-lookup"><span data-stu-id="e783f-135"><span id="UserId"></span><span id="userid"></span><span id="USERID"></span>UserId</span></span>
</dt> <dd>

<span data-ttu-id="e783f-136">Gibt die Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="e783f-136">Specifies the user ID.</span></span>

</dd> <dt>

<span data-ttu-id="e783f-137"><span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Hostname oder IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="e783f-137"><span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Hostname or IP address</span></span>
</dt> <dd>

<span data-ttu-id="e783f-138">Gibt entweder den Hostnamen oder die IP-Adresse des Computers an, von dem die Shell erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e783f-138">Specifies either the host name or IP address of the computer that created the shell.</span></span>

</dd> <dt>

<span data-ttu-id="e783f-139"><span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Shell-Speicherauslastung</span><span class="sxs-lookup"><span data-stu-id="e783f-139"><span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Shell memory usage</span></span>
</dt> <dd>

<span data-ttu-id="e783f-140">Gibt den Umfang des Arbeitsspeichers an, der von der Shell verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e783f-140">Specifies the amount of memory that has been used by the shell.</span></span>

</dd> <dt>

<span data-ttu-id="e783f-141"><span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Anzahl der Prozesse</span><span class="sxs-lookup"><span data-stu-id="e783f-141"><span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Number of processes</span></span>
</dt> <dd>

<span data-ttu-id="e783f-142">Gibt die Anzahl der Prozesse an, die von der Shell erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="e783f-142">Specifies the number of processes that have been created by the shell.</span></span>

</dd> </dl>

## <a name="enumerating-a-shell-on-a-local-host"></a><span data-ttu-id="e783f-143">Auflisten einer Shell auf einem lokalen Host</span><span class="sxs-lookup"><span data-stu-id="e783f-143">Enumerating a Shell on a Local Host</span></span>

<span data-ttu-id="e783f-144">Der folgende Befehl veranschaulicht, wie das WinRM-Hilfsprogramm verwendet wird, um Shells auf einem WinRM-Client aufzulisten: **WinRM-enumerationsshell**.</span><span class="sxs-lookup"><span data-stu-id="e783f-144">The following command demonstrates how to use the winrm utility to enumerate shells on a WinRM client: **winrm enumerate shell**.</span></span>

<span data-ttu-id="e783f-145">Im folgenden textbasierten Beispiel wird die Ausgabe für die shellenumeration angezeigt:</span><span class="sxs-lookup"><span data-stu-id="e783f-145">The following text-based example displays the output for shell enumeration:</span></span>

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S

Shell
    ShellId = EE3F11CE-FB3C-4C4E-B113-6F4D643C97D8
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M46S
    ShellInactivity = P0DT0H0M45S
    MemoryUsed = 48MB
    ChildProcesses = 0

Shell
    ShellId = 8FD7F2C4-A434-4D58-A7E8-46F8BF202D0B
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M47S
    ShellInactivity = P0DT0H0M47S
    MemoryUsed = 48MB
    ChildProcesses = 0
```

<span data-ttu-id="e783f-146">Weitere Informationen finden Sie in der bereitgestellten Online Hilfe, indem Sie den folgenden Befehl ausführen: **WinRM auflisten-?**.</span><span class="sxs-lookup"><span data-stu-id="e783f-146">For more information, see the online help provided by running the following command: **winrm enumerate -?**.</span></span>

## <a name="retrieving-information-about-a-specific-shell"></a><span data-ttu-id="e783f-147">Abrufen von Informationen zu einer bestimmten Shell</span><span class="sxs-lookup"><span data-stu-id="e783f-147">Retrieving Information About a Specific Shell</span></span>

<span data-ttu-id="e783f-148">Ein Administrator oder Benutzer kann auch den shellid-Bezeichner verwenden, um Informationen zur Shell abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e783f-148">An administrator or user can also use the ShellId identifier to retrieve information about the shell.</span></span> <span data-ttu-id="e783f-149">Der folgende Befehl veranschaulicht die Verwendung des Hilfsprogramms WinRM zum erhalten von Informationen zu einer bestimmten Shell: **WinRM Get Shell? Shellid = 0a6e6a01-8ab2-4037-86cc-bfc826a1244e**.</span><span class="sxs-lookup"><span data-stu-id="e783f-149">The following command demonstrates how to use the winrm utility to get information about a specific shell: **winrm get shell?ShellId=0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.</span></span>

<span data-ttu-id="e783f-150">Im folgenden textbasierten Beispiel wird die Ausgabe für Shellinformationen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="e783f-150">The following text-based example displays the output for shell information:</span></span>

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S
```

<span data-ttu-id="e783f-151">Weitere Informationen finden Sie in der Online Hilfe, die mit dem folgenden Befehl bereitgestellt wird: **WinRM Get-?**.</span><span class="sxs-lookup"><span data-stu-id="e783f-151">For more information, see the online help provided by the following command: **winrm get -?**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e783f-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e783f-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e783f-153">Unterstützung für mehrere Hops</span><span class="sxs-lookup"><span data-stu-id="e783f-153">Multi-Hop Support</span></span>](multi-hop-support.md)
</dt> <dt>

[<span data-ttu-id="e783f-154">Kontingent Verwaltung für Remote Shells</span><span class="sxs-lookup"><span data-stu-id="e783f-154">Quota Management for Remote Shells</span></span>](quotas.md)
</dt> <dt>

[<span data-ttu-id="e783f-155">Verwaltete Referenz für WS-Management PowerShell-Befehle</span><span class="sxs-lookup"><span data-stu-id="e783f-155">Managed Reference for WS-Management PowerShell Commands</span></span>](winrm-powershell-commandlets.md)
</dt> </dl>

 

 




