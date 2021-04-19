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
# <a name="connecting-to-wmi-on-a-remote-computer"></a><span data-ttu-id="31ce8-103">Herstellen einer Verbindung mit WMI auf einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="31ce8-103">Connecting to WMI on a Remote Computer</span></span>

<span data-ttu-id="31ce8-104">WMI kann zum Verwalten von und Zugreifen auf WMI-Daten auf Remote Computern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31ce8-104">WMI can be used to manage and access WMI data on remote computers.</span></span> <span data-ttu-id="31ce8-105">Remote Verbindungen in WMI werden von der [Windows-Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) und den DCOM-Einstellungen beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="31ce8-105">Remote connections in WMI are affected by the [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) and DCOM settings.</span></span> <span data-ttu-id="31ce8-106">Die [Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/aa905108(v=msdn.10)) erfordert möglicherweise auch Änderungen an einigen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="31ce8-106">[User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)) may also require changes to some settings.</span></span> <span data-ttu-id="31ce8-107">Wenn Ihre Einstellungen jedoch richtig sind, ähnelt der Remote Systemaufrufe einem lokalen WMI-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="31ce8-107">However, once your have your settings correct, the call to a remote system is very similar to a local WMI call.</span></span> <span data-ttu-id="31ce8-108">Sie können es jedoch mithilfe verschiedener Anmelde Informationen, alternativer Authentifizierungsprotokolle und anderer Sicherheitsfeatures komplexer gestalten.</span><span class="sxs-lookup"><span data-stu-id="31ce8-108">You may choose to make it more complex however, by using different credentials, alternate authentication protocols, and other security features.</span></span>

## <a name="configuring-a-computer-for-a-remote-connection"></a><span data-ttu-id="31ce8-109">Konfigurieren eines Computers für eine Remote Verbindung</span><span class="sxs-lookup"><span data-stu-id="31ce8-109">Configuring a Computer for a Remote Connection</span></span>

<span data-ttu-id="31ce8-110">Bevor Sie mit WMI auf ein Remote System zugreifen können, müssen Sie möglicherweise einige Sicherheitseinstellungen überprüfen, um zu bestätigen, dass Sie Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="31ce8-110">Before you can access a remote system with WMI, you may need to check some security settings to confirm that you have access.</span></span> <span data-ttu-id="31ce8-111">Dies gilt insbesondere in folgenden Fällen:</span><span class="sxs-lookup"><span data-stu-id="31ce8-111">Specifically:</span></span>

-   <span data-ttu-id="31ce8-112">Windows enthält eine Reihe von Sicherheitsfunktionen, die den Zugriff auf Skripts auf Remote Systemen blockieren können.</span><span class="sxs-lookup"><span data-stu-id="31ce8-112">Windows contains a number of security features that may block access to scripts on remote systems.</span></span> <span data-ttu-id="31ce8-113">Daher müssen Sie möglicherweise die Active Directory-und Windows-Firewall-Einstellungen Ihres Systems ändern, bevor Sie einen WMI-Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="31ce8-113">As such, you may need to modify your system's Active Directory and Windows Firewall settings before making a WMI call.</span></span> <span data-ttu-id="31ce8-114">Weitere Informationen finden Sie unter [Einrichten einer Remote-WMI-Verbindung](connecting-to-wmi-remotely-starting-with-vista.md) und Problembehandlung für [eine Remote-WMI-Verbindung](troubleshooting-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="31ce8-114">For more information, see [Setting up a Remote WMI Connection](connecting-to-wmi-remotely-starting-with-vista.md) and [Troubleshooting a Remote WMI Connection](troubleshooting-a-remote-wmi-connection.md).</span></span>

