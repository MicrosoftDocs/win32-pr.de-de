---
description: Herstellen einer Remoteverbindung mit WMI mit PowerShell
ms.assetid: 9a06f0c3-2845-48aa-9988-79cc4607ce19
ms.tgt_platform: multiple
title: Herstellen einer Remoteverbindung mit WMI mit PowerShell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d499c59ee6774b1e972e192dfc2c0d1228469196c66e8f3feb80d1c9d6339c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679870"
---
# <a name="connecting-to-wmi-remotely-with-powershell"></a>Herstellen einer Remoteverbindung mit WMI mit PowerShell

Windows PowerShell bietet einen einfachen Mechanismus zum Herstellen einer Verbindung mit Windows Management Instrumentation (WMI) auf einem Remotecomputer. Remoteverbindungen in WMI sind von [den Windows Firewall,](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11))DCOM-Einstellungen und [der Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/aa905108(v=msdn.10))betroffen. Weitere Informationen zum Konfigurieren von Remoteverbindungen finden Sie unter [Connecting to WMI Remotely Starting with Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).

Die Beispiele in diesem Thema basieren auf vbscripts von Herstellen einer [Verbindung mit WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md) In allen Beispielen in diesem Thema wird das Cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) verwendet. Weitere Informationen finden Sie unter [Get-WmiObject.](/previous-versions//dd315295(v=technet.10))

## <a name="windows-powershell-examples"></a>Windows PowerShell Beispiele

Beim Erstellen einer Verbindung mit einem Remotecomputer kann ein Benutzer die Verbindungsinformationen wie den Remotecomputernamen, die Anmeldeinformationen und die Authentifizierungsebene für die Verbindung angeben. Die folgenden Beispiele veranschaulichen das Herstellen einer Verbindung mit einem Remotecomputer mithilfe verschiedener Sätze von Anmeldeinformationen und den Zugriff auf WMI-Informationen.

Das folgende Windows PowerShell Beispiel zeigt das Festlegen der Identitätswechselebene:


```PowerShell

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -ComputerName Computer_B
```



Im vorherigen Beispiel stellt der Benutzer eine Verbindung mit einem Remotecomputer her, indem er die gleichen Anmeldeinformationen (Domäne und Benutzername) verwendet, mit denen er sich angemeldet hat. Der Benutzer hat außerdem die Verwendung des Identitätswechsels angefordert. Im Gegensatz zum ursprünglichen VBScript-Beispiel ist eine Monikerzeichenfolge nicht erforderlich, da die Identitätswechselebene durch die Eigenschaft "Identitätswechsel" festgelegt wird. Standardmäßig ist die Identitätswechselebene auf 3 (Identitätswechsel) festgelegt.

Im Beispiel werden alle Instanzen der [**Win32 \_ Process-Klasse**](/windows/desktop/CIMWin32Prov/win32-process) aufgelistet, die auf einem Remotecomputer ausgeführt werden.

> [!Note]  
> Sie sollten den WMI-Namespace angeben, mit dem eine Verbindung auf dem Remotecomputer hergestellt werden soll, da es möglich ist, dass der Standardnamespace auf verschiedenen Computern nicht identisch ist.

 

Im folgenden Windows PowerShell Beispiel wird gezeigt, wie Sie eine Verbindung mit einem Remotecomputer mit unterschiedlichen Anmeldeinformationen herstellen und die Identitätswechselebene auf 3 festlegen, also Identitätswechsel:


```PowerShell

$Computer = "atl-dc-01"

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -Credential `
FABRIKAM\administrator -ComputerName $Computer
```



Im vorherigen Beispiel wurde der Computername der variablen $Computer zugewiesen. Der Benutzer stellt mit bestimmten Anmeldeinformationen (Domäne und Benutzername) eine Verbindung mit einem Remotecomputer her und fordert einen Identitätswechsel für die Authentifizierungsebene an.

> [!Note]  
> Das Akzentzeichen \` () wird verwendet, um einen Zeilenbruch anzugeben. Er entspricht dem Unterstrich ( \_ ) in VBScript.

 

The following Windows PowerShell example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of [**Win32\_PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)—on each computer:


```PowerShell
$ArrComputers = "Computer1", "Computer2", "Computer3"
foreach ($Computer in $ArrComputers) 
{
write-host ""
write-host "===================================="
write-host "Computer: $Computer"
write-host "===================================="

write-host "-----------------------------------"
write-host "Win32_PnPEntity instance"
write-host "-----------------------------------"

$ColItems = Get-WmiObject -Class Win32_PnPEntity -Namespace "root\cimv2" -Computer $Computer
$ColItems[0..47] | Format-List Name, Status
}
```



> [!Note]  
> Zum Ausführen des obigen Windows PowerShell Skripts müssen Sie administrator auf den Remotecomputern sein. Beachten Sie außerdem im Zusammenhang mit dem vorherigen Beispiel Folgendes:

 

-   Die Computernamen im Array müssen in Anführungszeichen eingeschlossen werden, da es sich um Zeichenfolgen handelt.
-   Die vom [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) zurückgegebenen Objekte werden der $ColItems Variablen zugewiesen.
-   The range operator \[\] limited the list of Plug and Play devices to 48 instances. Weitere Informationen finden Sie unter [Informationen zu \_ Operatoren.](/previous-versions//dd347588(v=technet.10))
-   "" \| ist das Pipelinezeichen. Das von ColItems zurückgegebene Objekt wird an das [Format-List-Cmdlet]( /previous-versions//dd347700(v=technet.10)) gesendet.

Im folgenden Windows PowerShell Beispiel können Sie eine Verbindung mit einem Remotecomputer in einer anderen Domäne herstellen. In diesem Beispiel werden auch die Prozessnamen für Instanzen des [**\_ Win32-Prozesses**](/windows/desktop/CIMWin32Prov/win32-process) auf dem Remotecomputer angezeigt.


```PowerShell
$Computer = "FullComputerName" 
$Domain = "DOMAIN"
$Credential = Get-Credential
$ColItems = Get-WmiObject -Class Win32_Process -Authority "ntlmdomain:$Domain" `
-Credential $Credential -Locale "MS_409" -Namespace "root\cimv2"  -ComputerName $Computer

foreach ($ObjItem in $colItems) 
{
write-host "Process Name:" $ObjItem.name
}
```



> [!Note]  
> Zum Ausführen des obigen Windows PowerShell Skripts müssen Sie Administrator auf dem Remotecomputer sein.

 

Im vorherigen Beispiel stellt der Benutzer eine Verbindung mit einem Remotecomputer in einer anderen Domäne her und gibt ein bevorzugtes Gebietsschema an. Der Befehl [Get-Credential](/previous-versions//dd315327(v=technet.10)) fordert die Anmeldeinformationen des Benutzers an und weist die Anmeldeinformationen einem Objekt zu. Im Beispiel werden auch die Namen der Instanzen der [**Win32 \_ Process-Klasse**](/windows/desktop/CIMWin32Prov/win32-process) aufgelistet, die auf dem Computer ausgeführt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Herstellen einer Verbindung mit WMI auf einem Remotecomputer](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
