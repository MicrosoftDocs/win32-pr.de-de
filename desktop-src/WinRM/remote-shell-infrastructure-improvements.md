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
# <a name="remote-shell-infrastructure-improvements"></a>Verbesserungen der Remoteshell

Windows-Remoteverwaltung Version 2,0 (WinRM 2,0) bietet viele Verbesserungen der remoteshellinfrastruktur. In den folgenden Themen werden diese Verbesserungen detailliert beschrieben:

-   [Unterstützung für mehrere Hops](multi-hop-support.md)
-   [Kontingent Verwaltung für Remote Shells](quotas.md)

Zu den Verbesserungen der WinRM-remoteshellinfrastruktur gehört das Hinzufügen eines robusteren shellmanagers, der benutzerspezifische Shellinformationen verwaltet. WinRM-Benutzer können Shells auf Remote Computern erstellen, um Befehle oder Skripts auszuführen. Außerdem können Benutzer mehrere Shells auf einem Computer erstellen. Benutzer und Administratoren benötigen beide die Möglichkeit, Shells zu verwalten. Benutzer können die von Ihnen erstellten Shells aufzählen, löschen und löschen. Administratoren können alle aktiven Shells aufzählen und Details zu bestimmten Shells auf einem lokalen oder Remote Host abrufen. Administratoren können auch alle aktiven Shells auf einem lokalen oder Remote Host löschen.

Wenn ein Benutzer oder Administrator die aktiven Shells aufzählt, können vom WinRM-Dienst die folgenden Informationen zurückgegeben werden.

<dl> <dt>

<span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>Shellid
</dt> <dd>

Gibt den eindeutigen Bezeichner für die Shell an.

</dd> <dt>

<span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Umgebungsvariablen
</dt> <dd>

Gibt alle vom Benutzer festgelegten Umgebungsvariablen an.

</dd> <dt>

<span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory
</dt> <dd>

Gibt das Start Verzeichnis für die Shell an.

</dd> <dt>

<span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI
</dt> <dd>

Gibt den Ressourcen-URI für den shellvorgang an. Der Ressourcen-URI kann verwendet werden, um die für die Shellinstanz spezifische Plug-in-Konfiguration abzurufen.

</dd> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout
</dt> <dd>

Gibt die maximale Dauer (in Millisekunden) an, die die Shell ohne Anforderung geöffnet bleibt.

</dd> <dt>

<span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>Inputstreams
</dt> <dd>

Gibt die Eingabedaten Ströme für die Shell an.

</dd> <dt>

<span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>Outputstreams
</dt> <dd>

Gibt die Ausgabestreams für die Shell an.

</dd> <dt>

<span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Shellerstellungs Zeit
</dt> <dd>

Gibt den Erstellungszeit Stempel für die Shell an.

</dd> <dt>

<span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime
</dt> <dd>

Gibt die Dauer (in Millisekunden) an, in der sich die Shell im Leerlauf befindet.

</dd> <dt>

<span id="UserId"></span><span id="userid"></span><span id="USERID"></span>UserID
</dt> <dd>

Gibt die Benutzer-ID an.

</dd> <dt>

<span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Hostname oder IP-Adresse
</dt> <dd>

Gibt entweder den Hostnamen oder die IP-Adresse des Computers an, von dem die Shell erstellt wurde.

</dd> <dt>

<span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Shell-Speicherauslastung
</dt> <dd>

Gibt den Umfang des Arbeitsspeichers an, der von der Shell verwendet wurde.

</dd> <dt>

<span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Anzahl der Prozesse
</dt> <dd>

Gibt die Anzahl der Prozesse an, die von der Shell erstellt wurden.

</dd> </dl>

## <a name="enumerating-a-shell-on-a-local-host"></a>Auflisten einer Shell auf einem lokalen Host

Der folgende Befehl veranschaulicht, wie das WinRM-Hilfsprogramm verwendet wird, um Shells auf einem WinRM-Client aufzulisten: **WinRM-enumerationsshell**.

Im folgenden textbasierten Beispiel wird die Ausgabe für die shellenumeration angezeigt:

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

Weitere Informationen finden Sie in der bereitgestellten Online Hilfe, indem Sie den folgenden Befehl ausführen: **WinRM auflisten-?**.

## <a name="retrieving-information-about-a-specific-shell"></a>Abrufen von Informationen zu einer bestimmten Shell

Ein Administrator oder Benutzer kann auch den shellid-Bezeichner verwenden, um Informationen zur Shell abzurufen. Der folgende Befehl veranschaulicht die Verwendung des Hilfsprogramms WinRM zum erhalten von Informationen zu einer bestimmten Shell: **WinRM Get Shell? Shellid = 0a6e6a01-8ab2-4037-86cc-bfc826a1244e**.

Im folgenden textbasierten Beispiel wird die Ausgabe für Shellinformationen angezeigt:

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

Weitere Informationen finden Sie in der Online Hilfe, die mit dem folgenden Befehl bereitgestellt wird: **WinRM Get-?**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützung für mehrere Hops](multi-hop-support.md)
</dt> <dt>

[Kontingent Verwaltung für Remote Shells](quotas.md)
</dt> <dt>

[Verwaltete Referenz für WS-Management PowerShell-Befehle](winrm-powershell-commandlets.md)
</dt> </dl>

 

 




