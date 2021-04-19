---
title: Windows-Remoteverwaltung und WMI
description: Windows-Remoteverwaltung können zum Abrufen von Daten verwendet werden, die von Windows-Verwaltungsinstrumentation bereitgestellt werden.
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6942e89ea2e63ef809f3452e6ce55a493662c938
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106357173"
---
# <a name="windows-remote-management-and-wmi"></a><span data-ttu-id="60052-103">Windows-Remoteverwaltung und WMI</span><span class="sxs-lookup"><span data-stu-id="60052-103">Windows Remote Management and WMI</span></span>

<span data-ttu-id="60052-104">Windows-Remoteverwaltung können zum Abrufen von Daten verwendet werden, die von Windows-Verwaltungsinstrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page) und [Mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)) verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="60052-104">Windows Remote Management can be used to retrieve data exposed by Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page) and [MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)).</span></span> <span data-ttu-id="60052-105">Sie können WMI-Daten mit Skripts oder Anwendungen abrufen, die die [WinRM-Skript-API](winrm-scripting-api.md) oder über das **WinRM** -Befehlszeilen Tool verwenden.</span><span class="sxs-lookup"><span data-stu-id="60052-105">You can obtain WMI data with scripts or applications that use the [WinRM Scripting API](winrm-scripting-api.md) or through the **Winrm** command-line tool.</span></span>

