---
description: Beschreibt, wie Skripts, Anwendungen und Anbieter Verbindungen mit WMI auf Remotecomputern herstellen können, um Daten zu erhalten oder Hardware und Software zu steuern.
ms.assetid: 16b00ee3-f721-4912-9e8e-2fdbc897a813
ms.tgt_platform: multiple
title: Herstellen einer Verbindung mit WMI auf einem Remotecomputer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fd8c4b592353c10836e8dd5516d9c4f729aed5d968ef4c0e551a05a17c8a05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819716"
---
# <a name="connecting-to-wmi-on-a-remote-computer"></a>Herstellen einer Verbindung mit WMI auf einem Remotecomputer

WMI kann verwendet werden, um WMI-Daten auf Remotecomputern zu verwalten und darauf zu zugreifen. Remoteverbindungen in WMI sind von den Einstellungen Windows [Firewall und](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) DCOM betroffen. [Die Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/aa905108(v=msdn.10)) erfordert möglicherweise auch Änderungen an einigen Einstellungen. Wenn Ihre Einstellungen jedoch korrekt sind, ähnelt der Aufruf eines Remotesystems einem lokalen WMI-Aufruf. Sie können es jedoch komplexer machen, indem Sie unterschiedliche Anmeldeinformationen, alternative Authentifizierungsprotokolle und andere Sicherheitsfeatures verwenden.

## <a name="configuring-a-computer-for-a-remote-connection"></a>Konfigurieren eines Computers für eine Remoteverbindung

Bevor Sie mit WMI auf ein Remotesystem zugreifen können, müssen Sie möglicherweise einige Sicherheitseinstellungen überprüfen, um zu bestätigen, dass Sie Zugriff haben. Dies gilt insbesondere in folgenden Fällen:

-   Windows enthält eine Reihe von Sicherheitsfeatures, die den Zugriff auf Skripts auf Remotesystemen blockieren können. Daher müssen Sie möglicherweise die Active Directory- und Windows-Firewalleinstellungen Ihres Systems ändern, bevor Sie einen WMI-Aufruf tätigen. Weitere Informationen finden Sie unter [Einrichten einer WMI-Remoteverbindung und](connecting-to-wmi-remotely-starting-with-vista.md) [Problembehandlung bei einer Remote-WMI-Verbindung.](troubleshooting-a-remote-wmi-connection.md)

-   Die richtigen DCOM-Einstellungen müssen aktiviert sein, damit eine Remoteverbindung funktioniert. Das Ändern der DCOM-Einstellungen kann Benutzern mit geringen Rechten den Zugriff auf einen Computer für eine Remoteverbindung ermöglichen. Weitere Informationen finden Sie unter [Sichern einer WMI-Remoteverbindung.](securing-a-remote-wmi-connection.md)

Darüber hinaus kann es unter bestimmten Umständen sein, dass Sie WMI über einen festen Port ausführen möchten. Dazu müssen Sie auch Ihre Einstellungen ändern. Weitere Informationen finden Sie unter [Einrichten eines festen Ports für WMI.](setting-up-a-fixed-port-for-wmi.md)

## <a name="connecting-to-a-remote-computer"></a>Herstellen einer Verbindung mit einem Remotecomputer

Im Kern besteht das Herstellen einer Verbindung mit einem Remotesystem mit WMI darin, sicherzustellen, dass Sie über die entsprechenden Berechtigungen für den Zugriff auf das System verfügen und ihre Verbindung ordnungsgemäß konfiguriert ist. Sobald Sie über diese beiden Elemente verfügen, ist die Verbindung selbst relativ einfach. Wenn Sie beispielsweise Ihre Standardsicherheitsanmeldeinformationen verwenden, können Sie mithilfe des folgenden Codes auf WMI auf einem Remotesystem zugreifen:

<dl> <dt>

<span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Herstellen einer Remoteverbindung mit WMI mitHilfe von PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)
</dt> <dd>

Verwenden Sie *den Parameter -ComputerName,* der den meisten WMI-Cmdlets gemeinsam ist, z. [B. Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).


```PowerShell
$strComputer = "Computer_B"
$colSettings = Get-WmiObject Win32_OperatingSystem -ComputerName $strComputer
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Herstellen einer Remoteverbindung mit WMI mit VBScript](connecting-to-wmi-remotely-with-vbscript.md)
</dt> <dd>

Verwenden Sie einen Moniker, der den Namen des Remotesystems im Aufruf von [**GetObject enthält.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)


```VB
strComputer = "Computer_B"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSettings = objWMIService.ExecQuery("Select * from Win32_OperatingSystem")
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Herstellen einer Remoteverbindung mit WMI mit C #](connecting-to-wmi-remotely-with-c-.md)
</dt> <dd>

