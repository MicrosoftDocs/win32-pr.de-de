---
description: Das Format der Monikerzeichenfolge ähnelt einem standardmäßigen WMI-Objekt Pfad. Weitere Informationen finden Sie unter WMI-Objekt Pfad Anforderungen.
ms.assetid: 1aacc523-2a2f-43f5-96a3-aa0387cbae3e
ms.tgt_platform: multiple
title: Erstellen einer Monikerzeichenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e54e29b3c8f14890dc1cedd5907059308e8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344938"
---
# <a name="constructing-a-moniker-string"></a><span data-ttu-id="c6e56-104">Erstellen einer Monikerzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c6e56-104">Constructing a Moniker String</span></span>

<span data-ttu-id="c6e56-105">Das Format der Monikerzeichenfolge ähnelt einem standardmäßigen WMI-Objekt Pfad.</span><span class="sxs-lookup"><span data-stu-id="c6e56-105">The moniker string format is similar to that of a standard WMI object path.</span></span> <span data-ttu-id="c6e56-106">Weitere Informationen finden Sie unter [WMI-Objekt Pfad Anforderungen](wmi-object-path-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c6e56-106">For more information, see [WMI Object Path Requirements](wmi-object-path-requirements.md).</span></span>

<span data-ttu-id="c6e56-107">Ein Moniker besteht aus den folgenden Teilen:</span><span class="sxs-lookup"><span data-stu-id="c6e56-107">A moniker has the following parts:</span></span>

-   <span data-ttu-id="c6e56-108">Das Präfix winmgmts: (obligatorisch).</span><span class="sxs-lookup"><span data-stu-id="c6e56-108">The prefix WinMgmts: (mandatory).</span></span> <span data-ttu-id="c6e56-109">Das Präfix weist den Windows Script Host (WSH) an, dass der folgende Code die [Skript-API-Objekte](scripting-api-objects.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6e56-109">The prefix instructs the Windows Script Host (WSH) that the following code will be using the [Scripting API objects](scripting-api-objects.md).</span></span>
-   <span data-ttu-id="c6e56-110">Eine Sicherheits Einstellungs Komponente (optional)</span><span class="sxs-lookup"><span data-stu-id="c6e56-110">A security settings component (optional)</span></span>
-   <span data-ttu-id="c6e56-111">Eine WMI-Objekt Pfadkomponente (optional)</span><span class="sxs-lookup"><span data-stu-id="c6e56-111">A WMI object path component (optional)</span></span>

<span data-ttu-id="c6e56-112">Ein Kennwort kann nicht in einer WMI-Monikerzeichenfolge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c6e56-112">You cannot specify a password in a WMI moniker string.</span></span> <span data-ttu-id="c6e56-113">Wenn Sie beim Herstellen einer Verbindung mit WMI das Kennwort ("*stranpassword* "-Parameter) oder den Authentifizierungstyp ("*chanauthority* ") ändern müssen, dann wenden Sie sich an "WS. [**ConnectServer**](swbemlocator-connectserver.md)".</span><span class="sxs-lookup"><span data-stu-id="c6e56-113">If you must change the password (*strPassword* parameter) or the type of authentication (*strAuthority* parameter) when connecting to WMI, then call [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="c6e56-114">Beachten Sie, dass Sie nur das Kennwort und die Autorität in Verbindungen mit Remote Computern angeben können.</span><span class="sxs-lookup"><span data-stu-id="c6e56-114">Be aware that you can only specify the password and authority in connections to remote computers.</span></span> <span data-ttu-id="c6e56-115">Der Versuch, diese in einem Skript festzulegen, das auf dem lokalen Computer ausgeführt wird, führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="c6e56-115">Attempting to set these in a script that is running on the local computer results in a error.</span></span> <span data-ttu-id="c6e56-116">Weitere Informationen dazu, wann die Sicherheitseinstellungen und Objekt Pfad Komponenten verwendet werden, finden Sie unter [WMI-Sicherheitseinstellungen](/previous-versions/tn-archive/ee156574(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="c6e56-116">For more information about when the security settings and object path components are used, see [WMI Security Settings](/previous-versions/tn-archive/ee156574(v=technet.10)).</span></span>

<span data-ttu-id="c6e56-117">Der folgende Moniker gibt das [**Swap Services**](swbemservices.md) -Objekt an, das den Standardwert für den Namespace Stamm darstellt, bei dem der Identitätswechsel \\ aktiviert ist und die wbemprivilegedebug-Berechtigung (SeDebugPrivilege) aktiviert und die wbemprivilegesection-Berechtigung (SeSecurityPrivilege) deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c6e56-117">The following moniker specifies the [**SWbemServices**](swbemservices.md) object that represents the namespace root\\default, with impersonation on and the wbemPrivilegeDebug (SeDebugPrivilege) privilege enabled, and the wbemPrivilegeSecurity (SeSecurityPrivilege) privilege disabled.</span></span>


```VB
"winmgmts:{impersonationLevel=impersonate," & "(debug,!security)}!root\default"
```



> [!Note]
>
> <span data-ttu-id="c6e56-118">Bei allen Zeichen folgen literalen wird Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="c6e56-118">All string literals are case-insensitive.</span></span>
>
> <span data-ttu-id="c6e56-119">Mit dem Präfix "!" für eine Berechtigung wird angegeben, dass die Berechtigung deaktiviert werden soll. das Weglassen dieses Präfixes impliziert, dass die Berechtigung aktiviert werden muss.</span><span class="sxs-lookup"><span data-stu-id="c6e56-119">The "!" prefix on a privilege indicates that the privilege is to be disabled; the omission of this prefix implies that the privilege is to be enabled.</span></span>
>
> <span data-ttu-id="c6e56-120">Das Präfix "!" wird für den Computernamen oder den Namespace verwendet, wenn die Sicherheitseinstellungen vor dem Computernamen oder Namespace in Klammern angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c6e56-120">The "!" prefix is used on the computer name or namespace when security settings are specified in brackets before the computer name or namespace.</span></span>

 

<span data-ttu-id="c6e56-121">Die folgenden Standard Zuweisungen sind zulässig, wenn der Objekt Pfad angegeben wird:</span><span class="sxs-lookup"><span data-stu-id="c6e56-121">The following default assignments are allowed when specifying the object path:</span></span>

-   <span data-ttu-id="c6e56-122">Der Computername des Computers kann im Objekt Pfad weggelassen werden. in diesem Fall wird der Name des lokalen Computers angenommen.</span><span class="sxs-lookup"><span data-stu-id="c6e56-122">The computer machine name can be omitted from the object path, in which case the local machine name is assumed.</span></span>
-   <span data-ttu-id="c6e56-123">Der Namespace kann im Objekt Pfad weggelassen werden. in diesem Fall wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="c6e56-123">The namespace can be omitted from the object path, in which case the default namespace is assumed.</span></span>

    <span data-ttu-id="c6e56-124">Dies wird durch den Wert des Registrierungsschlüssels **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **Standard Namespace** festgelegt. der Standardwert ist "root \\ CIMv2".</span><span class="sxs-lookup"><span data-stu-id="c6e56-124">This is determined by the value of the registry key **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Namespace**, the default value is "Root\\CIMv2".</span></span>

-   <span data-ttu-id="c6e56-125">Es kann auch eine Klasse oder eine Instanz angegeben werden. in diesem Fall handelt es sich bei dem zurückgegebenen Objekt um ein WMI-Objekt und nicht um ein Dienst Objekt.</span><span class="sxs-lookup"><span data-stu-id="c6e56-125">A class or instance can also be specified, in which case the returned object is a WMI object rather than a services object.</span></span>

> [!Note]  
> <span data-ttu-id="c6e56-126">Wenn eine Klasse oder eine Instanz angegeben ist, können Sie den Namespace nicht weglassen, wenn Sie den Computernamen angeben.</span><span class="sxs-lookup"><span data-stu-id="c6e56-126">If a class or instance is specified, you cannot omit the namespace when specifying the computer machine name.</span></span>

 

<span data-ttu-id="c6e56-127">Einen Verweis auf die für die WMI-Monikerzeichenfolge verwendeten Berechtigungs Konstanten finden Sie unter [Berechtigungs Konstanten](privilege-constants.md)und in den Deskriptoren "Skript-Kurzname".</span><span class="sxs-lookup"><span data-stu-id="c6e56-127">For a reference of the Privilege Constants used on WMI moniker string, see [Privilege Constants](privilege-constants.md), and the "Scripting short name" descriptors.</span></span>

## <a name="valid-moniker-strings"></a><span data-ttu-id="c6e56-128">Gültige Monikerzeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="c6e56-128">Valid Moniker Strings</span></span>

<span data-ttu-id="c6e56-129">In den folgenden Beispielen werden gültige Monikerzeichenfolgen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c6e56-129">The following examples show valid moniker strings.</span></span>

<span data-ttu-id="c6e56-130">Der folgende Moniker identifiziert den Standard Namespace auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="c6e56-130">The following moniker identifies the default namespace on the local computer.</span></span> <span data-ttu-id="c6e56-131">Ein [**-**](swbemservices.md) Objekt wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e56-131">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
WinMgmts:
```



<span data-ttu-id="c6e56-132">Der folgende Moniker identifiziert den Standard Namespace auf dem Computer "MyServer".</span><span class="sxs-lookup"><span data-stu-id="c6e56-132">The following moniker identifies the default namespace on the computer myServer.</span></span> <span data-ttu-id="c6e56-133">Ein [**-**](swbemservices.md) Objekt wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e56-133">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts://myServer"
```



<span data-ttu-id="c6e56-134">Der folgende Moniker identifiziert den root \\ CIMV2-Namespace auf dem MyServer-Computer.</span><span class="sxs-lookup"><span data-stu-id="c6e56-134">The following moniker identifies the root\\cimv2 namespace on the myServer computer.</span></span> <span data-ttu-id="c6e56-135">Ein [**-**](swbemservices.md) Objekt wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e56-135">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts://myServer/root/cimv2"
```



<span data-ttu-id="c6e56-136">Der folgende Moniker identifiziert den root \\ CIMV2-Namespace auf dem lokalen Server.</span><span class="sxs-lookup"><span data-stu-id="c6e56-136">The following moniker identifies the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="c6e56-137">Ein [**-**](swbemservices.md) Objekt wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e56-137">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts:root/cimv2"
```



<span data-ttu-id="c6e56-138">Der folgende Moniker identifiziert die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse im root \\ CIMV2-Namespace auf dem MyServer-Server.</span><span class="sxs-lookup"><span data-stu-id="c6e56-138">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the root\\cimv2 namespace on the myServer server.</span></span> <span data-ttu-id="c6e56-139">Ein [**-**](swbemobject.md) Objekt wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e56-139">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" _
    & "!//myServer/root/cimv2:Win32_LogicalDisk"
```



<span data-ttu-id="c6e56-140">Der folgende Moniker identifiziert die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse im root \\ CIMV2-Namespace auf dem lokalen Server.</span><span class="sxs-lookup"><span data-stu-id="c6e56-140">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="c6e56-141">Ein [**-**](swbemobject.md) Objekt wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e56-141">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk"
```



<span data-ttu-id="c6e56-142">Der folgende Moniker identifiziert die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse im Standard Namespace auf dem lokalen Server.</span><span class="sxs-lookup"><span data-stu-id="c6e56-142">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the default namespace on the local server.</span></span> <span data-ttu-id="c6e56-143">Ein [**-**](swbemobject.md) Objekt wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e56-143">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk"
```



<span data-ttu-id="c6e56-144">Der folgende Moniker identifiziert die Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , die dem Laufwerk C: im Standard-Skript Namespace auf dem lokalen Server entspricht.</span><span class="sxs-lookup"><span data-stu-id="c6e56-144">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the default scripting namespace on the local server.</span></span> <span data-ttu-id="c6e56-145">Ein [**-**](swbemobject.md) Objekt wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e56-145">An [**SWbemObject**](swbemobject.md) object is returned.</span></span> <span data-ttu-id="c6e56-146">Der Standard Namespace für die Skripterstellung wird durch die standardmäßige Namespace-Konfigurationseinstellung festgelegt, wie im WMI-Steuerelement angegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e56-146">The default namespace for scripting is determined by the default namespace configuration setting as specified in the WMI Control.</span></span> <span data-ttu-id="c6e56-147">Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit mit dem WMI-Steuer](setting-namespace-security-with-the-wmi-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="c6e56-147">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>


```VB
"WinMgmts::Win32_LogicalDisk='C:'"
```



<span data-ttu-id="c6e56-148">Der folgende Moniker identifiziert die Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , die dem Laufwerk C: im root \\ CIMV2-Namespace auf dem MyServer-Server entspricht.</span><span class="sxs-lookup"><span data-stu-id="c6e56-148">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the root\\cimv2 namespace on the myServer server.</span></span> <span data-ttu-id="c6e56-149">Ein [**-**](swbemobject.md) Objekt wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e56-149">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!//myServer/root/cimv2:Win32_LogicalDisk="C:""
```



<span data-ttu-id="c6e56-150">Der folgende Moniker identifiziert die Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , die dem Laufwerk C: im root \\ CIMV2-Namespace auf dem lokalen Server entspricht.</span><span class="sxs-lookup"><span data-stu-id="c6e56-150">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="c6e56-151">Ein [**-**](swbemobject.md) Objekt wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e56-151">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk="C:""
```



<span data-ttu-id="c6e56-152">Der folgende Moniker identifiziert die Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , die dem Laufwerk C: im Standard Namespace auf dem lokalen Server entspricht.</span><span class="sxs-lookup"><span data-stu-id="c6e56-152">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the default namespace on the local server.</span></span> <span data-ttu-id="c6e56-153">Ein [**-**](swbemobject.md) Objekt wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6e56-153">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk="C:""
```



<span data-ttu-id="c6e56-154">Der folgende Moniker legt die Identitätswechsel Ebene fest, um die Identität anzunehmen, und legt die SE- \_ Debugberechtigung fest.</span><span class="sxs-lookup"><span data-stu-id="c6e56-154">The following moniker sets the impersonation level to impersonate and sets the SE\_DEBUG privilege.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate, (Debug)}"
```



<span data-ttu-id="c6e56-155">Der folgende Moniker legt die Identitätswechsel Ebene fest, um die Identität anzunehmen, und legt die SE- \_ Debugberechtigung fest.</span><span class="sxs-lookup"><span data-stu-id="c6e56-155">The following moniker sets the impersonation level to impersonate and sets the SE\_DEBUG privilege.</span></span> <span data-ttu-id="c6e56-156">Außerdem wird das Recht zum Herunterfahren der Berechtigung aufgehoben \_ .</span><span class="sxs-lookup"><span data-stu-id="c6e56-156">It also revokes the SE\_SHUTDOWN privilege.</span></span>


```VB
"WinMgmts:{impersonate,(Debug,!Shutdown)}"
```



<span data-ttu-id="c6e56-157">Der folgende Moniker ruft in englischer Sprache lokalisierte Beschreibungen für die Klasse **MyClass** aus dem \\ WMI-Stamm Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="c6e56-157">The following moniker retrieves American English localized descriptions for the **myclass** class from the root\\wmi namespace.</span></span>


```VB
"WinMgmts:[locale=ms_409]!root/wmi:myclass"
```



<span data-ttu-id="c6e56-158">Der folgende Moniker fordert die Kerberos-Authentifizierung mithilfe des Prinzipal Servers "mydomain" an \\ .</span><span class="sxs-lookup"><span data-stu-id="c6e56-158">The following moniker requests Kerberos authentication using the principal mydomain\\server.</span></span>


```VB
"Winmgmts:{impersonationLevel=delegate," _
    & "authority=kerberos:mydomain\server}" _
    & "!//myserver/root/default:__cimomidentification=@"
```



<span data-ttu-id="c6e56-159">Der folgende Moniker fordert die NTLM-Authentifizierung mithilfe der mydomain-Domäne an.</span><span class="sxs-lookup"><span data-stu-id="c6e56-159">The following moniker requests NTLM authentication using the mydomain domain.</span></span>


```VB
"Winmgmts:{impersonationLevel=impersonate," & _
    "authority=ntlmdomain:mydomain} " & _
    "!//myserver/root/default:__cimomidentification=@
```



<span data-ttu-id="c6e56-160">Im folgenden VBScript-Codebeispiel wird gezeigt, wie Sicherheits-und Gebiets Schema Parameter in einem Moniker kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="c6e56-160">The following VBScript code example shows how to combine security and locale parameters in a moniker.</span></span>


```VB
'*****************************************************************
'   Name    :  Moniker.vbs
'
'   Purpose :  This example shows how to set various 
'              parameters in a moniker. 
'****************************************************************

Set myobj = GetObject("WINMGMTS:" _
            & "{impersonationLevel=impersonate," _
            & "authenticationLevel=pktPrivacy," _
            & "authority=ntlmdomain:mydomain," _
            & "(Debug,!Shutdown)}" _
            & "[locale=ms_409]" _
            & "!\\User1\ROOT\CIMV2:Win32_LogicalDisk=""C:""")

wscript.echo "File system = " & myobj.filesystem
```



> [!Note]
>
> Obwohl Moniker einen direkteren Zugriff auf Objekte bereitstellen, kann die wiederholte Verwendung von Monikern unter bestimmten Umständen weniger effizient sein als der äquivalente Code, der explizit eine Verbindung mit WMI herstellt. <span data-ttu-id="c6e56-162">Wenn die Anwendungsleistung zu beachten ist, sollten Sie die Verwendung der alternativen Mechanismen in Erwägung ziehen.</span><span class="sxs-lookup"><span data-stu-id="c6e56-162">If application performance is a consideration, consider using the alternative mechanisms.</span></span>
>
> <span data-ttu-id="c6e56-163">Es ist nicht möglich, die **GetObject** -Funktion von VBScript zum Aktualisieren oder Festlegen von Daten zu verwenden, wenn Skripts ausgeführt werden, die in einer HTML-Seite eingebettet sind, da Microsoft Internet Explorer die Verwendung dieses aufrupts aus Sicherheitsgründen verweigert.</span><span class="sxs-lookup"><span data-stu-id="c6e56-163">It is not possible to use the **GetObject** function provided by VBScript to update or set data when running scripts embedded within an HTML page, as Microsoft Internet Explorer denies the use of this call for security reasons.</span></span>

 

 

 
