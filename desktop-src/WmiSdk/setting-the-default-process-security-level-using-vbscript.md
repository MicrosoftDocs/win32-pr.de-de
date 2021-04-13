---
title: Festlegen der Standardprozess-Sicherheitsstufe mit VBScript
description: Ein Skript kann die Standardeinstellungen für die WMI-Authentifizierung und den Identitätswechsel verwenden. Für das Skript ist jedoch möglicherweise eine Verbindung mit mehr Sicherheit erforderlich, oder es kann eine Verbindung mit einem Namespace hergestellt werden, der eine verschlüsselte Verbindung erfordert.
ms.assetid: cb477224-3117-45e4-9271-613b58e48b6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03fe69228021fe8d3f36f03e60cb2366b6132f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218312"
---
# <a name="set-the-default-process-security-level-with-vbscript"></a><span data-ttu-id="7c2ab-104">Festlegen der Standardprozess-Sicherheitsstufe mit VBScript</span><span class="sxs-lookup"><span data-stu-id="7c2ab-104">Set the default process security level with VBScript</span></span>

<span data-ttu-id="7c2ab-105">Ein Skript kann die Standardeinstellungen für die WMI-Authentifizierung und den Identitätswechsel verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-105">A script can use the default WMI authentication and impersonation settings.</span></span> <span data-ttu-id="7c2ab-106">Für das Skript ist jedoch möglicherweise eine Verbindung mit mehr Sicherheit erforderlich, oder es kann eine Verbindung mit einem Namespace hergestellt werden, der eine verschlüsselte Verbindung erfordert.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-106">However, the script may need a connection with more security or may connect to a namespace that requires an encrypted connection.</span></span> <span data-ttu-id="7c2ab-107">Weitere Informationen finden Sie unter [Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md) und [erfordern einer verschlüsselten Verbindung mit einem Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="7c2ab-107">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md) and [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="7c2ab-108">Im einfachsten Fall kann ein Skript die Standardeinstellungen für die Authentifizierung und den Identitätswechsel verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-108">In the simplest case, a script can use the default authentication and impersonation settings.</span></span> <span data-ttu-id="7c2ab-109">WMI wird normalerweise auf einem gemeinsamen Dienst Host ausgeführt und verwendet dieselbe Authentifizierung wie andere Prozesse auf dem Host.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-109">WMI normally runs in a shared service host and shares the same authentication as other processes in the host.</span></span> <span data-ttu-id="7c2ab-110">Wenn Sie den WMI-Prozess mit einer anderen Authentifizierungs Stufe ausführen möchten, führen Sie WMI mit dem [**WinMgmt**](winmgmt.md) -Befehl mit dem Schalter **/standalonehost** aus, und legen Sie die Authentifizierungs Ebene für WMI in der Regel fest.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-110">If you want to run the WMI process with a different level of authentication, run WMI with the [**winmgmt**](winmgmt.md) command with the **/standalonehost** switch and set the authentication level for WMI generally.</span></span> <span data-ttu-id="7c2ab-111">Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="7c2ab-111">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

<span data-ttu-id="7c2ab-112">Das folgende Skript verwendet die Standardeinstellungen für Identitätswechsel-und Authentifizierungs Ebenen.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-112">The following script uses default settings for impersonation and authentication levels.</span></span>


```VB
strComputer = "." 
Set objServices = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="7c2ab-113">Sie können auch einen [Moniker](constructing-a-moniker-string.md) in einem Aufruf von [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)verwenden und die Standard Sicherheitseinstellungen festlegen, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-113">You can also use a [moniker](constructing-a-moniker-string.md) in a call to [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx), and set the default security settings, as in the following example.</span></span>


```VB
strComputer = "." 
Set objServices = GetObject( _
    "winmgmts:{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!root/cimv2")
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="7c2ab-114">Weitere Informationen zum Festlegen von unterschiedlichen Identitätswechsel-oder Authentifizierungs Ebenen in einem Skript oder zum Festlegen der Standardwerte für einen Computer finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="7c2ab-114">For more information about setting different impersonation or authentication levels in a script, or for setting the default values for a computer, see the following topics:</span></span>

-   [<span data-ttu-id="7c2ab-115">Ändern der Standard Anmelde Informationen für die Authentifizierung mithilfe von VBScript</span><span class="sxs-lookup"><span data-stu-id="7c2ab-115">Changing the Default Authentication Credentials Using VBScript</span></span>](#changing-the-default-authentication-credentials-using-vbscript)
-   [<span data-ttu-id="7c2ab-116">Ändern der Standardeinstellungen für Identitätswechsel mithilfe von VBScript</span><span class="sxs-lookup"><span data-stu-id="7c2ab-116">Changing the Default Impersonation Settings Using VBScript</span></span>](#changing-the-default-impersonation-levels-using-vbscript)
-   [<span data-ttu-id="7c2ab-117">Festlegen der Standard Identitätswechsel Ebene mithilfe der Registrierung</span><span class="sxs-lookup"><span data-stu-id="7c2ab-117">Setting the Default Impersonation Level Using the Registry</span></span>](#setting-the-default-impersonation-level-using-the-registry)
-   [<span data-ttu-id="7c2ab-118">Zugreifen auf das "Swap Security"-Objekt in VBScript</span><span class="sxs-lookup"><span data-stu-id="7c2ab-118">Accessing the SWbemSecurity Object in VBScript</span></span>](#accessing-the-swbemsecurity-object-in-vbscript)
-   [<span data-ttu-id="7c2ab-119">**Austausch Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="7c2ab-119">**SWbemSecurity**</span></span>](swbemsecurity.md)

## <a name="changing-the-default-authentication-credentials-using-vbscript"></a><span data-ttu-id="7c2ab-120">Ändern der Standard Anmelde Informationen für die Authentifizierung mithilfe von VBScript</span><span class="sxs-lookup"><span data-stu-id="7c2ab-120">Changing the Default Authentication Credentials Using VBScript</span></span>

<span data-ttu-id="7c2ab-121">Sie können die Authentifizierungs Ebene in einem Skript mithilfe der [Monikerzeichenfolge](constructing-a-moniker-string.md) und der Objekte " [**Swap-Locator**](swbemlocator.md) " und " [**taubemsecurity**](swbemsecurity.md) " ändern.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-121">You can change the authentication level in a script using a [moniker](constructing-a-moniker-string.md) string, and the [**SWbemLocator**](swbemlocator.md) and [**SWbemSecurity**](swbemsecurity.md) objects.</span></span>

<span data-ttu-id="7c2ab-122">Die Authentifizierungs Ebene muss entsprechend den Anforderungen des Ziel Betriebssystems festgelegt werden, mit dem Sie eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-122">The authentication level must be set according to the requirements of the target operating system to which you are connecting.</span></span> <span data-ttu-id="7c2ab-123">Weitere Informationen finden Sie unter [Herstellen einer Verbindung zwischen verschiedenen Betriebssystemen](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span><span class="sxs-lookup"><span data-stu-id="7c2ab-123">For more information, see [Connecting Between Different Operating Systems](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span></span>

<span data-ttu-id="7c2ab-124">Im folgenden VBScript-Codebeispiel wird gezeigt, wie die Authentifizierungs Ebene in einem Skript geändert wird, das die Daten des freien Speicherplatzes von einem Remote Computer mit dem Namen "Server1" abruft.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-124">The following VBScript code example shows how to change the authentication level in a script that obtains the free space data from a remote computer named "Server1".</span></span>


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{authenticationLevel=Pkt}!\\" _
    & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
    Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
        "FreeSpace: " & vbTab & objDisk.FreeSpace 
    NextstrComputer = "." 
    Set objServices = GetObject( "winmgmts:{impersonationLevel=impersonate," _
                               & "authenticationLevel=pktPrivacy}!root/cimv2")
    Set objProcessSet = objServices.ExecQuery("SELECT Name FROM Win32_Process",,48)
    For Each Process in objProcessSet
        WScript.Echo Process.Name
    Next
Next
```



<span data-ttu-id="7c2ab-125">Verwenden Sie in Skript-monikerverbindungen mit WMI den Kurznamen, der in der Spalte "monikerName/Beschreibung" der Tabelle unten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-125">In script moniker connections to WMI, use the short name shown in the "Moniker name/description" column of the table below.</span></span> <span data-ttu-id="7c2ab-126">Im folgenden Skript wird die Authentifizierungs Ebene beispielsweise auf **wbemauthenticationlevelpktintegrity** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-126">For example, in the following script, the authentication level is set to **WbemAuthenticationLevelPktIntegrity**.</span></span>


```VB
SetobjWMIService = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!root\cimv2")
```



<span data-ttu-id="7c2ab-127">In der folgenden Tabelle sind die Authentifizierungs Ebenen aufgelistet, die Sie festlegen können.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-127">The following table lists the authentication levels you can set.</span></span> <span data-ttu-id="7c2ab-128">Diese Ebenen werden in wbemdisp. tlb in der Enumeration [wbemauthenticationlevelenumeration](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)definiert.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-128">These levels are defined in Wbemdisp.tlb in the enumeration [WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span>



| <span data-ttu-id="7c2ab-129">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="7c2ab-129">Name/value</span></span>                                                      | <span data-ttu-id="7c2ab-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c2ab-130">Description</span></span>                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c2ab-131">**Wbemauthenticationleveldefault**</span><span class="sxs-lookup"><span data-stu-id="7c2ab-131">**WbemAuthenticationLevelDefault**</span></span><br/> <span data-ttu-id="7c2ab-132">0</span><span class="sxs-lookup"><span data-stu-id="7c2ab-132">0</span></span><br/>      | <span data-ttu-id="7c2ab-133">Moniker: Standard</span><span class="sxs-lookup"><span data-stu-id="7c2ab-133">Moniker: Default</span></span><br/> <span data-ttu-id="7c2ab-134">WMI verwendet die Standardeinstellung für die Windows-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-134">WMI uses the default Windows authentication setting.</span></span> <span data-ttu-id="7c2ab-135">Dies ist die empfohlene Einstellung, die es WMI ermöglicht, bis zu dem vom Server benötigten Wert auszuhandeln, der Daten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-135">This is the recommended setting that allows WMI to negotiate to the level required by the server returning data.</span></span> <span data-ttu-id="7c2ab-136">Wenn für den Namespace jedoch eine Verschlüsselung erforderlich ist, verwenden Sie **wbemauthenticationlevelpktprivacy**.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-136">However, if the namespace requires encryption, use **WbemAuthenticationLevelPktPrivacy**.</span></span><br/> |
| <span data-ttu-id="7c2ab-137">**Wbemauthenticationlevelnone**</span><span class="sxs-lookup"><span data-stu-id="7c2ab-137">**WbemAuthenticationLevelNone**</span></span><br/> <span data-ttu-id="7c2ab-138">1</span><span class="sxs-lookup"><span data-stu-id="7c2ab-138">1</span></span><br/>         | <span data-ttu-id="7c2ab-139">Moniker: keine</span><span class="sxs-lookup"><span data-stu-id="7c2ab-139">Moniker: None</span></span><br/> <span data-ttu-id="7c2ab-140">Verwendet keine Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-140">Uses no authentication.</span></span><br/>                                                                                                                                                                                                                                            |
| <span data-ttu-id="7c2ab-141">**Wbemauthenticationlevelconnect**</span><span class="sxs-lookup"><span data-stu-id="7c2ab-141">**WbemAuthenticationLevelConnect**</span></span><br/> <span data-ttu-id="7c2ab-142">2</span><span class="sxs-lookup"><span data-stu-id="7c2ab-142">2</span></span><br/>      | <span data-ttu-id="7c2ab-143">Moniker: verbinden</span><span class="sxs-lookup"><span data-stu-id="7c2ab-143">Moniker: Connect</span></span><br/> <span data-ttu-id="7c2ab-144">Authentifiziert die Anmelde Informationen des Clients nur, wenn der Client eine Beziehung mit dem Server herstellt.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-144">Authenticates the credentials of the client only when the client establishes a relationship with the server.</span></span><br/>                                                                                                                                                    |
| <span data-ttu-id="7c2ab-145">**Wbemauthenticationlevelcall**</span><span class="sxs-lookup"><span data-stu-id="7c2ab-145">**WbemAuthenticationLevelCall**</span></span><br/> <span data-ttu-id="7c2ab-146">3</span><span class="sxs-lookup"><span data-stu-id="7c2ab-146">3</span></span><br/>         | <span data-ttu-id="7c2ab-147">Aufruf</span><span class="sxs-lookup"><span data-stu-id="7c2ab-147">Call</span></span><br/> <span data-ttu-id="7c2ab-148">Authentifiziert sich nur zu Beginn jedes Aufrufes, wenn der Server die Anforderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-148">Authenticates only at the beginning of each call when the server receives the request.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="7c2ab-149">**Wbemauthenticationlevelpkt**</span><span class="sxs-lookup"><span data-stu-id="7c2ab-149">**WbemAuthenticationLevelPkt**</span></span><br/> <span data-ttu-id="7c2ab-150">4</span><span class="sxs-lookup"><span data-stu-id="7c2ab-150">4</span></span><br/>          | <span data-ttu-id="7c2ab-151">Moniker: Pkt</span><span class="sxs-lookup"><span data-stu-id="7c2ab-151">Moniker: Pkt</span></span><br/> <span data-ttu-id="7c2ab-152">Authentifiziert, dass alle empfangenen Daten vom erwarteten Client stammen.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-152">Authenticates that all data received is from the expected client.</span></span><br/>                                                                                                                                                                                                   |
| <span data-ttu-id="7c2ab-153">**Wbemauthenticationlevelpktintegrity**</span><span class="sxs-lookup"><span data-stu-id="7c2ab-153">**WbemAuthenticationLevelPktIntegrity**</span></span><br/> <span data-ttu-id="7c2ab-154">5</span><span class="sxs-lookup"><span data-stu-id="7c2ab-154">5</span></span><br/> | <span data-ttu-id="7c2ab-155">Moniker: PktIntegrity</span><span class="sxs-lookup"><span data-stu-id="7c2ab-155">Moniker: PktIntegrity</span></span><br/> <span data-ttu-id="7c2ab-156">Authentifiziert und überprüft, ob keine der zwischen Client und Server übertragenen Daten geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-156">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="7c2ab-157">**Wbemauthenticationlevelpktprivacy**</span><span class="sxs-lookup"><span data-stu-id="7c2ab-157">**WbemAuthenticationLevelPktPrivacy**</span></span><br/> <span data-ttu-id="7c2ab-158">6</span><span class="sxs-lookup"><span data-stu-id="7c2ab-158">6</span></span><br/>   | <span data-ttu-id="7c2ab-159">Moniker: PKTPRIVACY</span><span class="sxs-lookup"><span data-stu-id="7c2ab-159">Moniker: PktPrivacy</span></span><br/> <span data-ttu-id="7c2ab-160">Authentifiziert alle vorherigen Identitätswechsel Ebenen und verschlüsselt den Argument Wert jedes Remote Prozedur Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-160">Authenticates all previous impersonation levels and encrypts the argument value of each remote procedure call.</span></span> <span data-ttu-id="7c2ab-161">Verwenden Sie diese Einstellung, wenn der Namespace, für den Sie eine Verbindung herstellen möchten, eine verschlüsselte Verbindung erfordert.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-161">Use this setting if the namespace to which you are connecting requires an encrypted connection.</span></span><br/>                                               |



 

<span data-ttu-id="7c2ab-162">Um einen erfolgreichen-Rückruf zu ermitteln, überprüfen Sie den Rückgabewert, nachdem Sie die Authentifizierungs Ebene geändert haben.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-162">To determine a successful call, check the return value after you change the authentication level.</span></span>

<span data-ttu-id="7c2ab-163">Da z. b. lokale Verbindungen immer die Authentifizierungs Ebene **wbemauthenticationlevelpktprivacy** aufweisen, kann im folgenden Beispiel die Authentifizierungs Ebene nicht festgelegt werden, da Sie mit dem lokalen Computer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-163">For example, because local connections always have an authentication level of **wbemAuthenticationLevelPktPrivacy**, the following example fails to set the authentication level because it connects to the local computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!" _
    & "\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="7c2ab-164">Ein Anbieter kann die Sicherheit für einen Namespace so festlegen, dass keine Daten zurückgegeben werden, es sei denn, Sie verwenden den Paket Datenschutz (PKTPRIVACY) in der Verbindung mit diesem Namespace.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-164">A provider can set the security on a namespace so that no data is returned unless you use packet privacy (PktPrivacy) in your connection to that namespace.</span></span> <span data-ttu-id="7c2ab-165">Dadurch wird sichergestellt, dass die Daten beim Überschreiten des Netzwerks verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-165">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="7c2ab-166">Wenn Sie versuchen, eine niedrigere Authentifizierungs Ebene festzulegen, erhalten Sie die Meldung "Zugriff verweigert".</span><span class="sxs-lookup"><span data-stu-id="7c2ab-166">If you try to set a lower authentication level, you will get an access denied message.</span></span> <span data-ttu-id="7c2ab-167">Weitere Informationen finden Sie unter [Sichern von WMI-Namespaces](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="7c2ab-167">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="changing-the-default-impersonation-levels-using-vbscript"></a><span data-ttu-id="7c2ab-168">Ändern der Standard Identitätswechsel Ebenen mithilfe von VBScript</span><span class="sxs-lookup"><span data-stu-id="7c2ab-168">Changing the Default Impersonation Levels Using VBScript</span></span>

<span data-ttu-id="7c2ab-169">Wenn Sie Aufrufe der Skript-API für WMI ausführen, wird empfohlen, die Standardeinstellungen zu verwenden, die WMI für die Identitätswechsel Ebene bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-169">When you make calls to the Scripting API for WMI, it is recommended that you use the defaults that WMI provides for the impersonation level.</span></span> <span data-ttu-id="7c2ab-170">Remote Anrufe und einige Anbieter mit mehr als einem Netzwerkhop erfordern eine höhere Identitätswechsel Ebene als WMI verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-170">Remote calls and some providers with more than one network hop require a higher impersonation level than WMI uses.</span></span> <span data-ttu-id="7c2ab-171">Wenn die Identitätswechsel Ebene nicht ausreicht, kann ein Anbieter eine Anforderung ablehnen oder unvollständige Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-171">If the impersonation level is not sufficient, a provider might refuse a request or provide incomplete information.</span></span>

<span data-ttu-id="7c2ab-172">Wenn Sie die Identitätswechsel Ebene nicht in einem Moniker oder durch Festlegen von " [**Swap Security. Identitäts ationlevel**](swbemsecurity-impersonationlevel.md) " für ein Sicherungs fähiges Objekt festlegen, legen Sie die Standard-DCOM-Identitätswechsel Ebene für das Betriebssystem fest.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-172">If you do not set the impersonation level in either a moniker or by setting [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) on a securable object, then set the default DCOM impersonation level for the operating system.</span></span> <span data-ttu-id="7c2ab-173">Die Ebene des Identitäts Wechsels muss entsprechend den Anforderungen des Ziel Betriebssystems festgelegt werden, mit dem Sie eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-173">The impersonation level must be set according to the requirements of the target operating system to which you are connecting.</span></span> <span data-ttu-id="7c2ab-174">Weitere Informationen finden Sie unter [Herstellen einer Verbindung zwischen verschiedenen Betriebssystemen](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span><span class="sxs-lookup"><span data-stu-id="7c2ab-174">For more information, see [Connecting Between Different Operating Systems](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span></span>

<span data-ttu-id="7c2ab-175">Im folgenden VBScript-Codebeispiel wird gezeigt, wie die Identitätswechsel Ebene im gleichen Skript geändert wird.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-175">The following VBScript code example shows changing the impersonation level in the same script shown above.</span></span>


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" _
                              & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
             "FreeSpace: " & vbTab & objDisk.FreeSpace 
Next
```



<span data-ttu-id="7c2ab-176">In der folgenden Tabelle werden die Authentifizierungs Ebenen in [wbemimpersonationlevelenum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) aufgelistet, die verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-176">The following table lists the authentication levels in [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) that use.</span></span>



| <span data-ttu-id="7c2ab-177">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="7c2ab-177">Name/value</span></span>                                                    | <span data-ttu-id="7c2ab-178">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c2ab-178">Description</span></span>                                                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c2ab-179">**wbemimpersonationlevelanonymous**</span><span class="sxs-lookup"><span data-stu-id="7c2ab-179">**wbemImpersonationLevelAnonymous**</span></span><br/> <span data-ttu-id="7c2ab-180">1</span><span class="sxs-lookup"><span data-stu-id="7c2ab-180">1</span></span><br/>   | <span data-ttu-id="7c2ab-181">Moniker: Anonym</span><span class="sxs-lookup"><span data-stu-id="7c2ab-181">Moniker: Anonymous</span></span><br/> <span data-ttu-id="7c2ab-182">Verbirgt die Anmeldeinformationen des Aufrufers.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-182">Hides the credentials of the caller.</span></span> <span data-ttu-id="7c2ab-183">Bei Verwendung dieser Identitätswechselebene können Aufrufe von WMI fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-183">Calls to WMI may fail with this impersonation level.</span></span><br/>                                                                                                  |
| <span data-ttu-id="7c2ab-184">**wbemimpersonationlevelidentifizierung**</span><span class="sxs-lookup"><span data-stu-id="7c2ab-184">**wbemImpersonationLevelIdentify**</span></span><br/> <span data-ttu-id="7c2ab-185">2</span><span class="sxs-lookup"><span data-stu-id="7c2ab-185">2</span></span><br/>    | <span data-ttu-id="7c2ab-186">Moniker: identifizieren</span><span class="sxs-lookup"><span data-stu-id="7c2ab-186">Moniker: Identify</span></span><br/> <span data-ttu-id="7c2ab-187">Ermöglicht es Objekten, die Anmeldeinformationen des Aufrufers abzufragen.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-187">Allows objects to query the credentials of the caller.</span></span> <span data-ttu-id="7c2ab-188">Bei Verwendung dieser Identitätswechselebene können Aufrufe von WMI fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-188">Calls to WMI may fail with this impersonation level.</span></span><br/>                                                                                 |
| <span data-ttu-id="7c2ab-189">**wbemimpersonationlevelidentitäts-Ate**</span><span class="sxs-lookup"><span data-stu-id="7c2ab-189">**wbemImpersonationLevelImpersonate**</span></span><br/> <span data-ttu-id="7c2ab-190">3</span><span class="sxs-lookup"><span data-stu-id="7c2ab-190">3</span></span><br/> | <span data-ttu-id="7c2ab-191">Moniker: Identität annehmen</span><span class="sxs-lookup"><span data-stu-id="7c2ab-191">Moniker: Impersonate</span></span><br/> <span data-ttu-id="7c2ab-192">Ermöglicht es Objekten, die Anmeldeinformationen des Aufrufers zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-192">Allows objects to use the credentials of the caller.</span></span> <span data-ttu-id="7c2ab-193">Dies ist die empfohlene Identitätswechsel Ebene für die Skript-API für WMI-Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-193">This is the recommended impersonation level for Scripting API for WMI calls.</span></span><br/>                                                        |
| <span data-ttu-id="7c2ab-194">**wbemimpersonationleveldelegat**</span><span class="sxs-lookup"><span data-stu-id="7c2ab-194">**wbemImpersonationLevelDelegate**</span></span><br/> <span data-ttu-id="7c2ab-195">4</span><span class="sxs-lookup"><span data-stu-id="7c2ab-195">4</span></span><br/>    | <span data-ttu-id="7c2ab-196">Moniker: Delegat</span><span class="sxs-lookup"><span data-stu-id="7c2ab-196">Moniker: Delegate</span></span><br/> <span data-ttu-id="7c2ab-197">Ermöglicht es Objekten, anderen Objekten die Verwendung der Anmeldeinformationen des Aufrufers zu gestatten.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-197">Allows objects to permit other objects to use the credentials of the caller.</span></span> <span data-ttu-id="7c2ab-198">Dieser Identitätswechsel funktioniert mit der Skript-API für WMI-Aufrufe, kann jedoch ein unnötiges Sicherheitsrisiko darstellen.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-198">This impersonation will work with Scripting API for WMI calls but may constitute an unnecessary security risk.</span></span><br/> |



 

<span data-ttu-id="7c2ab-199">Im folgenden Beispiel wird gezeigt, wie der Identitätswechsel in einer Monikerzeichenfolge festgelegt wird, wenn eine bestimmte Instanz des [**Win32- \_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process)angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-199">The following example shows how to set the impersonation in a moniker string when obtaining a specific instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>


```VB
Set object = GetObject("winmgmts:{impersonationLevel=impersonate}!root\cimv2:Win32_Process.Handle='0'")
```



<span data-ttu-id="7c2ab-200">Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="7c2ab-200">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

## <a name="setting-the-default-impersonation-level-using-the-registry"></a><span data-ttu-id="7c2ab-201">Festlegen der Standard Identitätswechsel Ebene mithilfe der Registrierung</span><span class="sxs-lookup"><span data-stu-id="7c2ab-201">Setting the Default Impersonation Level Using the Registry</span></span>

<span data-ttu-id="7c2ab-202">Wenn Sie Zugriff auf die Registrierung haben, können Sie auch den Standard Registrierungsschlüssel für die Identitätswechsel Ebene festlegen.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-202">If you have access to the registry, you can also set the default impersonation level registry key.</span></span> <span data-ttu-id="7c2ab-203">Dieser Schlüssel gibt an, welche Identitätswechsel Ebene die Skript-API für WMI verwendet, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-203">This key specifies which impersonation level the Scripting API for WMI uses unless otherwise specified.</span></span> <span data-ttu-id="7c2ab-204">Der folgende Pfad identifiziert den Registrierungs Pfad.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-204">The following path identifies the registry path.</span></span>

<span data-ttu-id="7c2ab-205">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **Standard** Identitätswechsel Ebene</span><span class="sxs-lookup"><span data-stu-id="7c2ab-205">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Impersonation Level**</span></span>

<span data-ttu-id="7c2ab-206">Standardmäßig ist der Registrierungsschlüssel auf 3 festgelegt. dabei wird die Identitätswechsel Ebene annehmen angegeben.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-206">By default, the registry key is set to 3, specifying the Impersonate impersonation level.</span></span> <span data-ttu-id="7c2ab-207">Einige Anbieter erfordern möglicherweise eine höhere Identitätswechsel Ebene.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-207">Some providers may require a higher level of impersonation.</span></span>

## <a name="accessing-the-swbemsecurity-object-in-vbscript"></a><span data-ttu-id="7c2ab-208">Zugreifen auf das "Swap Security"-Objekt in VBScript</span><span class="sxs-lookup"><span data-stu-id="7c2ab-208">Accessing the SWbemSecurity Object in VBScript</span></span>

<span data-ttu-id="7c2ab-209">Die andere Möglichkeit, die Identitätswechsel Ebene festzulegen, ist das [**Swap**](swbemsecurity.md) -Sicherheits Objekt, das als [**\_ Sicherheits**](swbemservices-security-.md) Eigenschaft der Objekte " [**Swap Services**](swbemservices.md)", " [**errbewbject**](swbemobject.md)", " [**errbemubjectset**](swbemobjectset.md)", " [**errbemeventsource**](swbemeventsource.md)", " [**errbewbjectpath**](swbemobjectpath.md)" und " [**errbemlocator**](swbemlocator.md) " angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-209">The other way you can set the impersonation level is from the [**SWbemSecurity**](swbemsecurity.md) security object, which appears as the [**Security\_**](swbemservices-security-.md) property of the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemEventSource**](swbemeventsource.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects.</span></span>

<span data-ttu-id="7c2ab-210">WMI übergibt die Sicherheitseinstellung eines übergeordneten Objekts an die nachfolgenden Elemente des ursprünglichen Objekts.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-210">WMI passes the security setting of a parent object to the descendants of the original object.</span></span> <span data-ttu-id="7c2ab-211">Aus diesem Grund können Sie die Identitätswechsel Ebene eines " [**errbemservices**](swbemservices.md) "-Objekts festlegen, nachdem Sie sich bei WMI-und API-Aufrufen mit diesem Objekt oder Objekten, die daraus erstellt wurden, anmelden, z. b. Objekte des Typs " [**Austausch Vorgang**](swbemobject.md)".</span><span class="sxs-lookup"><span data-stu-id="7c2ab-211">Therefore, you can set the impersonation level of an [**SWbemServices**](swbemservices.md) object after logging on to WMI and API calls using this object or objects created from it, such as objects of type [**SWbemObject**](swbemobject.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c2ab-212">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7c2ab-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c2ab-213">Herstellen einer Verbindung mit WMI auf einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="7c2ab-213">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="7c2ab-214">Sichern von Skript Clients</span><span class="sxs-lookup"><span data-stu-id="7c2ab-214">Securing Scripting Clients</span></span>](securing-scripting-clients.md)
</dt> </dl>

 

