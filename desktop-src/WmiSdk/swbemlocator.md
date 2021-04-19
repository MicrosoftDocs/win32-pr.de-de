---
description: Mit den Methoden des-Objekts von "Swap-Locator" können Sie ein-Objekt abrufen, das eine Verbindung mit einem Namespace auf einem lokalen Computer oder einem Remote Host Computer darstellt.
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: Swap-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator
- ISWbemLocator
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 964b040fa5046aa619dc08df92838dca343ba9b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348660"
---
# <a name="swbemlocator-object"></a><span data-ttu-id="23955-103">Swap-Objekt</span><span class="sxs-lookup"><span data-stu-id="23955-103">SWbemLocator object</span></span>

<span data-ttu-id="23955-104">Mit den Methoden des-Objekts von " **Swap-Locator** " können Sie [**ein-**](swbemservices.md) Objekt abrufen, das eine Verbindung mit einem Namespace auf einem lokalen Computer oder einem Remote Host Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="23955-104">You can use the methods of the **SWbemLocator** object to obtain an [**SWbemServices**](swbemservices.md) object that represents a connection to a namespace on either a local computer or a remote host computer.</span></span> <span data-ttu-id="23955-105">Anschließend können Sie die Methoden des WS- **Services** -Objekts verwenden, um auf WMI zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="23955-105">You can then use the methods of the **SWbemServices** object to access WMI.</span></span> <span data-ttu-id="23955-106">Dieses Objekt kann durch den VBScript-Befehl "up- **Object** " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="23955-106">This object can be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="23955-107">Member</span><span class="sxs-lookup"><span data-stu-id="23955-107">Members</span></span>

<span data-ttu-id="23955-108">Das Objekt " **Swap-Locator** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="23955-108">The **SWbemLocator** object has these types of members:</span></span>

-   [<span data-ttu-id="23955-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="23955-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="23955-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23955-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="23955-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="23955-111">Methods</span></span>

<span data-ttu-id="23955-112">Das **taubemlocator** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="23955-112">The **SWbemLocator** object has these methods.</span></span>



| <span data-ttu-id="23955-113">Methode</span><span class="sxs-lookup"><span data-stu-id="23955-113">Method</span></span>                                              | <span data-ttu-id="23955-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23955-114">Description</span></span>                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [<span data-ttu-id="23955-115">**Server Verbindung**</span><span class="sxs-lookup"><span data-stu-id="23955-115">**ConnectServer**</span></span>](swbemlocator-connectserver.md) | <span data-ttu-id="23955-116">Stellt eine Verbindung mit WMI auf dem angegebenen Computer her.</span><span class="sxs-lookup"><span data-stu-id="23955-116">Connects to WMI on the specified computer.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="23955-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23955-117">Properties</span></span>

<span data-ttu-id="23955-118">Das **taubemlocator** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="23955-118">The **SWbemLocator** object has these properties.</span></span>



| <span data-ttu-id="23955-119">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="23955-119">Property</span></span>                                                | <span data-ttu-id="23955-120">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="23955-120">Access type</span></span>          | <span data-ttu-id="23955-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23955-121">Description</span></span>                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="23955-122">**Sicherheit\_**</span><span class="sxs-lookup"><span data-stu-id="23955-122">**Security\_**</span></span>](swbemlocator-security-.md)<br/> | <span data-ttu-id="23955-123">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23955-123">Read-only</span></span><br/> | <span data-ttu-id="23955-124">Wird verwendet, um die Sicherheitseinstellungen zu lesen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="23955-124">Used to read or change the security settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="23955-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23955-125">Remarks</span></span>

