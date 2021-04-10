---
title: Abrufen von Daten von einem Remote Computer
description: Sie können Daten abrufen oder Ressourcen sowohl auf Remote Computern als auch auf dem lokalen Computer verwalten. Das Herstellen einer Verbindung mit einem Remote Computer in einem Windows-Remoteverwaltung Skript ähnelt dem Herstellen einer lokalen Verbindung.
ms.assetid: 578eee80-a6c1-4456-9683-14e0a3386248
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cfc95a73dab4c9a0f19481b7ba41f3c40a3862d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858266"
---
# <a name="obtaining-data-from-a-remote-computer"></a><span data-ttu-id="5ed65-104">Abrufen von Daten von einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="5ed65-104">Obtaining Data from a Remote Computer</span></span>

<span data-ttu-id="5ed65-105">Sie können Daten abrufen oder Ressourcen sowohl auf Remote Computern als auch auf dem lokalen Computer verwalten.</span><span class="sxs-lookup"><span data-stu-id="5ed65-105">You can obtain data or manage resources on remote computers as well as the local computer.</span></span> <span data-ttu-id="5ed65-106">Das Herstellen einer Verbindung mit einem Remote Computer in einem Windows-Remoteverwaltung Skript ähnelt dem Herstellen einer lokalen Verbindung.</span><span class="sxs-lookup"><span data-stu-id="5ed65-106">Connecting to a remote computer in a Windows Remote Management script is very similar to making a local connection.</span></span> <span data-ttu-id="5ed65-107">WMI-Instanzdaten sind verfügbar. wenn auf dem Remote Computer BMC-Hardware vorhanden ist, die mithilfe des WS-Management Protokolls kommunizieren kann, sind auch die Daten der [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5ed65-107">WMI instance data is available and, if the remote computer has BMC hardware that can communicate using the WS-Management protocol, then [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) data is also available.</span></span> <span data-ttu-id="5ed65-108">Weitere Informationen finden Sie unter [Windows-Remoteverwaltung und WMI](windows-remote-management-and-wmi.md) und [Remote Hardware Verwaltung](remote-hardware-management.md).</span><span class="sxs-lookup"><span data-stu-id="5ed65-108">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md) and [Remote Hardware Management](remote-hardware-management.md).</span></span>

<span data-ttu-id="5ed65-109">Möglicherweise müssen Sie ein [**ConnectionOptions**](connectionoptions.md) -Objekt erstellen, um Informationen über den Authentifizierungstyp anzugeben, der für die Anmeldung angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="5ed65-109">You may need to create a [**ConnectionOptions**](connectionoptions.md) object to specify information about the type of authentication requested for the logon.</span></span>

<span data-ttu-id="5ed65-110">Wenn das Konto auf dem Remote Computer über denselben Anmelde Namen und dasselbe Kennwort verfügt, benötigen Sie lediglich den Transport, den Domänen Namen und den Computernamen.</span><span class="sxs-lookup"><span data-stu-id="5ed65-110">If the account on the remote computer has the same logon username and password, the only extra information you need is the transport, the domain name, and the computer name.</span></span> <span data-ttu-id="5ed65-111">Aufgrund der [Benutzerkontensteuerung (User Account Control, UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista)muss das Remote Konto ein Domänen Konto und ein Mitglied der Gruppe "Remote Computer Administratoren" sein.</span><span class="sxs-lookup"><span data-stu-id="5ed65-111">Because of [User Account Control (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista), the remote account must be a domain account and a member of the remote computer Administrators group.</span></span> <span data-ttu-id="5ed65-112">Wenn das Konto Mitglied der Gruppe "Administratoren" ist, ist der Zugriff auf den WinRM-Dienst nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="5ed65-112">If the account is a local computer member of the Administrators group, then UAC does not allow access to the WinRM service.</span></span> <span data-ttu-id="5ed65-113">Für den Zugriff auf einen WinRM-Remote Dienst in einer Arbeitsgruppe muss die UAC-Filterung für lokale Konten deaktiviert werden, indem der folgende DWORD-Registrierungs Eintrag erstellt und der Wert auf 1 festgelegt wird: **\[ HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \] LocalAccountTokenFilterPolicy**.</span><span class="sxs-lookup"><span data-stu-id="5ed65-113">To access a remote WinRM service in a workgroup, UAC filtering for local accounts must be disabled by creating the following DWORD registry entry and setting its value to 1: **\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\System\] LocalAccountTokenFilterPolicy**.</span></span>

<span data-ttu-id="5ed65-114">**So stellen Sie mithilfe Ihres Anmelde namens und Kennworts eine Verbindung mit einem Remote Computer her**</span><span class="sxs-lookup"><span data-stu-id="5ed65-114">**To connect to a remote computer using your logon username and password**</span></span>

1.  <span data-ttu-id="5ed65-115">Geben Sie den Zielcomputer mit einem voll qualifizierten Domänen Namen oder einer IP-Adresse an, und weisen Sie ihn einer Konstanten zu.</span><span class="sxs-lookup"><span data-stu-id="5ed65-115">Specify the target computer with a fully qualified domain name or an IP address and assign this to a constant.</span></span> <span data-ttu-id="5ed65-116">Wenn eine IPv6-Adresse angegeben ist, muss die Adresse in eckige Klammern eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="5ed65-116">If an IPv6 address is specified, then the address must be enclosed in square brackets.</span></span>

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  <span data-ttu-id="5ed65-117">Erstellen Sie ein [**WSMAN**](wsman.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5ed65-117">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("WSMan.Automation")
    ```

    

3.  <span data-ttu-id="5ed65-118">Erstellen Sie die Sitzung, geben Sie den Transport, http oder HTTPS an, und verketten Sie Sie mit der Konstante, die den Zielcomputer darstellt.</span><span class="sxs-lookup"><span data-stu-id="5ed65-118">Create the session, specifying the transport, HTTP or HTTPS, and concatenating it with the constant representing the target computer.</span></span>

    ```VB
    
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

<span data-ttu-id="5ed65-119">Das folgende VBScript-Codebeispiel zeigt das komplette Skript.</span><span class="sxs-lookup"><span data-stu-id="5ed65-119">The following VBScript code example shows the complete script.</span></span> <span data-ttu-id="5ed65-120">Das Skript enthält eine Unterroutine zum Transformieren der Daten aus unformatierten XML-Daten in eine lesbare Form.</span><span class="sxs-lookup"><span data-stu-id="5ed65-120">The script includes a subroutine to transform the data from raw XML to human-readable form.</span></span> <span data-ttu-id="5ed65-121">Weitere Informationen finden Sie unter [Anzeigen der XML-Ausgabe von WinRM-Skripts](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="5ed65-121">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



<span data-ttu-id="5ed65-122">**So stellen Sie eine Verbindung mit einem Remote Computer mit einem anderen Konto her**</span><span class="sxs-lookup"><span data-stu-id="5ed65-122">**To connect to a remote computer using a different account**</span></span>

1.  <span data-ttu-id="5ed65-123">Geben Sie den Zielcomputer mit einem voll qualifizierten Domänen Namen oder einer IP-Adresse an, und weisen Sie ihn einer Konstanten zu.</span><span class="sxs-lookup"><span data-stu-id="5ed65-123">Specify the target computer with a fully qualified domain name or an IP address and assign this to a constant.</span></span> <span data-ttu-id="5ed65-124">Wenn eine IPv6-Adresse angegeben ist, muss die Adresse in eckige Klammern eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="5ed65-124">If an IPv6 address is specified, then the address must be enclosed in square brackets.</span></span>

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  <span data-ttu-id="5ed65-125">Erstellen Sie ein [**WSMAN**](wsman.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5ed65-125">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    
    ```

    

3.  <span data-ttu-id="5ed65-126">Rufen Sie die [**WSMAN. kreateconnectionoptions**](wsman-createconnectionoptions.md) -Methode auf, um ein [**ConnectionOptions**](connectionoptions.md) -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5ed65-126">Call the [**WSMan.CreateConnectionOptions**](wsman-createconnectionoptions.md) method to create a [**ConnectionOptions**](connectionoptions.md) object.</span></span> <span data-ttu-id="5ed65-127">Das Konto auf dem Remote Computer muss Mitglied der Gruppe "lokale Computer Administratoren" sein.</span><span class="sxs-lookup"><span data-stu-id="5ed65-127">The account on the remote computer must be a member of the local computer administrators group.</span></span>

    ```VB
    Set objConnectionOptions = objWsman.CreateConnectionOptions
    objConnectionOptions.UserName = "Username"
    objConnectionOptions.Password = "Password"
    ```

    

4.  <span data-ttu-id="5ed65-128">Geben Sie im [**WSMAN. kreatesession**](wsman-createsession.md) -Befehl die entsprechenden sitzungsverbindungsflags im *Flags* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="5ed65-128">On the [**WSman.CreateSession**](wsman-createsession.md) call, specify the appropriate session connection flags in the *flags* parameter.</span></span> <span data-ttu-id="5ed65-129">Weitere Informationen finden Sie unter [Sitzungs Konstanten](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5ed65-129">For more information, see [Session Constants](session-constants.md).</span></span> <span data-ttu-id="5ed65-130">Geben Sie den Zielcomputer mit einem voll qualifizierten Computernamen oder einer IP-Adresse und dem Transport-– http oder HTTPS an.</span><span class="sxs-lookup"><span data-stu-id="5ed65-130">Specify the target computer with a fully qualified computer name or an IP address and the transport—http or https.</span></span> <span data-ttu-id="5ed65-131">Dieses Skript fordert die [*Kerberos*](windows-remote-management-glossary.md) -Authentifizierung vom Remote-WinRM-Dienst an.</span><span class="sxs-lookup"><span data-stu-id="5ed65-131">This script requests [*Kerberos*](windows-remote-management-glossary.md) authentication from the remote WinRM service.</span></span>

    <span data-ttu-id="5ed65-132">Anders als bei WMI-Skripts können Sie verschiedene Authentifizierungsmethoden in WinRM-Skripts verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ed65-132">Unlike WMI scripts, you can use several methods of authentication in WinRM scripts.</span></span> <span data-ttu-id="5ed65-133">Weitere Informationen finden Sie unter [Authentifizierung für Remote Verbindungen](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="5ed65-133">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

    ```VB
    iFlags = objWsman.SessionFlagUseKerberos Or _
      objWsman.SessionFlagCredUserNamePassword
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
      iFlags, objConnectionOptions)
    ```

    

5.  <span data-ttu-id="5ed65-134">Nachdem das Sitzungs Objekt verfügbar ist, können Sie eine beliebige [**Sitzungs**](session.md) Objektmethode zum Abrufen von Daten für eine Ressource abrufen.</span><span class="sxs-lookup"><span data-stu-id="5ed65-134">After the session object is available, you can call any of the [**Session**](session.md) object methods to obtain data for a resource.</span></span> <span data-ttu-id="5ed65-135">Sie können Daten für alle Ressourcen erhalten, die auf dem Computer verfügbar sind, auf dem die Sitzung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5ed65-135">You can get data for any resource that is available on the computer on which the session is running.</span></span> <span data-ttu-id="5ed65-136">Weitere Informationen finden Sie unter Abrufen [von Daten vom lokalen Computer](obtaining-data-from-the-local-computer.md).</span><span class="sxs-lookup"><span data-stu-id="5ed65-136">For more information, see [Obtaining Data from the Local Computer](obtaining-data-from-the-local-computer.md).</span></span>

<span data-ttu-id="5ed65-137">Das folgende VBScript-Codebeispiel zeigt das komplette Skript.</span><span class="sxs-lookup"><span data-stu-id="5ed65-137">The following VBScript code example shows the complete script.</span></span> <span data-ttu-id="5ed65-138">Das Skript enthält eine Unterroutine zum Transformieren der Daten aus unformatierten XML-Daten in eine lesbare Form.</span><span class="sxs-lookup"><span data-stu-id="5ed65-138">The script includes a subroutine to transform the data from raw XML to human-readable form.</span></span> <span data-ttu-id="5ed65-139">Weitere Informationen finden Sie unter [Anzeigen der XML-Ausgabe von WinRM-Skripts](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="5ed65-139">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span> <span data-ttu-id="5ed65-140">Das Skript gibt die Kerberos-Authentifizierung an, aber wenn sich der Remote Computer in einer Arbeitsgruppe und nicht in einer Domäne befindet, wird bei der Angabe von Kerberos ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="5ed65-140">The script specifies Kerberos authentication, but if the remote computer is in a workgroup rather than a domain, specifying Kerberos generates an error.</span></span>


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("Wsman.Automation")
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "Username"
objConnectionOptions.Password = "Password"
iFlags = objWsman.SessionFlagUseKerberos Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
  iFlags, objConnectionOptions)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="5ed65-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5ed65-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ed65-142">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="5ed65-142">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="5ed65-143">Verwenden von Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="5ed65-143">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="5ed65-144">Windows-Remoteverwaltung Referenz</span><span class="sxs-lookup"><span data-stu-id="5ed65-144">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 