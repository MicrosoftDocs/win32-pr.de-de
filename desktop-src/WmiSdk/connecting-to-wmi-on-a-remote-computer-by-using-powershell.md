---
description: Remote Verbindung mit WMI mithilfe von PowerShell
ms.assetid: 9a06f0c3-2845-48aa-9988-79cc4607ce19
ms.tgt_platform: multiple
title: Remote Verbindung mit WMI mithilfe von PowerShell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a2bb1ad982a20a10dbadd89856d118f1be9bd82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755352"
---
# <a name="connecting-to-wmi-remotely-with-powershell"></a>Remote Verbindung mit WMI mithilfe von PowerShell

Windows PowerShell bietet einen einfachen Mechanismus zum Herstellen einer Verbindung mit Windows-Verwaltungsinstrumentation (WMI) auf einem Remote Computer. Remote Verbindungen in WMI sind von der [Windows-Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), den DCOM-Einstellungen und der [Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/aa905108(v=msdn.10))betroffen. Weitere Informationen zum Konfigurieren von Remote Verbindungen finden Sie unter Herstellen einer Remote [Verbindung mit WMI ab Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).

Die Beispiele in diesem Thema basieren darauf, dass die VBScripts [eine Verbindung mit WMI auf einem Remote Computer herstellen](connecting-to-wmi-on-a-remote-computer.md). Alle Beispiele in diesem Thema verwenden das [Get-WMIObject](/previous-versions//dd315295(v=technet.10)) -Cmdlet. Weitere Informationen finden Sie unter [Get-WMIObject](/previous-versions//dd315295(v=technet.10)).

## <a name="windows-powershell-examples"></a>Windows PowerShell-Beispiele

Beim Herstellen einer Verbindung mit einem Remote Computer kann ein Benutzer die Verbindungsinformationen angeben, z. b. den Remote Computernamen, die Anmelde Informationen und die Authentifizierungs Ebene für die Verbindung. In den folgenden Beispielen wird veranschaulicht, wie Sie eine Verbindung mit einem Remote Computer mithilfe verschiedener Sätze von Anmelde Informationen herstellen und wie Sie auf WMI-Informationen zugreifen.

Das folgende Windows PowerShell-Beispiel zeigt das Festlegen der Identitätswechsel Ebene:


```PowerShell

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -ComputerName Computer_B
```



Im vorherigen Beispiel stellt der Benutzer mit denselben Anmelde Informationen (Domäne und Benutzername), mit denen Sie sich angemeldet haben, eine Verbindung mit einem Remote Computer her. Der Benutzer hat auch angefordert, den Identitätswechsel zu verwenden. Im Gegensatz zum ursprünglichen VBScript-Beispiel wird eine Monikerzeichenfolge nicht benötigt, da die Identitätswechsel Ebene von der Eigenschaft "Identitätswechsel" festgelegt wird. Standardmäßig ist die Ebene des Identitäts Wechsels auf 3 (Identität annehmen) festgelegt.

Im Beispiel werden alle Instanzen der Win32- [**\_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse aufgelistet, die auf dem Remote Computer ausgeführt werden.

> [!Note]  
> Geben Sie den WMI-Namespace an, mit dem auf dem Remote Computer eine Verbindung hergestellt werden soll, da der Standard Namespace auf unterschiedlichen Computern möglicherweise nicht identisch ist.

 

Das folgende Windows PowerShell-Beispiel zeigt, wie Sie eine Verbindung mit einem Remote Computer mit unterschiedlichen Anmelde Informationen herstellen und die Identitätswechsel Ebene auf 3 festlegen, dessen Identität angenommen wird:


```PowerShell

$Computer = "atl-dc-01"

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -Credential `
FABRIKAM\administrator -ComputerName $Computer
```



Im vorherigen Beispiel wurde der Computername der $Computer Variablen zugewiesen. Der Benutzer stellt eine Verbindung mit einem Remote Computer mithilfe spezifischer Anmelde Informationen (Domäne und Benutzername) her und fordert Identitätswechsel für die Authentifizierungs Ebene an.

> [!Note]  
> Das Zeichen mit einem Doppel Akzent ( \` ) wird verwendet, um einen Zeilenumbruch anzugeben. Dies entspricht dem Unterstrich Zeichen ( \_ ) in VBScript.

 

Im folgenden Windows PowerShell-Beispiel wird eine Verbindung mit einer Gruppe von Remote Computern in derselben Domäne hergestellt, indem ein Array von Remote Computernamen erstellt und dann die Namen der Plug & Play Geräte – Instanzen von [**Win32 \_ pnptity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)– auf den einzelnen Computern angezeigt werden:


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
> Um das vorangehende Windows PowerShell-Skript auszuführen, müssen Sie Administrator auf den Remote Computern sein. Beachten Sie außerdem Folgendes im Zusammenhang mit dem vorherigen Beispiel:

 

-   Die Computernamen im Array müssen in Anführungszeichen eingeschlossen werden, da Sie Zeichen folgen sind.
-   Die vom [Get-WMIObject](/previous-versions//dd315295(v=technet.10)) zurückgegebenen Objekte werden der $ColItems Variablen zugewiesen.
-   Der Bereichs Operator \[ \] beschränkte die Liste der Plug & Play Geräte auf 48 Instanzen. Weitere Informationen finden Sie unter Informationen [zu \_ Operatoren](/previous-versions//dd347588(v=technet.10)).
-   " \| " Ist das Pipeline Zeichen. Das von "colItems" zurückgegebene Objekt wird an das Cmdlet " [Format-List]( /previous-versions//dd347700(v=technet.10)) " gesendet.

Das folgende Windows PowerShell-Beispiel ermöglicht es Ihnen, eine Verbindung mit einem Remote Computer in einer anderen Domäne herzustellen. In diesem Beispiel werden auch die Prozessnamen für Instanzen des [**Win32- \_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process) auf dem Remote Computer angezeigt.


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
> Um das vorangehende Windows PowerShell-Skript auszuführen, müssen Sie Administrator auf dem Remote Computer sein.

 

Im vorherigen Beispiel stellt der Benutzer eine Verbindung mit einem Remote Computer in einer anderen Domäne her und gibt ein bevorzugtes Gebiets Schema an. Der [Get-Credential](/previous-versions//dd315327(v=technet.10)) -Befehl fordert die Anmelde Informationen des Benutzers an und weist die Anmelde Informationen einem Objekt zu. Im Beispiel werden auch die Namen von Instanzen der [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse aufgelistet, die auf dem Computer ausgeführt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