<span data-ttu-id="23955-126">Am Anfang des WMI-skriptingbibliotheks-Objektmodells befindet sich das Objekt "Swap-Locator".</span><span class="sxs-lookup"><span data-stu-id="23955-126">At the top of the WMI scripting library object model is the SWbemLocator object.</span></span> <span data-ttu-id="23955-127">Mithilfe von "Swap-Locator" wird eine authentifizierte Verbindung mit einem WMI-Namespace hergestellt, ähnlich wie die VBScript-Funktion "GetObject" und der WMI-Moniker "winmgmts:" zum Herstellen einer authentifizierten Verbindung mit WMI.</span><span class="sxs-lookup"><span data-stu-id="23955-127">SWbemLocator is used to establish an authenticated connection to a WMI namespace, much as the VBScript GetObject function and the WMI moniker "winmgmts:" are used to establish an authenticated connection to WMI.</span></span> <span data-ttu-id="23955-128">Allerdings ist der Austausch Vorgang so konzipiert, dass zwei spezifische Skript Szenarien adressiert werden, die nicht mithilfe von GetObject und dem WMI-Moniker ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="23955-128">However, SWbemLocator is designed to address two specific scripting scenarios that cannot be performed using GetObject and the WMI moniker.</span></span> <span data-ttu-id="23955-129">Wenn Sie Folgendes benötigen, müssen Sie den folgenden Befehl verwenden:</span><span class="sxs-lookup"><span data-stu-id="23955-129">You must use SWbemLocator if you need to:</span></span>

-   <span data-ttu-id="23955-130">Geben Sie Benutzer-und Kenn Wort Anmelde Informationen für die Verbindung mit WMI auf einem Remote Computer an.</span><span class="sxs-lookup"><span data-stu-id="23955-130">Provide user and password credentials to connect to WMI on a remote computer.</span></span> <span data-ttu-id="23955-131">Der WMI-Moniker, der mit der GetObject-Funktion verwendet wird, enthält keinen Mechanismus zum Angeben von Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="23955-131">The WMI moniker used with the GetObject function does not include a mechanism for specifying credentials.</span></span> <span data-ttu-id="23955-132">Die meisten WMI-Aktivitäten (einschließlich aller auf Remote Computern ausgeführten) erfordern Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="23955-132">Most WMI activities (including all of those carried out on remote computers) require administrator rights.</span></span> <span data-ttu-id="23955-133">Wenn Sie sich in der Regel mit einem regulären Benutzerkonto anstelle eines Administrator Kontos anmelden, können Sie die meisten WMI-Aufgaben nur ausführen, wenn Sie das Skript unter Alternative Anmelde Informationen ausführen.</span><span class="sxs-lookup"><span data-stu-id="23955-133">If you typically log on using a regular user account instead of an administrator account, you will not be able to perform most WMI tasks unless you run the script under alternate credentials.</span></span>
-   <span data-ttu-id="23955-134">Stellen Sie eine Verbindung mit WMI her, wenn Sie ein WMI-Skript aus einer Webseite heraus ausführen.</span><span class="sxs-lookup"><span data-stu-id="23955-134">Connect to WMI if you are running a WMI script from within a Web page.</span></span> <span data-ttu-id="23955-135">Sie können die GetObject-Funktion nicht verwenden, wenn Sie Skripts ausführen, die in einer HTML-Seite eingebettet sind, da Internet Explorer die Verwendung von GetObject aus Sicherheitsgründen nicht zulässt.</span><span class="sxs-lookup"><span data-stu-id="23955-135">You cannot use the GetObject function when running scripts embedded within an HTML page because Internet Explorer disallows the use of GetObject for security reasons.</span></span>

<span data-ttu-id="23955-136">Außerdem empfiehlt es sich, für die Verbindung mit WMI die Verbindung mit WMI zu verwenden, wenn Sie die WMI-Verbindungs Zeichenfolge mit "GetObject" verwirrend oder schwierig finden.</span><span class="sxs-lookup"><span data-stu-id="23955-136">In addition, you might want to use SWbemLocator to connect to WMI if you find the WMI connection string used with GetObject confusing or difficult.</span></span>

