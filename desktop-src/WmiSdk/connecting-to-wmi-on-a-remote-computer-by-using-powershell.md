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
# <a name="connecting-to-wmi-remotely-with-powershell"></a><span data-ttu-id="c6a9b-103">Remote Verbindung mit WMI mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="c6a9b-103">Connecting to WMI Remotely with PowerShell</span></span>

<span data-ttu-id="c6a9b-104">Windows PowerShell bietet einen einfachen Mechanismus zum Herstellen einer Verbindung mit Windows-Verwaltungsinstrumentation (WMI) auf einem Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-104">Windows PowerShell provides a simple mechanism to connect to Windows Management Instrumentation (WMI) on a remote computer.</span></span> <span data-ttu-id="c6a9b-105">Remote Verbindungen in WMI sind von der [Windows-Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), den DCOM-Einstellungen und der [Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/aa905108(v=msdn.10))betroffen.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-105">Remote connections in WMI are affected by the [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), DCOM settings, and [User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)).</span></span> <span data-ttu-id="c6a9b-106">Weitere Informationen zum Konfigurieren von Remote Verbindungen finden Sie unter Herstellen einer Remote [Verbindung mit WMI ab Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span><span class="sxs-lookup"><span data-stu-id="c6a9b-106">For more information about configuring remote connections, see [Connecting to WMI Remotely Starting with Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

<span data-ttu-id="c6a9b-107">Die Beispiele in diesem Thema basieren darauf, dass die VBScripts [eine Verbindung mit WMI auf einem Remote Computer herstellen](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="c6a9b-107">The examples in this topic are based on the VBScripts from [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="c6a9b-108">Alle Beispiele in diesem Thema verwenden das [Get-WMIObject](/previous-versions//dd315295(v=technet.10)) -Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-108">All of the examples in this topic use the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="c6a9b-109">Weitere Informationen finden Sie unter [Get-WMIObject](/previous-versions//dd315295(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="c6a9b-109">For more information, see [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span></span>

## <a name="windows-powershell-examples"></a><span data-ttu-id="c6a9b-110">Windows PowerShell-Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6a9b-110">Windows PowerShell examples</span></span>

<span data-ttu-id="c6a9b-111">Beim Herstellen einer Verbindung mit einem Remote Computer kann ein Benutzer die Verbindungsinformationen angeben, z. b. den Remote Computernamen, die Anmelde Informationen und die Authentifizierungs Ebene für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-111">When creating a connection to a remote computer, a user can specify the connection information such as the remote computer name, credentials, and the authentication level for the connection.</span></span> <span data-ttu-id="c6a9b-112">In den folgenden Beispielen wird veranschaulicht, wie Sie eine Verbindung mit einem Remote Computer mithilfe verschiedener Sätze von Anmelde Informationen herstellen und wie Sie auf WMI-Informationen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-112">The following examples illustrate how to connect to a remote computer by using different sets of credentials and how to access WMI information.</span></span>

<span data-ttu-id="c6a9b-113">Das folgende Windows PowerShell-Beispiel zeigt das Festlegen der Identitätswechsel Ebene:</span><span class="sxs-lookup"><span data-stu-id="c6a9b-113">The following Windows PowerShell example shows setting the impersonation level:</span></span>


```PowerShell

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -ComputerName Computer_B
```



<span data-ttu-id="c6a9b-114">Im vorherigen Beispiel stellt der Benutzer mit denselben Anmelde Informationen (Domäne und Benutzername), mit denen Sie sich angemeldet haben, eine Verbindung mit einem Remote Computer her.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-114">In the preceding example, the user connects to a remote computer by using the same credentials (domain and user name) that they logged on with.</span></span> <span data-ttu-id="c6a9b-115">Der Benutzer hat auch angefordert, den Identitätswechsel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-115">The user also requested to use impersonation.</span></span> <span data-ttu-id="c6a9b-116">Im Gegensatz zum ursprünglichen VBScript-Beispiel wird eine Monikerzeichenfolge nicht benötigt, da die Identitätswechsel Ebene von der Eigenschaft "Identitätswechsel" festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-116">Unlike the original VBScript example, a moniker string is not needed because the impersonation level is set by the "Impersonation" property.</span></span> <span data-ttu-id="c6a9b-117">Standardmäßig ist die Ebene des Identitäts Wechsels auf 3 (Identität annehmen) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-117">By default, the impersonation level is set to 3 (Impersonate).</span></span>

<span data-ttu-id="c6a9b-118">Im Beispiel werden alle Instanzen der Win32- [**\_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse aufgelistet, die auf dem Remote Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-118">The example lists all the instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class that are running on remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="c6a9b-119">Geben Sie den WMI-Namespace an, mit dem auf dem Remote Computer eine Verbindung hergestellt werden soll, da der Standard Namespace auf unterschiedlichen Computern möglicherweise nicht identisch ist.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-119">You should specify the WMI namespace to connect to on the remote computer because it is possible that the default namespace is not the same on different computers.</span></span>

 

<span data-ttu-id="c6a9b-120">Das folgende Windows PowerShell-Beispiel zeigt, wie Sie eine Verbindung mit einem Remote Computer mit unterschiedlichen Anmelde Informationen herstellen und die Identitätswechsel Ebene auf 3 festlegen, dessen Identität angenommen wird:</span><span class="sxs-lookup"><span data-stu-id="c6a9b-120">The following Windows PowerShell example shows how to connect to a remote computer with different credentials and to set the impersonation level to 3, which is Impersonate:</span></span>


```PowerShell

$Computer = "atl-dc-01"

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -Credential `
FABRIKAM\administrator -ComputerName $Computer
```



<span data-ttu-id="c6a9b-121">Im vorherigen Beispiel wurde der Computername der $Computer Variablen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-121">In the preceding example, the computer name was assigned to the $Computer variable.</span></span> <span data-ttu-id="c6a9b-122">Der Benutzer stellt eine Verbindung mit einem Remote Computer mithilfe spezifischer Anmelde Informationen (Domäne und Benutzername) her und fordert Identitätswechsel für die Authentifizierungs Ebene an.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-122">The user connects to a remote computer by using specific credentials (domain and user name) and requests impersonation for the authentication level.</span></span>

> [!Note]  
> <span data-ttu-id="c6a9b-123">Das Zeichen mit einem Doppel Akzent ( \` ) wird verwendet, um einen Zeilenumbruch anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-123">The grave-accent character (\`) is used to indicate a line break.</span></span> <span data-ttu-id="c6a9b-124">Dies entspricht dem Unterstrich Zeichen ( \_ ) in VBScript.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-124">It is equivalent to the underscore character (\_) in VBScript.</span></span>

 

<span data-ttu-id="c6a9b-125">Im folgenden Windows PowerShell-Beispiel wird eine Verbindung mit einer Gruppe von Remote Computern in derselben Domäne hergestellt, indem ein Array von Remote Computernamen erstellt und dann die Namen der Plug & Play Geräte – Instanzen von [**Win32 \_ pnptity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)– auf den einzelnen Computern angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="c6a9b-125">The following Windows PowerShell example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of [**Win32\_PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)—on each computer:</span></span>


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
> <span data-ttu-id="c6a9b-126">Um das vorangehende Windows PowerShell-Skript auszuführen, müssen Sie Administrator auf den Remote Computern sein.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-126">To run the preceding Windows PowerShell script, you must be an administrator on the remote computers.</span></span> <span data-ttu-id="c6a9b-127">Beachten Sie außerdem Folgendes im Zusammenhang mit dem vorherigen Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c6a9b-127">Also, relating to the preceding example, note the following:</span></span>

 

-   <span data-ttu-id="c6a9b-128">Die Computernamen im Array müssen in Anführungszeichen eingeschlossen werden, da Sie Zeichen folgen sind.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-128">The computer names in the array must be enclosed in quotation marks because they are strings.</span></span>
-   <span data-ttu-id="c6a9b-129">Die vom [Get-WMIObject](/previous-versions//dd315295(v=technet.10)) zurückgegebenen Objekte werden der $ColItems Variablen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-129">The objects returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) are assigned to the $ColItems variable.</span></span>
-   <span data-ttu-id="c6a9b-130">Der Bereichs Operator \[ \] beschränkte die Liste der Plug & Play Geräte auf 48 Instanzen.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-130">The range operator \[\] limited the list of Plug and Play devices to 48 instances.</span></span> <span data-ttu-id="c6a9b-131">Weitere Informationen finden Sie unter Informationen [zu \_ Operatoren](/previous-versions//dd347588(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="c6a9b-131">For more information, see [About\_Operators](/previous-versions//dd347588(v=technet.10)).</span></span>
-   <span data-ttu-id="c6a9b-132">" \| " Ist das Pipeline Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-132">The "\|" is the pipeline character.</span></span> <span data-ttu-id="c6a9b-133">Das von "colItems" zurückgegebene Objekt wird an das Cmdlet " [Format-List]( /previous-versions//dd347700(v=technet.10)) " gesendet.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-133">The object returned by ColItems is sent to the [Format-List]( /previous-versions//dd347700(v=technet.10)) cmdlet.</span></span>

<span data-ttu-id="c6a9b-134">Das folgende Windows PowerShell-Beispiel ermöglicht es Ihnen, eine Verbindung mit einem Remote Computer in einer anderen Domäne herzustellen.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-134">The following Windows PowerShell example enables you to connect to a remote computer on a different domain.</span></span> <span data-ttu-id="c6a9b-135">In diesem Beispiel werden auch die Prozessnamen für Instanzen des [**Win32- \_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process) auf dem Remote Computer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-135">This example also displays the process names for instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) on the remote computer.</span></span>


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
> <span data-ttu-id="c6a9b-136">Um das vorangehende Windows PowerShell-Skript auszuführen, müssen Sie Administrator auf dem Remote Computer sein.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-136">To run the preceding Windows PowerShell script, you must be an administrator on the remote computer.</span></span>

 

<span data-ttu-id="c6a9b-137">Im vorherigen Beispiel stellt der Benutzer eine Verbindung mit einem Remote Computer in einer anderen Domäne her und gibt ein bevorzugtes Gebiets Schema an.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-137">In the preceding example, the user connects to a remote computer on a different domain and specifies a preferred locale.</span></span> <span data-ttu-id="c6a9b-138">Der [Get-Credential](/previous-versions//dd315327(v=technet.10)) -Befehl fordert die Anmelde Informationen des Benutzers an und weist die Anmelde Informationen einem Objekt zu.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-138">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) command requests the user's credentials and assigns the credentials to an object.</span></span> <span data-ttu-id="c6a9b-139">Im Beispiel werden auch die Namen von Instanzen der [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse aufgelistet, die auf dem Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c6a9b-139">The example also lists the names of instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class that are running on the computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6a9b-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c6a9b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6a9b-141">Herstellen einer Verbindung mit WMI auf einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="c6a9b-141">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