-   <span data-ttu-id="31ce8-115">Die richtigen DCOM-Einstellungen müssen aktiviert werden, damit eine Remote Verbindung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="31ce8-115">The correct DCOM settings must be enabled for a remote connection to work.</span></span> <span data-ttu-id="31ce8-116">Wenn Sie DCOM-Einstellungen ändern, können Benutzer mit geringen Rechten auf einen Computer für eine Remote Verbindung zugreifen.</span><span class="sxs-lookup"><span data-stu-id="31ce8-116">Changing DCOM settings can allow low rights users access to a computer for a remote connection.</span></span> <span data-ttu-id="31ce8-117">Weitere Informationen finden Sie unter [Sichern einer Remote-WMI-Verbindung](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="31ce8-117">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

<span data-ttu-id="31ce8-118">Außerdem kann es Situationen geben, in denen Sie WMI als einen festgelegten Port ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="31ce8-118">In addition, there may be some circumstances in which you may wish to run WMI though a fixed port.</span></span> <span data-ttu-id="31ce8-119">Zu diesem Zweck müssen Sie auch Ihre Einstellungen ändern.</span><span class="sxs-lookup"><span data-stu-id="31ce8-119">To do this, you will also need to change your settings.</span></span> <span data-ttu-id="31ce8-120">Weitere Informationen finden Sie unter [Einrichten eines Fixed-Ports für WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="31ce8-120">For more information, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

## <a name="connecting-to-a-remote-computer"></a><span data-ttu-id="31ce8-121">Herstellen einer Verbindung mit einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="31ce8-121">Connecting to a Remote Computer</span></span>

<span data-ttu-id="31ce8-122">Das Herstellen einer Verbindung mit einem Remote System mit WMI besteht darin, sicherzustellen, dass Sie über die entsprechenden Berechtigungen für den Zugriff auf das System verfügen und dass die Verbindung ordnungsgemäß konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="31ce8-122">At its heart, connecting to a remote system with WMI consists of making sure that you have the appropriate permissions to access the system, and that your connection is properly configured.</span></span> <span data-ttu-id="31ce8-123">Wenn Sie über diese beiden Elemente verfügen, ist die Verbindung selbst relativ einfach.</span><span class="sxs-lookup"><span data-stu-id="31ce8-123">Once you have those two elements, the connection itself is relatively simple.</span></span> <span data-ttu-id="31ce8-124">Wenn Sie z. b. die standardmäßigen Sicherheits Anmelde Informationen verwenden, können Sie auf WMI auf einem Remote System zugreifen, indem Sie den folgenden Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="31ce8-124">For example, if you are using your default security credentials, you can access WMI on a remote system using the following code:</span></span>

<dl> <dt>

<span data-ttu-id="31ce8-125"><span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Remote Verbindung mit WMI mithilfe von PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="31ce8-125"><span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Connecting to WMI Remotely with PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)</span></span>
</dt> <dd>

<span data-ttu-id="31ce8-126">Verwenden Sie den Parameter " *-Computername* ", der den meisten WMI-Cmdlets entspricht, z. b. [Get-WMIObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="31ce8-126">Use the *-ComputerName* parameter common to most WMI cmdlets, such as [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).</span></span>


```PowerShell
$strComputer = "Computer_B"
$colSettings = Get-WmiObject Win32_OperatingSystem -ComputerName $strComputer
```



</dd> <dt>

<span data-ttu-id="31ce8-127"><span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Remote Verbindung mit WMI mit VBScript](connecting-to-wmi-remotely-with-vbscript.md)</span><span class="sxs-lookup"><span data-stu-id="31ce8-127"><span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Connecting to WMI Remotely with VBScript](connecting-to-wmi-remotely-with-vbscript.md)</span></span>
</dt> <dd>

<span data-ttu-id="31ce8-128">Verwenden Sie einen Moniker, der den Namen des Remote Systems im Aufruf von [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)enthält.</span><span class="sxs-lookup"><span data-stu-id="31ce8-128">Use a moniker that contains the name of the remote system in the call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>


```VB
strComputer = "Computer_B"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSettings = objWMIService.ExecQuery("Select * from Win32_OperatingSystem")
```



</dd> <dt>

<span data-ttu-id="31ce8-129"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Remote Verbindung mit WMI mit C #](connecting-to-wmi-remotely-with-c-.md)</span><span class="sxs-lookup"><span data-stu-id="31ce8-129"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connecting to WMI Remotely with C#](connecting-to-wmi-remotely-with-c-.md)</span></span>
</dt> <dd>