<span data-ttu-id="23955-137">Sie verwenden "" anstelle von "GetObject", um einen Verweis auf "Swap" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="23955-137">You use CreateObject rather than GetObject to create a reference to SWbemLocator.</span></span> <span data-ttu-id="23955-138">Um den Verweis zu erstellen, müssen Sie die Funktion "degid" ("WbemScripting. Swap") der Funktion "degid" ("WbemScripting. sexbemlocator") der Funktion "degid" übergeben, wie in Zeile 2 im folgenden Skript Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="23955-138">To create the reference, you must pass the CreateObject function the SWbemLocator programmatic identifier (ProgID) "WbemScripting.SWbemLocator", as shown on line 2 in the following script sample.</span></span> <span data-ttu-id="23955-139">Nachdem Sie einen Verweis auf ein Objekt vom Typ "WS-Locator" abgerufen haben, rufen Sie die ConnectServer-Methode auf, um eine Verbindung mit WMI herzustellen und einen Verweis auf ein Objekt vom Typ "WS</span><span class="sxs-lookup"><span data-stu-id="23955-139">After you obtain a reference to an SWbemLocator object, you call the ConnectServer method to connect to WMI and obtain a reference to an SWbemServices object.</span></span> <span data-ttu-id="23955-140">Dies wird in Zeile 3 des folgenden Skripts veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="23955-140">This is demonstrated on line 3 of the following script.</span></span>


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="23955-141">Wenn Sie ein Skript unter Alternativen Anmelde Informationen ausführen möchten, fügen Sie den Benutzernamen und das Kennwort als zusätzliche Parameter an ConnectServer ein.</span><span class="sxs-lookup"><span data-stu-id="23955-141">To run a script under alternate credentials, include the user name and password as additional parameters passed to ConnectServer.</span></span> <span data-ttu-id="23955-142">Dieses Skript wird z. b. unter den Anmelde Informationen eines Benutzers namens kenmyer mit dem Kennwort homerj ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23955-142">For example, this script runs under the credentials of a user named kenmyer, with the password homerj.</span></span>


```VB
strComputer = "atl-dc-01"
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer _
    (strComputer, "root\cimv2", "kenmyer", "homerj")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="23955-143">Sie können auch das Format Domäne \\ Benutzername verwenden, um einen Benutzernamen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="23955-143">You can also use the Domain\\User Name format to specify a user name.</span></span> <span data-ttu-id="23955-144">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="23955-144">For example:</span></span>

`" fabrikam\kenmyer"`

## <a name="examples"></a><span data-ttu-id="23955-145">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23955-145">Examples</span></span>

<span data-ttu-id="23955-146">Im folgenden PowerShell-Beispiel wird **SWbemLocator** verwendet, um eine Verbindung mit einem Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="23955-146">The following PowerShell example uses **SWbemLocator** to connect to a server.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="23955-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23955-147">Requirements</span></span>



| <span data-ttu-id="23955-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23955-148">Requirement</span></span> | <span data-ttu-id="23955-149">Wert</span><span class="sxs-lookup"><span data-stu-id="23955-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23955-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23955-150">Minimum supported client</span></span><br/> | <span data-ttu-id="23955-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23955-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23955-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23955-152">Minimum supported server</span></span><br/> | <span data-ttu-id="23955-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23955-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23955-154">Header</span><span class="sxs-lookup"><span data-stu-id="23955-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="23955-155"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="23955-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="23955-156">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="23955-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="23955-157"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="23955-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="23955-158">DLL</span><span class="sxs-lookup"><span data-stu-id="23955-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23955-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23955-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="23955-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="23955-160">CLSID</span></span><br/>                    | <span data-ttu-id="23955-161">CLSID- \_ Austausch</span><span class="sxs-lookup"><span data-stu-id="23955-161">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="23955-162">IID</span><span class="sxs-lookup"><span data-stu-id="23955-162">IID</span></span><br/>                      | <span data-ttu-id="23955-163">IID \_ iswbemlocator</span><span class="sxs-lookup"><span data-stu-id="23955-163">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="23955-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23955-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23955-165">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="23955-165">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




