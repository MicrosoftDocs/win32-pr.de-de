---
description: Sie können eine Remote Verbindung mit WMI mit VBScript herstellen, indem Sie ein Verbindungs Objekt erstellen. Dieses Objekt enthält den Namen des Computers, den WMI-Namespace, mit dem Sie eine Verbindung herstellen möchten, sowie alle relevanten Anmelde Informationen und Authentifizierungs Ebenen.
ms.assetid: b2ad262b-148d-47cc-8be7-6df99245aa7f
ms.tgt_platform: multiple
title: Remote Verbindung mit WMI mit VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07cff2f0cd0ca06de059d9b39e36d715b5555eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345276"
---
# <a name="connecting-to-wmi-remotely-with-vbscript"></a><span data-ttu-id="7b2c8-104">Remote Verbindung mit WMI mit VBScript</span><span class="sxs-lookup"><span data-stu-id="7b2c8-104">Connecting to WMI Remotely with VBScript</span></span>

<span data-ttu-id="7b2c8-105">Sie können eine Remote Verbindung mit WMI mit VBScript herstellen, indem Sie ein Verbindungs Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-105">You can create a remote connection to WMI with VBScript by creating a connection object.</span></span> <span data-ttu-id="7b2c8-106">Dieses Objekt enthält den Namen des Computers, den WMI-Namespace, mit dem Sie eine Verbindung herstellen möchten, sowie alle relevanten Anmelde Informationen und Authentifizierungs Ebenen.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-106">This object contains the name of the computer, the WMI namespace you want to connect to, as well as any relevant credentials and authentication levels.</span></span>

<span data-ttu-id="7b2c8-107">**So stellen Sie eine Verbindung mit einem Remote System mithilfe von VBScript her**</span><span class="sxs-lookup"><span data-stu-id="7b2c8-107">**To connect to a remote system using VBScript**</span></span>

1.  <span data-ttu-id="7b2c8-108">Geben Sie die Verbindungsinformationen an, z. b. den Remote Computernamen, die Anmelde Informationen und die Authentifizierungs Ebene für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-108">Specify the connection information such as the remote computer name, credentials, and the authentication level for the connection.</span></span>

    <span data-ttu-id="7b2c8-109">Wenn Sie mit den gleichen Anmelde Informationen (Domäne und Benutzername), mit denen Sie angemeldet sind, eine Verbindung mit einem Remote Computer herstellen, können Sie die Verbindungsinformationen in einem [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)-[Moniker](constructing-a-moniker-string.md)angeben, wie im folgenden Codebeispiel beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-109">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you can specify the connection information in a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)[moniker](constructing-a-moniker-string.md), as described in the following code sample.</span></span>

    ```VB
    strComputer = "Computer_B"
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & "\Root\CIMv2")
    ```

    

    <span data-ttu-id="7b2c8-110">Im Allgemeinen sollten Sie den WMI-Namespace angeben, mit dem auf dem Remote Computer eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-110">Generally speaking, you should specify the WMI namespace to connect to on the remote computer.</span></span> <span data-ttu-id="7b2c8-111">Dies liegt daran, dass es möglich ist, dass der Standard Namespace auf unterschiedlichen Computern nicht identisch ist.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-111">This is because it is possible that the default namespace is not the same on different computers.</span></span> <span data-ttu-id="7b2c8-112">Durch die Angabe des Namespace wird sichergestellt, dass Sie eine Verbindung mit dem gleichen Namespace auf allen Computern herstellen.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-112">Specifying the namespace ensures that you connect to the same namespace on all computers.</span></span>

    <span data-ttu-id="7b2c8-113">Weitere Informationen zu VBScript-Konstanten und Skript Zeichenfolgen für die Verwendung der monikerverbindung finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="7b2c8-113">For more information on VBScript constants and scripting strings for using the moniker connection, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

2.  <span data-ttu-id="7b2c8-114">Wenn Sie eine Verbindung mit einem Remote Computer in einer anderen Domäne herstellen oder einen anderen Benutzernamen und ein anderes Kennwort verwenden, müssen Sie die Methode " [**Swap. ConnectServer**](swbemlocator-connectserver.md) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-114">If you connect to a remote computer in a different domain or using a different user name and password, then you must use the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

    <span data-ttu-id="7b2c8-115">Wie bei einem Moniker verwenden Sie **ConnectServer** , um die Anmelde Informationen, die Authentifizierungs Ebene und den Namespace für die Remote Verbindung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-115">As with a moniker, you use **ConnectServer** to specify the credentials, authentication level, and namespace for the remote connection.</span></span> <span data-ttu-id="7b2c8-116">Im folgenden Codebeispiel wird die Verwendung von ConnectServer für den Zugriff auf einen Remote Computer mithilfe eines Administrator Kontos und Kennworts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-116">The following code sample describes using ConnectServer to access a remote computer using an administrator account and password.</span></span>

    ```VB
    strComputer = "Computer_B"
    Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                         "Root\CIMv2", _
                                                         "fabrikam\administrator", _
                                                         "password")
    ```

    