<span data-ttu-id="31ce8-130">Verwenden Sie für die aktuelle Version der verwalteten WMI-Schnittstelle ([Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))) das [cimsession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) -Objekt, um eine Verbindung mit einem Remote Host darzustellen.</span><span class="sxs-lookup"><span data-stu-id="31ce8-130">For the current version of the WMI managed interface ([Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))), use the [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object to represent a connection to a remote host.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
string Namespace = @"root\cimv2";
string OSQuery = "SELECT * FROM Win32_OperatingSystem";
CimSession mySession = CimSession.Create("Computer_B");
IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
```



</dd> <dt>

<span data-ttu-id="31ce8-131"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Remote Verbindung mit WMI mit C #](connecting-to-wmi-remotely-with-c-.md)</span><span class="sxs-lookup"><span data-stu-id="31ce8-131"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connecting to WMI Remotely with C#](connecting-to-wmi-remotely-with-c-.md)</span></span>
</dt> <dd>

<span data-ttu-id="31ce8-132">Verwenden Sie für die v1-Version der verwalteten WMI-Schnittstelle ([System. Management](/dotnet/api/system.management)) das [ManagementScope](/dotnet/api/system.management.managementscope) -Objekt, um eine Verbindung mit einem Remote Host darzustellen.</span><span class="sxs-lookup"><span data-stu-id="31ce8-132">For the v1 version of the WMI managed interface ([System.Management](/dotnet/api/system.management)), use the [ManagementScope](/dotnet/api/system.management.managementscope) object to represent a connection to a remote host.</span></span>


```CSharp
using System.Management;
...
ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
scope.Connect();
ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
```



</dd> <dt>

<span data-ttu-id="31ce8-133"><span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Beispiel: erhalten von WMI-Daten von einem Remote Computer (C++)](example--getting-wmi-data-from-a-remote-computer.md)</span><span class="sxs-lookup"><span data-stu-id="31ce8-133"><span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Example: Getting WMI Data from a Remote Computer (C++)](example--getting-wmi-data-from-a-remote-computer.md)</span></span>
</dt> <dd>

<span data-ttu-id="31ce8-134">Verwenden Sie die [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) -Methode, um den Namen des Remote Computers im *Parameter "* " "" "" "".</span><span class="sxs-lookup"><span data-stu-id="31ce8-134">Use the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method to specify the name of the remote computer in the *strNetworkResource* parameter.</span></span>


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

<span data-ttu-id="31ce8-135">Die vorherigen Codebeispiele sind wohl die einfachste Remote Verbindung, die Sie mit WMI ausführen können.</span><span class="sxs-lookup"><span data-stu-id="31ce8-135">The previous code samples are arguably the most basic remote connection you can perform with WMI.</span></span> <span data-ttu-id="31ce8-136">In den Beispielen wird Folgendes vorausgesetzt:</span><span class="sxs-lookup"><span data-stu-id="31ce8-136">Specifically, the samples assume the following:</span></span>

-   <span data-ttu-id="31ce8-137">Sie sind ein Administrator auf dem Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="31ce8-137">You are an administrator on the remote machine.</span></span> <span data-ttu-id="31ce8-138">Aufgrund der [Benutzerkontensteuerung](/previous-versions/aa905108(v=msdn.10))muss das Konto auf dem Remote System ein Domänen Konto in der Gruppe "Administratoren" sein.</span><span class="sxs-lookup"><span data-stu-id="31ce8-138">Due to [User Account Control](/previous-versions/aa905108(v=msdn.10)), the account on the remote system must be a domain account in the Administrators group.</span></span> <span data-ttu-id="31ce8-139">Weitere Informationen finden Sie unter Benutzerkontensteuerung und WMI.</span><span class="sxs-lookup"><span data-stu-id="31ce8-139">For more information, see User Account Control and WMI.</span></span>
-   <span data-ttu-id="31ce8-140">Das Kennwort auf dem aktuellen lokalen Computer ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="31ce8-140">The password on your current local machine is not blank.</span></span> <span data-ttu-id="31ce8-141">Dabei handelt es sich im Wesentlichen um eine Windows-Sicherheitsanforderung, die Sie mit einem Kennwort bei Ihrem System angemeldet haben müssen.</span><span class="sxs-lookup"><span data-stu-id="31ce8-141">This is essentially a Windows security requirement that you must have logged onto your system with a password.</span></span>
-   <span data-ttu-id="31ce8-142">Sowohl der lokale als auch der Remote Computer befinden sich in derselben Domäne.</span><span class="sxs-lookup"><span data-stu-id="31ce8-142">Both your local and remote computers are within the same domain.</span></span> <span data-ttu-id="31ce8-143">Wenn Sie Domänen übergreifende Grenzen benötigen, müssen Sie zusätzliche Informationen bereitstellen oder ein etwas anderes Programmiermodell verwenden.</span><span class="sxs-lookup"><span data-stu-id="31ce8-143">If you need to cross domain boundaries, you would need to supply additional information or use a slightly different programming model.</span></span>
-   <span data-ttu-id="31ce8-144">Sie verwenden Ihr eigenes Konto, um auf den Remote Computer zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="31ce8-144">You are using your own account to access the remote machine.</span></span> <span data-ttu-id="31ce8-145">Wenn Sie versuchen, auf ein anderes Konto zuzugreifen, müssen Sie zusätzliche Anmelde Informationen angeben.</span><span class="sxs-lookup"><span data-stu-id="31ce8-145">If you were trying to access a different account, you would need to supply additional credentials.</span></span> <span data-ttu-id="31ce8-146">(Beachten Sie, dass der Versuch, lokal mit anderen Anmelde Informationen als Ihrem aktuellen Konto auf WMI zuzugreifen, nicht zulässig ist.)</span><span class="sxs-lookup"><span data-stu-id="31ce8-146">(Note that trying to access WMI locally with credentials different than your current account is not permitted.)</span></span>
-   <span data-ttu-id="31ce8-147">Auf beiden Computern wird IPv6 ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31ce8-147">Both computers are running IPv6.</span></span> <span data-ttu-id="31ce8-148">WMI unterstützt Verbindungen mit Computern, auf denen IPv6 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31ce8-148">WMI supports connections to computers running IPv6.</span></span> <span data-ttu-id="31ce8-149">Auf dem lokalen Computer und auf dem Computer \_ B muss jedoch IPv6 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="31ce8-149">However, both your local machine and "Computer\_B" must be running IPv6.</span></span> <span data-ttu-id="31ce8-150">Beide Computer können auch IPv4 ausführen.</span><span class="sxs-lookup"><span data-stu-id="31ce8-150">Either computer may be running IPv4 also.</span></span> <span data-ttu-id="31ce8-151">Weitere Informationen finden Sie [unter IPv6-und IPv4-Unterstützung in WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="31ce8-151">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>
-   <span data-ttu-id="31ce8-152">Ihr Skript muss nicht delegiert werden, d. h., es ist nicht erforderlich, über den Ziel-Remote Computer auf zusätzliche Remote Computer zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="31ce8-152">Your script does not need to delegate - that is, it does not need to access additional remote computers through the targeted remote computer.</span></span> <span data-ttu-id="31ce8-153">Weitere Informationen finden Sie unter [delegieren mit WMI](connecting-to-a-3rd-computer-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="31ce8-153">For more information, see [Delegating with WMI](connecting-to-a-3rd-computer-delegation.md).</span></span>
-   <span data-ttu-id="31ce8-154">Sie versuchen, einen bestimmten-Befehl zu erstellen, anstatt einen Remote Prozess zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="31ce8-154">You are trying to make a specific call, rather than creating a remote process.</span></span> <span data-ttu-id="31ce8-155">Weitere Informationen finden Sie unter [Erstellen von Prozessen per Remote Verbindung mithilfe von WMI](creating-processes-remotely.md).</span><span class="sxs-lookup"><span data-stu-id="31ce8-155">For more information, see [Creating Processes Remotely using WMI](creating-processes-remotely.md).</span></span>

<span data-ttu-id="31ce8-156">Mit diesen Einschränkungen ist ein WMI-Remote Rückruf sehr ähnlich wie bei einem lokalen WMI-Rückruf. der einzige Unterschied besteht darin, dass Sie den Namen des Remote Systems angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="31ce8-156">With those restrictions in mind, a remote WMI call is very similar to a local WMI call - the only difference being that you must specify the name of the remote system.</span></span> <span data-ttu-id="31ce8-157">Sie haben jedoch die Möglichkeit, viele dieser Features zu ändern, indem Sie unterschiedliche Anmelde Informationen verwenden oder den Anrufen über einen Drittanbieter Computer weiterleiten oder auf eine andere Domäne zugreifen.</span><span class="sxs-lookup"><span data-stu-id="31ce8-157">However, you may choose to change many of those features: using different credentials, or routing your call through a 3rd party computer, or accessing a different domain.</span></span>

 

 