<span data-ttu-id="60052-106">WinRM unterstützt den größten Teil der vertrauten WMI-Klassen und-Vorgänge, einschließlich eingebetteter Objekte.</span><span class="sxs-lookup"><span data-stu-id="60052-106">WinRM supports most of the familiar WMI classes and operations, including embedded objects.</span></span> <span data-ttu-id="60052-107">WinRM kann WMI zum Sammeln von Daten zu [*Ressourcen*](windows-remote-management-glossary.md) oder zum Verwalten von Ressourcen auf einem Windows-basierten Betriebssystem nutzen.</span><span class="sxs-lookup"><span data-stu-id="60052-107">WinRM can leverage WMI to collect data about [*resources*](windows-remote-management-glossary.md) or to manage resources on a Windows-based operating system.</span></span> <span data-ttu-id="60052-108">Dies bedeutet, dass Sie Daten über Objekte wie Datenträger, Netzwerkadapter, Dienste oder Prozesse in Ihrem Unternehmen über den vorhandenen Satz von [WMI-Klassen](/windows/desktop/WmiSdk/wmi-classes)abrufen können.</span><span class="sxs-lookup"><span data-stu-id="60052-108">That means that you can obtain data about objects such as disks, network adapters, services, or processes in your enterprise through the existing set of [WMI classes](/windows/desktop/WmiSdk/wmi-classes).</span></span> <span data-ttu-id="60052-109">Sie können auch auf die Hardware Daten zugreifen, die über den standardmäßigen WMI- [IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="60052-109">You can also access the hardware data that is available from the standard WMI [IPMI provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

## <a name="identifying-a-wmi-resource"></a><span data-ttu-id="60052-110">Identifizieren einer WMI-Ressource</span><span class="sxs-lookup"><span data-stu-id="60052-110">Identifying a WMI Resource</span></span>

<span data-ttu-id="60052-111">Sie können auf eine WMI-Klasse als [*Ressource*](windows-remote-management-glossary.md) in WinRM und im WS-Management-Protokoll verweisen: eine verwaltete Entität, z. b. ein Dienst oder ein Datenträger.</span><span class="sxs-lookup"><span data-stu-id="60052-111">You can reference a WMI class as a [*resource*](windows-remote-management-glossary.md) in WinRM and in the WS-Management protocol: a type of managed entity, like a service or a disk.</span></span>

<span data-ttu-id="60052-112">Eine WMI-Klasse oder-Methode wird durch einen [*URI*](windows-remote-management-glossary.md)identifiziert, ebenso wie jede andere Ressource, wenn das WS-Management Protokoll verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="60052-112">A WMI class or method is identified by a [*URI*](windows-remote-management-glossary.md), just as any other resource is when using the WS-Management protocol.</span></span> <span data-ttu-id="60052-113">Der URI kann eine WMI-Ressource (Klasse), eine WMI-Aktion (-Methode) oder eine bestimmte Instanz einer Klasse in [*Nachrichten*](windows-remote-management-glossary.md) angeben, die über ein Netzwerk gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="60052-113">The URI can specify a WMI resource (class), a WMI action (method), or identify a specific instance of a class in [*messages*](windows-remote-management-glossary.md) sent over a network.</span></span> <span data-ttu-id="60052-114">Weitere Informationen finden Sie unter [Ressourcen-URIs](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="60052-114">For more information, see [Resource URIs](resource-uris.md).</span></span>

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a><span data-ttu-id="60052-115">Erstellen des URI-Präfixes für WMI-Klassen</span><span class="sxs-lookup"><span data-stu-id="60052-115">Constructing the URI Prefix for WMI Classes</span></span>

<span data-ttu-id="60052-116">Das URI-Präfix enthält einen Fixed-Part-und den WMI-Namespace.</span><span class="sxs-lookup"><span data-stu-id="60052-116">The URI prefix contains a fixed part and the WMI namespace.</span></span> <span data-ttu-id="60052-117">Beispielsweise lautet das URI-Präfix in Windows Server, das den fixierten Teil des Präfixes enthält, wie folgt: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` .</span><span class="sxs-lookup"><span data-stu-id="60052-117">For example, the URI prefix in Windows Server that contains the fixed part of the prefix is: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>`.</span></span> <span data-ttu-id="60052-118">Dadurch kann das URI-Präfix für jeden WMI-Namespace generiert werden.</span><span class="sxs-lookup"><span data-stu-id="60052-118">This allows the URI prefix to be generated for any WMI namespace.</span></span> <span data-ttu-id="60052-119">Wenn Sie z. b. **auf \\ den WMI** -Stamm Namespace zugreifen möchten, verwenden Sie das folgende URI-Präfix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` .</span><span class="sxs-lookup"><span data-stu-id="60052-119">For example, to access the **root\\default** WMI namespace, use the following URI prefix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/`.</span></span>

<span data-ttu-id="60052-120">Der Großteil der WMI-Klassen für die Verwaltung ist im **root \\ CIMV2** -Namespace.</span><span class="sxs-lookup"><span data-stu-id="60052-120">The majority of the WMI classes for management are in the **root\\cimv2** namespace.</span></span> <span data-ttu-id="60052-121">Um auf Klassen und Instanzen im **root \\ CIMV2** -Namespace zuzugreifen, verwenden Sie das URI-Präfix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` .</span><span class="sxs-lookup"><span data-stu-id="60052-121">To access classes and instances in **root\\cimv2** namespace, use the URI prefix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`.</span></span> <span data-ttu-id="60052-122">Weitere Informationen finden Sie unter [Ressourcen-URIs](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="60052-122">For more information, see [Resource URIs](resource-uris.md).</span></span>

## <a name="generating-a-complete-uri-for-wmi-classes"></a><span data-ttu-id="60052-123">Erstellen eines kompletten URI für WMI-Klassen</span><span class="sxs-lookup"><span data-stu-id="60052-123">Generating a Complete URI for WMI Classes</span></span>

<span data-ttu-id="60052-124">Der URI, den Sie entweder für das **WinRM** -Befehlszeilen Tool oder für ein Skript angeben, besteht aus dem Präfix und der Ressourcen Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="60052-124">The URI that you supply, either to the **Winrm** command-line tool or to a script, consists of the prefix plus the resource specification.</span></span>

<span data-ttu-id="60052-125">Im folgenden Verfahren wird beschrieben, wie Sie einen Ressourcen-URI generieren, um eine WMI-Klasse zu erhalten oder in einem enumeringvorgang zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="60052-125">The following procedure describes how to generate a resource URI either to get a WMI class or to use in an enumerate operation.</span></span>

<span data-ttu-id="60052-126">**So generieren Sie einen Ressourcen-URI für eine WMI-Klasse**</span><span class="sxs-lookup"><span data-stu-id="60052-126">**To generate a resource URI for a WMI class**</span></span>

1.  <span data-ttu-id="60052-127">Beginnen Sie mit dem Präfix, das angibt, dass das WS-Management Protokoll Schema verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="60052-127">Start with the prefix that indicates the WS-Management protocol schema should be used.</span></span>

    https://schemas.microsoft.com/wbem/wsman/1

    <span data-ttu-id="60052-128">Das Ressourcen-URI-Präfix für die WMI-Klassen ist immer identisch.</span><span class="sxs-lookup"><span data-stu-id="60052-128">The resource URI prefix for WMI classes is always the same.</span></span> <span data-ttu-id="60052-129">Weitere Informationen finden Sie unter [URI-Präfixe](uri-prefixes.md).</span><span class="sxs-lookup"><span data-stu-id="60052-129">For more information, see [URI Prefixes](uri-prefixes.md).</span></span>

2.  <span data-ttu-id="60052-130">Fügen Sie dem Präfix den WMI-Namespace hinzu.</span><span class="sxs-lookup"><span data-stu-id="60052-130">Add the WMI namespace to the prefix.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  <span data-ttu-id="60052-131">Fügen Sie den Klassennamen hinzu.</span><span class="sxs-lookup"><span data-stu-id="60052-131">Add the class name.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  <span data-ttu-id="60052-132">Um den Wert einer Eigenschaft festzulegen oder um eine bestimmte Methode aufzurufen, fügen Sie den erforderlichen Schlüsselwert bzw. die erforderlichen Werte für die Klasse hinzu.</span><span class="sxs-lookup"><span data-stu-id="60052-132">To set the value of a property, or to invoke a specific method, add the required key value or values for the class.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    <span data-ttu-id="60052-133">Wenn Sie den Schlüsselwert leer lassen, wird der ursprüngliche Eigenschafts Wert nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="60052-133">If you leave the key value blank, you will not alter the original property value.</span></span>

    > [!Note]  
    > <span data-ttu-id="60052-134">Wenn Sie den Schlüsselwert leer lassen, wird der Eigenschafts Wert auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60052-134">Leaving the key value blank sets the property value to **NULL**.</span></span>

     

## <a name="locating-a-wmi-resource-with-winrm"></a><span data-ttu-id="60052-135">Suchen einer WMI-Ressource mit WinRM</span><span class="sxs-lookup"><span data-stu-id="60052-135">Locating a WMI Resource with WinRM</span></span>

<span data-ttu-id="60052-136">Sie können WMI-Daten entweder über das Befehlszeilen Tool, mithilfe von **WinRM** oder mithilfe eines Visual Basic Skripts abrufen, das die [WinRM-Skript-API](winrm-scripting-api.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="60052-136">You can obtain WMI data either through the command-line tool, **Winrm**, or through a Visual Basic script that uses the [WinRM Scripting API](winrm-scripting-api.md).</span></span> <span data-ttu-id="60052-137">Sie verwenden keinen [WMI-Pfad](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) , um eine Ressource zu suchen.</span><span class="sxs-lookup"><span data-stu-id="60052-137">You do not use a [WMI path](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) to locate a resource.</span></span> <span data-ttu-id="60052-138">Stattdessen konvertieren Sie den WMI-Namespace und die Hierarchie in einen [*URI*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="60052-138">Instead, you convert the WMI namespace and hierarchy to a [*URI*](windows-remote-management-glossary.md).</span></span>

<span data-ttu-id="60052-139">Der WinRM-URI für eine WMI-Klasse enthält zwei Teile: das [URI-Präfix](uri-prefixes.md) und die Klasse, auf die Sie zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="60052-139">The WinRM URI for a WMI class contains two parts: the [URI prefix](uri-prefixes.md) and the class that you want to access.</span></span>

<span data-ttu-id="60052-140">Beispielsweise kann der folgende URI für die [**Session. Enumerate**](session-enumerate.md) -Methode bereitgestellt werden, um alle Dienste auf einem Computer aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="60052-140">For example, the following URI can be supplied to the [**Session.Enumerate**](session-enumerate.md) method to list all the services on a computer.</span></span> <span data-ttu-id="60052-141">Das URI-Präfix ist `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` , und die-Klasse ist der [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="60052-141">The URI prefix is `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`, and the class is [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

<span data-ttu-id="60052-142">Auflisten der Daten für alle Instanzen einer Ressource oder Klasse in WMI auf verschiedene Weise:</span><span class="sxs-lookup"><span data-stu-id="60052-142">In WMI, list the data for all of the instances of a resource or class in several ways:</span></span>

-   <span data-ttu-id="60052-143">Eine Abfrage für alle Instanzen dieser Ressource.</span><span class="sxs-lookup"><span data-stu-id="60052-143">A query for all the instances of that resource.</span></span>

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   <span data-ttu-id="60052-144">Einen aufzurufenden [**Austausch von "errbemservices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) " oder " [**errbemubject. Instance \_**](/windows/desktop/WmiSdk/swbemobject-instances-)".</span><span class="sxs-lookup"><span data-stu-id="60052-144">A call to [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) or [**SWbemObject.Instances\_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span></span>

    `Set colServices = InstancesOf("Win32_Service")`

<span data-ttu-id="60052-145">In WinRM gibt es eine Möglichkeit, alle Instanzen einer Ressource aufzulisten: [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="60052-145">In WinRM, there is one way to list all of the instances of a resource: [**Session.Enumerate**](session-enumerate.md).</span></span>


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a><span data-ttu-id="60052-146">Suchen einer bestimmten Instanz einer WMI-Ressource</span><span class="sxs-lookup"><span data-stu-id="60052-146">Locating a Specific Instance of a WMI Resource</span></span>

<span data-ttu-id="60052-147">In WMI können Sie eine bestimmte Instanz einer Klasse angeben, indem Sie Werte für die Schlüsseleigenschaften angeben oder eine Instanz Abfragen, die mit einer Liste von Eigenschafts Werten übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="60052-147">In WMI, you can designate a particular instance of a class either by specifying values for the key properties or by querying for an instance that matches a list of property values.</span></span> <span data-ttu-id="60052-148">Schlüsseleigenschaften haben den WMI- [**Schlüssel Qualifizierer**](/windows/desktop/WmiSdk/key-qualifier).</span><span class="sxs-lookup"><span data-stu-id="60052-148">Key properties have the WMI [**Key qualifier**](/windows/desktop/WmiSdk/key-qualifier).</span></span>

<span data-ttu-id="60052-149">Sie können eine bestimmte Instanz einer Klasse auf verschiedene Weise abrufen:</span><span class="sxs-lookup"><span data-stu-id="60052-149">You can obtain a specific instance of a class in several ways:</span></span>

-   <span data-ttu-id="60052-150">Einen aufzurufenden [**Sitzungs. Enumerate**](session-enumerate.md) mit den Parametern *Filter* und *Dialekt* zum Erstellen einer Abfrage.</span><span class="sxs-lookup"><span data-stu-id="60052-150">A call to [**Session.Enumerate**](session-enumerate.md) with the *filter* and *dialect* parameters to create a query.</span></span>

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   <span data-ttu-id="60052-151">Einen aufzurufenden [**Swap-Dienst. Get**](/windows/desktop/WmiSdk/swbemservices-get).</span><span class="sxs-lookup"><span data-stu-id="60052-151">A call to [**SWbemServices.Get**](/windows/desktop/WmiSdk/swbemservices-get).</span></span> <span data-ttu-id="60052-152">Für [**Session. Get**](session-get.md)müssen Sie einen oder mehrere bestimmte Schlüsselwerte angeben, denen ein Fragezeichen (?) vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="60052-152">For [**Session.Get**](session-get.md), you must supply one or more specific key values, preceded by a question mark (?).</span></span>

    <span data-ttu-id="60052-153">Das Format des URI für eine bestimmte Instanz ist `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` .</span><span class="sxs-lookup"><span data-stu-id="60052-153">The format of the URI for a specific instance is `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    <span data-ttu-id="60052-154">Eine WMI-Klasse kann über mehr als einen Schlüssel verfügen.</span><span class="sxs-lookup"><span data-stu-id="60052-154">A WMI class may have more than one key.</span></span> <span data-ttu-id="60052-155">Schlüssel Name-Wert-Paare werden durch ein "+"-Zeichen getrennt.</span><span class="sxs-lookup"><span data-stu-id="60052-155">Key name-value pairs are separated by a "+" sign.</span></span> <span data-ttu-id="60052-156">In diesem Fall lautet das Format: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` .</span><span class="sxs-lookup"><span data-stu-id="60052-156">In that case, the format is: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2`.</span></span>

    <span data-ttu-id="60052-157">Die WinRM-Syntax zum Abrufen eines Singleton-WMI-Objekts unterscheidet sich von WMI.</span><span class="sxs-lookup"><span data-stu-id="60052-157">The WinRM syntax to obtain a singleton WMI object is different from WMI.</span></span> <span data-ttu-id="60052-158">Ein Singleton ist eine WMI-Klasse, die so definiert ist, dass nur eine Instanz zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="60052-158">A singleton is a WMI class defined so that only one instance is allowed.</span></span> <span data-ttu-id="60052-159">[**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) oder [**Win32 \_ wmisetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) sind Beispiele für eine WMI-Singleton-Klasse.</span><span class="sxs-lookup"><span data-stu-id="60052-159">[**Win32\_CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) or [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) are examples of a WMI singleton class.</span></span>

    <span data-ttu-id="60052-160">Die WMI-Syntax für Singletons wird im folgenden VBScript-Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="60052-160">The WMI syntax for singletons is shown in the following VBScript code example.</span></span>

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    <span data-ttu-id="60052-161">Das folgende Beispiel zeigt die WinRM-Singleton-Syntax, die "@" nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="60052-161">The following example shows the WinRM singleton syntax which does not use "@".</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   <span data-ttu-id="60052-162">Hinzufügen eines [*Selektor*](windows-remote-management-glossary.md) zu einem [**ResourceLocator**](resourcelocator.md) -oder [**iwsmanresourcelocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="60052-162">Adding a [*selector*](windows-remote-management-glossary.md) to a [**ResourceLocator**](resourcelocator.md) or [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) object.</span></span>

    <span data-ttu-id="60052-163">Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie ein Selektor verwendet wird, um eine bestimmte Instanz des [**Win32- \_ Prozessors**](/windows/desktop/CIMWin32Prov/win32-processor)zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="60052-163">The following VBScript code example shows how to use a selector to get a specific instance of [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor).</span></span>

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a><span data-ttu-id="60052-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60052-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60052-165">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="60052-165">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="60052-166">URI-Präfixe</span><span class="sxs-lookup"><span data-stu-id="60052-166">URI Prefixes</span></span>](uri-prefixes.md)
</dt> <dt>

[<span data-ttu-id="60052-167">Ressourcen-URIs</span><span class="sxs-lookup"><span data-stu-id="60052-167">Resource URIs</span></span>](resource-uris.md)
</dt> <dt>

[<span data-ttu-id="60052-168">Skripterstellung in Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="60052-168">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>
