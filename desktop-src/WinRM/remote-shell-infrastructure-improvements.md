---
title: Verbesserungen der RemoteShell-Infrastruktur
description: Windows Die Remoteverwaltungsversion 2.0 (WinRM 2.0) bietet viele Verbesserungen der Remoteshellinfrastruktur.
ms.assetid: b22693ba-fa43-44bb-9b2d-0c64fad6e3cc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf88a472319b4b4677992f97509a3603cfe4a32f272388caf9db100b6e7457ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121660"
---
# <a name="remote-shell-infrastructure-improvements"></a>Verbesserungen der RemoteShell-Infrastruktur

Windows Die Remoteverwaltungsversion 2.0 (WinRM 2.0) bietet viele Verbesserungen der Remoteshellinfrastruktur. In den folgenden Themen werden diese Verbesserungen ausführlich beschrieben:

-   [Unterstützung für mehrere Hops](multi-hop-support.md)
-   [Kontingentverwaltung für Remoteshells](quotas.md)

Eine der Verbesserungen an der WinRM-Remoteshellinfrastruktur ist die Ergänzung eines robusteren Shell-Managers, der benutzerspezifische Shellinformationen verwaltet. WinRM-Benutzer können Shells auf Remotecomputern erstellen, um Befehle oder Skripts auszuführen. Darüber hinaus können Benutzer mehrere Shells auf einem Computer erstellen. Sowohl Benutzer als auch Administratoren benötigen die Möglichkeit, Shells zu verwalten. Benutzer können die erstellten Shells aufzählen, erhalten und löschen. Administratoren können alle aktiven Shells aufzählen und Details zu bestimmten Shells auf einem lokalen oder Remotehost abrufen. Administratoren können auch alle aktiven Shells auf einem lokalen oder Remotehost löschen.

Wenn ein Benutzer oder Administrator die aktiven Shells aufzählt, können die folgenden Informationen vom WinRM-Dienst zurückgegeben werden.

<dl> <dt>

<span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId
</dt> <dd>

Gibt den eindeutigen Bezeichner für die Shell an.

</dd> <dt>

<span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Umgebungsvariablen
</dt> <dd>

Gibt alle vom Benutzer festgelegten Umgebungsvariablen an.

</dd> <dt>

<span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory
</dt> <dd>

Gibt das Startverzeichnis für die Shell an.

</dd> <dt>

<span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI
</dt> <dd>

Gibt den Ressourcen-URI für den Shellvorgang an. Der Ressourcen-URI kann verwendet werden, um die für die Shellinstanz spezifische Plug-In-Konfiguration abzurufen.

</dd> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>Idletimeout
</dt> <dd>

Gibt die maximale Dauer in Millisekunden an, die die Shell ohne Anforderung geöffnet bleibt.

</dd> <dt>

<span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams
</dt> <dd>

Gibt die Eingabestreams für die Shell an.

</dd> <dt>

<span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams
</dt> <dd>

Gibt die Ausgabestreams für die Shell an.

</dd> <dt>

<span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Erstellungszeit der Shell
</dt> <dd>

Gibt den Erstellungszeitstempel für die Shell an.

</dd> <dt>

<span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime
</dt> <dd>

Gibt die Dauer in Millisekunden an, für die sich die Shell im Leerlauf befindet.

</dd> <dt>

<span id="UserId"></span><span id="userid"></span><span id="USERID"></span>Userid
</dt> <dd>

Gibt die Benutzer-ID an.

</dd> <dt>

<span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Hostname oder IP-Adresse
</dt> <dd>

Gibt entweder den Hostnamen oder die IP-Adresse des Computers an, der die Shell erstellt hat.

</dd> <dt>

<span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Shellspeicherauslastung
</dt> <dd>

Gibt die Menge an Arbeitsspeicher an, die von der Shell verwendet wurde.

</dd> <dt>

<span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Anzahl von Prozessen
</dt> <dd>

Gibt die Anzahl der Prozesse an, die von der Shell erstellt wurden.

</dd> </dl>

## <a name="enumerating-a-shell-on-a-local-host"></a>Aufzählen einer Shell auf einem lokalen Host

Der folgende Befehl veranschaulicht die Verwendung des Hilfsprogramms winrm zum Aufzählen von Shells auf einem WinRM-Client: **winrm enumerate shell**.

Im folgenden textbasierten Beispiel wird die Ausgabe für die Shellenumeration angezeigt:

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

Weitere Informationen finden Sie in der Onlinehilfe, die durch Ausführen des folgenden Befehls bereitgestellt wird: **winrm enumerate -?**.

## <a name="retrieving-information-about-a-specific-shell"></a>Abrufen von Informationen zu einer bestimmten Shell

Ein Administrator oder Benutzer kann auch den ShellId-Bezeichner verwenden, um Informationen zur Shell abzurufen. Der folgende Befehl veranschaulicht, wie sie das Hilfsprogramm winrm verwenden, um Informationen zu einer bestimmten Shell zu erhalten: **winrm get shell? ShellId=0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.

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

Weitere Informationen finden Sie in der Onlinehilfe des folgenden Befehls: **winrm get -?**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützung für mehrere Hops](multi-hop-support.md)
</dt> <dt>

[Kontingentverwaltung für Remoteshells](quotas.md)
</dt> <dt>

[Verwaltete Referenz für WS-Management PowerShell-Befehle](winrm-powershell-commandlets.md)
</dt> </dl>

 

 




