---
description: Beschreibt, wie-Skripts,-Anwendungen und-Anbieter Verbindungen mit WMI auf Remote Computern herstellen können, um Daten abzurufen oder Hardware und Software zu steuern.
ms.assetid: 16b00ee3-f721-4912-9e8e-2fdbc897a813
ms.tgt_platform: multiple
title: Herstellen einer Verbindung mit WMI auf einem Remote Computer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d581d1be73013e57ef2193102f6e8afc287b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362820"
---
# <a name="connecting-to-wmi-on-a-remote-computer"></a>Herstellen einer Verbindung mit WMI auf einem Remote Computer

WMI kann zum Verwalten von und Zugreifen auf WMI-Daten auf Remote Computern verwendet werden. Remote Verbindungen in WMI werden von der [Windows-Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) und den DCOM-Einstellungen beeinflusst. Die [Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/aa905108(v=msdn.10)) erfordert möglicherweise auch Änderungen an einigen Einstellungen. Wenn Ihre Einstellungen jedoch richtig sind, ähnelt der Remote Systemaufrufe einem lokalen WMI-Rückruf. Sie können es jedoch mithilfe verschiedener Anmelde Informationen, alternativer Authentifizierungsprotokolle und anderer Sicherheitsfeatures komplexer gestalten.

## <a name="configuring-a-computer-for-a-remote-connection"></a>Konfigurieren eines Computers für eine Remote Verbindung

Bevor Sie mit WMI auf ein Remote System zugreifen können, müssen Sie möglicherweise einige Sicherheitseinstellungen überprüfen, um zu bestätigen, dass Sie Zugriff haben. Dies gilt insbesondere in folgenden Fällen:

-   Windows enthält eine Reihe von Sicherheitsfunktionen, die den Zugriff auf Skripts auf Remote Systemen blockieren können. Daher müssen Sie möglicherweise die Active Directory-und Windows-Firewall-Einstellungen Ihres Systems ändern, bevor Sie einen WMI-Befehl ausführen. Weitere Informationen finden Sie unter [Einrichten einer Remote-WMI-Verbindung](connecting-to-wmi-remotely-starting-with-vista.md) und Problembehandlung für [eine Remote-WMI-Verbindung](troubleshooting-a-remote-wmi-connection.md).

-   Die richtigen DCOM-Einstellungen müssen aktiviert werden, damit eine Remote Verbindung funktioniert. Wenn Sie DCOM-Einstellungen ändern, können Benutzer mit geringen Rechten auf einen Computer für eine Remote Verbindung zugreifen. Weitere Informationen finden Sie unter [Sichern einer Remote-WMI-Verbindung](securing-a-remote-wmi-connection.md).

Außerdem kann es Situationen geben, in denen Sie WMI als einen festgelegten Port ausführen möchten. Zu diesem Zweck müssen Sie auch Ihre Einstellungen ändern. Weitere Informationen finden Sie unter [Einrichten eines Fixed-Ports für WMI](setting-up-a-fixed-port-for-wmi.md).

## <a name="connecting-to-a-remote-computer"></a>Herstellen einer Verbindung mit einem Remote Computer

Das Herstellen einer Verbindung mit einem Remote System mit WMI besteht darin, sicherzustellen, dass Sie über die entsprechenden Berechtigungen für den Zugriff auf das System verfügen und dass die Verbindung ordnungsgemäß konfiguriert ist. Wenn Sie über diese beiden Elemente verfügen, ist die Verbindung selbst relativ einfach. Wenn Sie z. b. die standardmäßigen Sicherheits Anmelde Informationen verwenden, können Sie auf WMI auf einem Remote System zugreifen, indem Sie den folgenden Code verwenden:

<dl> <dt>

<span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Remote Verbindung mit WMI mithilfe von PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)
</dt> <dd>

Verwenden Sie den Parameter " *-Computername* ", der den meisten WMI-Cmdlets entspricht, z. b. [Get-WMIObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).


```PowerShell
$strComputer = "Computer_B"
$colSettings = Get-WmiObject Win32_OperatingSystem -ComputerName $strComputer
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Remote Verbindung mit WMI mit VBScript](connecting-to-wmi-remotely-with-vbscript.md)
</dt> <dd>

Verwenden Sie einen Moniker, der den Namen des Remote Systems im Aufruf von [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)enthält.


```VB
strComputer = "Computer_B"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSettings = objWMIService.ExecQuery("Select * from Win32_OperatingSystem")
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Remote Verbindung mit WMI mit C #](connecting-to-wmi-remotely-with-c-.md)
</dt> <dd>