3.  <span data-ttu-id="7b2c8-117">Wenn Sie die [**ConnectServer**](swbemlocator-connectserver.md) -Funktion für Remote Verbindungen verwenden, legen Sie Identitätswechsel und Authentifizierung für das Sicherheits Objekt fest, das durch einen aufrufswert von " [**Swap Services. Security**](swbemservices-security-.md)" abgerufen wird</span><span class="sxs-lookup"><span data-stu-id="7b2c8-117">When using the [**ConnectServer**](swbemlocator-connectserver.md) function for remote connections, set impersonation and authentication on the security object obtained by a call to [**SWbemServices.Security**](swbemservices-security-.md).</span></span> <span data-ttu-id="7b2c8-118">Sie können die Enumeration [wbemimpersonationlevelenum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) zum Angeben der Identitätswechsel Ebene verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-118">You can use the enumeration [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) to specify impersonation level.</span></span>

    <span data-ttu-id="7b2c8-119">Im folgenden Codebeispiel wird die Identitätswechsel Ebene für das vorherige VBScript-Codebeispiel festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-119">The following code sample sets the impersonation level for the previous VBScript code sample.</span></span>

    ```VB
    objSWbemServices.Security_.ImpersonationLevel = 3
    ```

    

    <span data-ttu-id="7b2c8-120">Beachten Sie, dass einige Verbindungen eine bestimmte Authentifizierungs Ebene erfordern.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-120">Note that some connections require a specific authentication level.</span></span> <span data-ttu-id="7b2c8-121">Weitere Informationen finden Sie unter [Festlegen der Prozesssicherheit für Client Anwendungen](setting-client-application-process-security.md) und [Sichern von Skript Clients](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="7b2c8-121">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md) and [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

    <span data-ttu-id="7b2c8-122">Insbesondere sollten Sie die Authentifizierungs Ebene auf **RPC \_ C \_ authn \_ Level \_ Pkt \_ Privacy** oder 6 festlegen, wenn der Namespace, für den Sie eine Verbindung mit dem Remote Computer herstellen, eine verschlüsselte Verbindung erfordert, bevor Daten zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-122">In particular, you should set the authentication level to **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** or 6 if the namespace to which you are connecting on the remote computer requires an encrypted connection before it will return data.</span></span> <span data-ttu-id="7b2c8-123">Sie können diese Authentifizierungs Ebene auch dann verwenden, wenn Sie vom Namespace nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-123">You can also use this authentication level, even if the namespace does not require it.</span></span> <span data-ttu-id="7b2c8-124">Dadurch wird sichergestellt, dass die Daten beim Überschreiten des Netzwerks verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-124">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="7b2c8-125">Wenn Sie versuchen, eine niedrigere Authentifizierungs Ebene festzulegen, als zulässig ist, wird die Meldung "Zugriff verweigert" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-125">If you attempt to set a lower authentication level than is allowed, an access denied message will be returned.</span></span> <span data-ttu-id="7b2c8-126">Weitere Informationen finden Sie unter [erfordern einer verschlüsselten Verbindung mit einem Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="7b2c8-126">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="7b2c8-127">Nachdem Sie die Verbindung hergestellt haben, können Sie weiterhin auf WMI-Daten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-127">Once you have made your connection, you can continue to access WMI data.</span></span> <span data-ttu-id="7b2c8-128">Weitere Informationen finden Sie unter [WMI-Tasks für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md).</span><span class="sxs-lookup"><span data-stu-id="7b2c8-128">For more information, see [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7b2c8-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b2c8-129">Examples</span></span>

<span data-ttu-id="7b2c8-130">Ein umfangreicheres VBScript-Beispiel finden Sie im Abschnitt "Beispiele" auf der Referenzseite zu " [**mpbemlocator. ConnectServer**](swbemlocator-connectserver.md) ".</span><span class="sxs-lookup"><span data-stu-id="7b2c8-130">For a larger VBScript sample, see the Examples section in the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) reference page.</span></span>

<span data-ttu-id="7b2c8-131">Im folgenden VBScript-Codebeispiel wird eine Verbindung mit einer Gruppe von Remote Computern in derselben Domäne hergestellt, indem ein Array von Remote Computernamen erstellt und dann die Namen der Plug & Play Geräte – Instanzen von [**Win32 \_ pnptity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)– auf den einzelnen Computern angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-131">The following VBScript code example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of [**Win32\_PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)—on each computer.</span></span> <span data-ttu-id="7b2c8-132">Zum Ausführen des folgenden Skripts müssen Sie Administrator auf den Remote Computern sein.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-132">To run the script below, you must be an administrator on the remote computers.</span></span> <span data-ttu-id="7b2c8-133">Beachten Sie, dass \\ \\ vor dem Hinzufügen des Remote Computer namens durch das Skript nach der Einstellung der Identitätswechsel Ebene "" erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-133">Note that the "\\\\" required before the remote computer name is added by the script following the impersonation level setting.</span></span> <span data-ttu-id="7b2c8-134">Weitere Informationen zu WMI-Pfaden finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="7b2c8-134">For more information about WMI paths, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" & strComputer& "\Root\CIMv2") 
    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



<span data-ttu-id="7b2c8-135">Mithilfe des folgenden VBScript-Code Beispiels können Sie eine Verbindung mit einem Remote Computer mithilfe verschiedener Anmelde Informationen herstellen.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-135">The following VBScript code example enables you to connect to a remote computer using different credentials.</span></span> <span data-ttu-id="7b2c8-136">Beispielsweise ein Remote Computer in einer anderen Domäne oder eine Verbindung mit einem Remote Computer, der einen anderen Benutzernamen und ein anderes Kennwort benötigt.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-136">For example, a remote computer in a different domain or connecting to a remote computer requiring a different user name and password.</span></span> <span data-ttu-id="7b2c8-137">Verwenden Sie in diesem Fall die Verbindung " [**Swap Services. ConnectServer**](swbemlocator-connectserver.md) ".</span><span class="sxs-lookup"><span data-stu-id="7b2c8-137">In this case, use the [**SWbemServices.ConnectServer**](swbemlocator-connectserver.md) connection.</span></span>


```VB
' Full Computer Name
' can be found by right-clicking My Computer,
' then click Properties, then click the Computer Name tab)
' or use the computer's IP address
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```



## <a name="related-topics"></a><span data-ttu-id="7b2c8-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7b2c8-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b2c8-139">Herstellen einer Verbindung mit WMI auf einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="7b2c8-139">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