Verwenden Sie für die aktuelle Version der verwalteten WMI-Schnittstelle ([Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))) das [CimSession-Objekt,](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) um eine Verbindung mit einem Remotehost zu darstellen.


```CSharp
using Microsoft.Management.Infrastructure;
...
string Namespace = @"root\cimv2";
string OSQuery = "SELECT * FROM Win32_OperatingSystem";
CimSession mySession = CimSession.Create("Computer_B");
IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Herstellen einer Remoteverbindung mit WMI mit C #](connecting-to-wmi-remotely-with-c-.md)
</dt> <dd>

Verwenden Sie für die v1-Version der von WMI verwalteten Schnittstelle ([System.Management](/dotnet/api/system.management)) das [ManagementScope-Objekt,](/dotnet/api/system.management.managementscope) um eine Verbindung mit einem Remotehost zu darstellen.


```CSharp
using System.Management;
...
ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
scope.Connect();
ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
```



</dd> <dt>

<span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Beispiel: Abrufen von WMI-Daten von einem Remotecomputer (C++)](example--getting-wmi-data-from-a-remote-computer.md)
</dt> <dd>

Verwenden Sie [**die IWbemLocator::ConnectServer-Methode,**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) um den Namen des Remotecomputers im *parameter strNetworkResource* anzugeben.


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

Die vorherigen Codebeispiele sind wohl die grundlegendste Remoteverbindung, die Sie mit WMI ausführen können. In den Beispielen wird insbesondere Folgendes angenommen:

-   Sie sind Administrator auf dem Remotecomputer. Aufgrund der [Benutzerkontensteuerung muss](/previous-versions/aa905108(v=msdn.10))das Konto auf dem Remotesystem ein Domänenkonto in der Gruppe Administratoren sein. Weitere Informationen finden Sie unter Benutzerkontensteuerung und WMI.
-   Das Kennwort auf Dem aktuellen lokalen Computer ist nicht leer. Dies ist im Wesentlichen Windows Sicherheitsanforderung, dass Sie sich mit einem Kennwort bei Ihrem System angemeldet haben müssen.
-   Sowohl Ihr lokaler als auch der Remotecomputer befinden sich in derselben Domäne. Wenn Sie Domänengrenzen überschreiten müssen, müssen Sie zusätzliche Informationen liefern oder ein etwas anderes Programmiermodell verwenden.
-   Sie verwenden Ihr eigenes Konto für den Zugriff auf den Remotecomputer. Wenn Sie versuchen, auf ein anderes Konto zu zugreifen, müssen Sie zusätzliche Anmeldeinformationen angeben. (Beachten Sie, dass der Versuch, lokal mit Anmeldeinformationen, die sich von Ihrem aktuellen Konto unterscheiden, auf WMI zu zugreifen, nicht zulässig ist.)
-   Auf beiden Computern wird IPv6 ausgeführt. WMI unterstützt Verbindungen mit Computern, auf denen IPv6 ausgeführt wird. Allerdings muss sowohl auf Ihrem lokalen Computer als auch auf "Computer \_ B" IPv6 ausgeführt werden. Auf beiden Computern wird möglicherweise auch IPv4 ausgeführt. Weitere Informationen finden Sie unter [IPv6- und IPv4-Unterstützung in WMI.](ipv6-and-ipv4-support-in-wmi.md)
-   Ihr Skript muss nicht delegieren. Das heißt, es muss nicht über den Ziel-Remotecomputer auf zusätzliche Remotecomputer zugreifen. Weitere Informationen finden Sie unter [Delegieren mit WMI.](connecting-to-a-3rd-computer-delegation.md)
-   Sie versuchen, einen bestimmten Aufruf zu erstellen, anstatt einen Remoteprozess zu erstellen. Weitere Informationen finden Sie unter [Remote erstellen von Prozessen mit WMI.](creating-processes-remotely.md)

Vor diesem Hintergrund ist ein Remote-WMI-Aufruf einem lokalen WMI-Aufruf sehr ähnlich. Der einzige Unterschied besteht in der Angabe des Namens des Remotesystems. Sie können jedoch viele dieser Features ändern: verwenden Sie unterschiedliche Anmeldeinformationen, weiterleiten Sie Ihren Anruf über einen Drittanbietercomputer, oder greifen Sie auf eine andere Domäne zu.

 

 