Verwenden Sie für die aktuelle Version der verwalteten WMI-Schnittstelle ([Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))) das [cimsession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) -Objekt, um eine Verbindung mit einem Remote Host darzustellen.


```CSharp
using Microsoft.Management.Infrastructure;
...
string Namespace = @"root\cimv2";
string OSQuery = "SELECT * FROM Win32_OperatingSystem";
CimSession mySession = CimSession.Create("Computer_B");
IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Remote Verbindung mit WMI mit C #](connecting-to-wmi-remotely-with-c-.md)
</dt> <dd>

Verwenden Sie für die v1-Version der verwalteten WMI-Schnittstelle ([System. Management](/dotnet/api/system.management)) das [ManagementScope](/dotnet/api/system.management.managementscope) -Objekt, um eine Verbindung mit einem Remote Host darzustellen.


```CSharp
using System.Management;
...
ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
scope.Connect();
ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
```



</dd> <dt>

<span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Beispiel: erhalten von WMI-Daten von einem Remote Computer (C++)](example--getting-wmi-data-from-a-remote-computer.md)
</dt> <dd>

Verwenden Sie die [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) -Methode, um den Namen des Remote Computers im *Parameter "* " "" "" "".


```CSharp
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTER_B\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
        );
```



</dd> </dl>

Die vorherigen Codebeispiele sind wohl die einfachste Remote Verbindung, die Sie mit WMI ausführen können. In den Beispielen wird Folgendes vorausgesetzt:

-   Sie sind ein Administrator auf dem Remote Computer. Aufgrund der [Benutzerkontensteuerung](/previous-versions/aa905108(v=msdn.10))muss das Konto auf dem Remote System ein Domänen Konto in der Gruppe "Administratoren" sein. Weitere Informationen finden Sie unter Benutzerkontensteuerung und WMI.
-   Das Kennwort auf dem aktuellen lokalen Computer ist nicht leer. Dabei handelt es sich im Wesentlichen um eine Windows-Sicherheitsanforderung, die Sie mit einem Kennwort bei Ihrem System angemeldet haben müssen.
-   Sowohl der lokale als auch der Remote Computer befinden sich in derselben Domäne. Wenn Sie Domänen übergreifende Grenzen benötigen, müssen Sie zusätzliche Informationen bereitstellen oder ein etwas anderes Programmiermodell verwenden.
-   Sie verwenden Ihr eigenes Konto, um auf den Remote Computer zuzugreifen. Wenn Sie versuchen, auf ein anderes Konto zuzugreifen, müssen Sie zusätzliche Anmelde Informationen angeben. (Beachten Sie, dass der Versuch, lokal mit anderen Anmelde Informationen als Ihrem aktuellen Konto auf WMI zuzugreifen, nicht zulässig ist.)
-   Auf beiden Computern wird IPv6 ausgeführt. WMI unterstützt Verbindungen mit Computern, auf denen IPv6 ausgeführt wird. Auf dem lokalen Computer und auf dem Computer \_ B muss jedoch IPv6 ausgeführt werden. Beide Computer können auch IPv4 ausführen. Weitere Informationen finden Sie [unter IPv6-und IPv4-Unterstützung in WMI](ipv6-and-ipv4-support-in-wmi.md).
-   Ihr Skript muss nicht delegiert werden, d. h., es ist nicht erforderlich, über den Ziel-Remote Computer auf zusätzliche Remote Computer zuzugreifen. Weitere Informationen finden Sie unter [delegieren mit WMI](connecting-to-a-3rd-computer-delegation.md).
-   Sie versuchen, einen bestimmten-Befehl zu erstellen, anstatt einen Remote Prozess zu erstellen. Weitere Informationen finden Sie unter [Erstellen von Prozessen per Remote Verbindung mithilfe von WMI](creating-processes-remotely.md).

Mit diesen Einschränkungen ist ein WMI-Remote Rückruf sehr ähnlich wie bei einem lokalen WMI-Rückruf. der einzige Unterschied besteht darin, dass Sie den Namen des Remote Systems angeben müssen. Sie haben jedoch die Möglichkeit, viele dieser Features zu ändern, indem Sie unterschiedliche Anmelde Informationen verwenden oder den Anrufen über einen Drittanbieter Computer weiterleiten oder auf eine andere Domäne zugreifen.

 

 
