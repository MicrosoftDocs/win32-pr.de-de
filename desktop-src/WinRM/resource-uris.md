---
title: Ressourcen-URIs
description: Ein Ressourcen-URI ist ein Bezeichner für einen unterschiedlichen Typ von Verwaltungsvorgang oder Wert, der von Verwaltungsdiensten verwendet wird, die das WS-Management Protokoll implementieren.
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 665c73caf5cf636ab7f0a0162f488ff073917984
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516811"
---
# <a name="resource-uris"></a><span data-ttu-id="95b11-103">Ressourcen-URIs</span><span class="sxs-lookup"><span data-stu-id="95b11-103">Resource URIs</span></span>

<span data-ttu-id="95b11-104">Ein [*Ressourcen-URI*](windows-remote-management-glossary.md) ist ein Bezeichner für einen unterschiedlichen Typ von Verwaltungsvorgang oder Wert, der von Verwaltungsdiensten verwendet wird, die das WS-Management Protokoll implementieren.</span><span class="sxs-lookup"><span data-stu-id="95b11-104">A [*resource URI*](windows-remote-management-glossary.md) is an identifier for a distinct type of management operation or value used by management services that implement the WS-Management protocol.</span></span> <span data-ttu-id="95b11-105">Ein Verwaltungs Wert kann die Temperatur innerhalb eines Computers sein.</span><span class="sxs-lookup"><span data-stu-id="95b11-105">A management value could be the temperature inside a computer.</span></span> <span data-ttu-id="95b11-106">Ein Beispiel für einen Verwaltungsvorgang ist das Starten eines beendeten dienbes oder das Festlegen eines Benutzer Kontingents für das Datenträger Volume.</span><span class="sxs-lookup"><span data-stu-id="95b11-106">An example of a management operation is starting a stopped service or setting a disk volume user quota.</span></span>

## <a name="resource-uri-format"></a><span data-ttu-id="95b11-107">Ressourcen-URI-Format</span><span class="sxs-lookup"><span data-stu-id="95b11-107">Resource URI Format</span></span>

<span data-ttu-id="95b11-108">Ein URI besteht aus einem Präfix und einem Pfad zu einer Ressource, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="95b11-108">A URI consists of a prefix and a path to a resource as is shown in the following example:</span></span>

<span data-ttu-id="95b11-109">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"</span><span class="sxs-lookup"><span data-stu-id="95b11-109">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"</span></span>

<span data-ttu-id="95b11-110">Diese Schema Spezifikation gibt an, dass der URI auf Version 1 des offiziellen WS-Management Protokolls basiert und dass es sich bei der Ressource um einen [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) im \\ Namespace "root cimv2" des WMI-Repository handelt.</span><span class="sxs-lookup"><span data-stu-id="95b11-110">This schema specification indicates that the URI is based on version 1 of the official WS-Management protocol and that the resource is a [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in the "root\\cimv2" namespace of the WMI repository.</span></span> <span data-ttu-id="95b11-111">URI-Präfixe enthalten eine Schema Spezifikation, z. b. "Schemas.Microsoft.com/wbem/wsman/1/WMI", und einen bestimmten Ressourcentyp, z. b. **Win32 \_ LogicalDisk**.</span><span class="sxs-lookup"><span data-stu-id="95b11-111">URI prefixes contain a schema specification, such as "schemas.microsoft.com/wbem/wsman/1/wmi" and a specific type of resource, such as **Win32\_LogicalDisk**.</span></span> <span data-ttu-id="95b11-112">Weitere Informationen zum Identifizieren einer bestimmten Instanz einer WMI-Klasse finden Sie unter [Windows-Remoteverwaltung und WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="95b11-112">For more information about identifying a specific instance of a WMI class, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="95b11-113">Weitere Informationen finden Sie unter [URI-Präfixe](uri-prefixes.md).</span><span class="sxs-lookup"><span data-stu-id="95b11-113">For more information, see [URI Prefixes](uri-prefixes.md).</span></span>

## <a name="types-of-resource-uris"></a><span data-ttu-id="95b11-114">Typen von Ressourcen-URIs</span><span class="sxs-lookup"><span data-stu-id="95b11-114">Types of Resource URIs</span></span>

<span data-ttu-id="95b11-115">Während [*Windows-Verwaltungsinstrumentation (WMI)*](windows-remote-management-glossary.md) die primäre Quelle von Verwaltungsdaten für Windows-basierte Betriebssysteme ist, sind auch andere Quellen für das Verwaltungs Schema vorhanden.</span><span class="sxs-lookup"><span data-stu-id="95b11-115">While [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md) is the primary source of management data for Windows-based operating systems, other sources of management schema also exist.</span></span>

<span data-ttu-id="95b11-116">In der folgenden Liste werden verschiedene Typen von Ressourcen-URIs beschrieben, die von Windows-Remoteverwaltung verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="95b11-116">The following list describes several types of resource URIs used by Windows Remote Management:</span></span>

-   <span data-ttu-id="95b11-117">WMI-URIs</span><span class="sxs-lookup"><span data-stu-id="95b11-117">WMI URIs</span></span>

    <span data-ttu-id="95b11-118">Diese Gruppe von URIs stellt einen [*Common Information Model*](/windows/desktop/WmiSdk/gloss-c) Klassenpfad dar, der den Namespace und die Klasse enthält.</span><span class="sxs-lookup"><span data-stu-id="95b11-118">This group of URIs represent a [*Common Information Model*](/windows/desktop/WmiSdk/gloss-c) class path which includes namespace and class.</span></span>

    <span data-ttu-id="95b11-119">WMI-URIs können in verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="95b11-119">WMI URIs can be used in:</span></span>

    -   <span data-ttu-id="95b11-120">[**Sitzungs**](session.md) Methoden</span><span class="sxs-lookup"><span data-stu-id="95b11-120">[**Session**](session.md) methods</span></span>
    -   <span data-ttu-id="95b11-121">[**Iwsmansession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) -Methoden</span><span class="sxs-lookup"><span data-stu-id="95b11-121">[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) methods</span></span>
    -   <span data-ttu-id="95b11-122">[**WSMAN. kreateresourcelocator**](wsman-createresourcelocator.md) -Methode oder [**iwsman. kreateresourcelocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator) -Methode</span><span class="sxs-lookup"><span data-stu-id="95b11-122">[**WSMan.CreateResourceLocator**](wsman-createresourcelocator.md) or [**IWSMan.CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator) methods</span></span>
    -   <span data-ttu-id="95b11-123">[**ResourceLocator**](resourcelocator.md) -Methode oder [**iwsmanresourcelocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) -Methode</span><span class="sxs-lookup"><span data-stu-id="95b11-123">[**ResourceLocator**](resourcelocator.md) or [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) methods</span></span>

-   <span data-ttu-id="95b11-124">IPMI-URIs</span><span class="sxs-lookup"><span data-stu-id="95b11-124">IPMI URIs</span></span>

    <span data-ttu-id="95b11-125">Diese Gruppe von URIs stellt Branchenstandard-URIs dar, die auf CIM-Version 2,9 basieren.</span><span class="sxs-lookup"><span data-stu-id="95b11-125">This group of URIs represent industry standard URIs based upon CIM version 2.9.</span></span> <span data-ttu-id="95b11-126">IPMI-URIs können in den [**Sitzungs**](session.md) Methoden [**Get**](session-get.md), [**Put**](session-put.md), [**Enumerate**](session-enumerate.md) und [**aufrufen**](session-invoke.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95b11-126">IPMI URIs can be used in [**Session**](session.md) methods [**Get**](session-get.md), [**Put**](session-put.md), [**Enumerate**](session-enumerate.md) , and [**Invoke**](session-invoke.md).</span></span>

    <span data-ttu-id="95b11-127">z. B. https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd.</span><span class="sxs-lookup"><span data-stu-id="95b11-127">An example is https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd.</span></span> <span data-ttu-id="95b11-128">Diese Ressource wird gemäß dem [DMTF.org](https://www.dmtf.org/home) CIM-Schema definiert.</span><span class="sxs-lookup"><span data-stu-id="95b11-128">This resource is defined according to the [DMTF.org](https://www.dmtf.org/home) CIM schema.</span></span>

-   <span data-ttu-id="95b11-129">WinRM-Konfigurations-URIs</span><span class="sxs-lookup"><span data-stu-id="95b11-129">WinRM configuration URIs</span></span>

    <span data-ttu-id="95b11-130">Diese Gruppe von URIs sind Konfigurations Vorgänge für die WinRM-[*Listenerkonfiguration*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="95b11-130">This group of URIs are configuration operations for the WinRM [*listener*](windows-remote-management-glossary.md) configuration.</span></span>

    <span data-ttu-id="95b11-131"> https://schemas.microsoft.com/wbem/wsman/1/config/listener kann in den [**Sitzungs**](session.md) Methoden [**Get**](session-get.md), [**Put**](session-put.md), [**Create**](session-create.md), [**Delete**](session-delete.md)und [**Enumerate**](session-enumerate.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95b11-131">https://schemas.microsoft.com/wbem/wsman/1/config/listener can be used in [**Session**](session.md) methods [**Get**](session-get.md), [**Put**](session-put.md), [**Create**](session-create.md), [**Delete**](session-delete.md), and [**Enumerate**](session-enumerate.md).</span></span>

-   <span data-ttu-id="95b11-132">[*System Ereignisprotokoll*](windows-remote-management-glossary.md) -URIs (SEL)</span><span class="sxs-lookup"><span data-stu-id="95b11-132">[*System Event Log*](windows-remote-management-glossary.md) (SEL) URIs</span></span>

    <span data-ttu-id="95b11-133">Diese Gruppe von URIs abonniert Ereignis Sammler Ereignisse aus dem BMC.</span><span class="sxs-lookup"><span data-stu-id="95b11-133">This group of URIs subscribes to Event Collector events from the BMC.</span></span> <span data-ttu-id="95b11-134">Sie können diese Ereignisse mithilfe des Befehlszeilen Tools **wevtutil** abonnieren.</span><span class="sxs-lookup"><span data-stu-id="95b11-134">You can subscribe to these events using the **Wevtutil** command-line tool.</span></span> <span data-ttu-id="95b11-135">Weitere Informationen finden Sie unter https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.</span><span class="sxs-lookup"><span data-stu-id="95b11-135">For more information, see https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.</span></span>

## <a name="case-sensitivity"></a><span data-ttu-id="95b11-136">Groß- und Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="95b11-136">Case Sensitivity</span></span>

<span data-ttu-id="95b11-137">Das [*WMI-Plug-in*](windows-remote-management-glossary.md) behält die Groß-/Kleinschreibung des in einer Anforderung empfangenen Ressourcen-URI bei.</span><span class="sxs-lookup"><span data-stu-id="95b11-137">The [*WMI plug-in*](windows-remote-management-glossary.md) preserves the case of the resource URI received in a request.</span></span> <span data-ttu-id="95b11-138">Um die Interoperabilität mit anderen Implementierungen WS-Management Protokolls sicherzustellen, sollten Sie jedoch im Ressourcen-URI die richtige Groß-/Kleinschreibung für die angeforderte Ressource verwenden.</span><span class="sxs-lookup"><span data-stu-id="95b11-138">However, to ensure interoperability with other implementations of WS-Management protocol, use the correct case for the requested resource in resource URI.</span></span> <span data-ttu-id="95b11-139">Die richtige Groß-/Kleinschreibung ist die vom Ressourcenanbieter definierte Schreibweise.</span><span class="sxs-lookup"><span data-stu-id="95b11-139">The correct case is the spelling defined by the resource provider.</span></span>

<span data-ttu-id="95b11-140">Obwohl bei Ressourcen-URIs die Groß-/Kleinschreibung nicht beachtet werden muss, bewirkt XML- [*Fragment*](windows-remote-management-glossary.md)</span><span class="sxs-lookup"><span data-stu-id="95b11-140">While resource URIs do not require case-sensitivity, [*fragment*](windows-remote-management-glossary.md) XML does.</span></span> <span data-ttu-id="95b11-141">Ein Fragment gibt anstelle des gesamten Eigenschaften Satzes für eine Ressource nur eine Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="95b11-141">A fragment specifies just one property, rather than the entire set of properties for a resource.</span></span> <span data-ttu-id="95b11-142">Im Fall von WMI-Ressourcen Ruft die fragmentsyntax eine Eigenschaft aus einer Ressourcen Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="95b11-142">In the case of WMI resources, fragment syntax gets one property from a resource instance.</span></span> <span data-ttu-id="95b11-143">Wenn Sie z. b. nur die **Version** -Eigenschaft von [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) erhalten, muss ein Fragment verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95b11-143">For example, getting only the **Version** property from [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requires using a fragment.</span></span> <span data-ttu-id="95b11-144">Weitere Informationen zu Fragmenten finden Sie unter "Hinzufügen eines Selektor zu einem ResourceLocator-oder iwsmanresourcelocator-Objekt" in [Windows-Remoteverwaltung und WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="95b11-144">For more information about fragments, see "Adding a selector to a ResourceLocator or IWSManResourceLocator object" in [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="95b11-145">Nach den XML-und [*XPath*](windows-remote-management-glossary.md) -Standards erzwingt das [*WMI-Plug-in*](windows-remote-management-glossary.md) die Unterscheidung nach Groß-/Kleinschreibung für Fragmente und XML, die die Eingabeparameter für eine Methode definiert.</span><span class="sxs-lookup"><span data-stu-id="95b11-145">Following XML and [*XPath*](windows-remote-management-glossary.md) standards, the [*WMI plug-in*](windows-remote-management-glossary.md) enforces case-sensitivity for fragments and XML that defines the input parameters for a method.</span></span> <span data-ttu-id="95b11-146">Die Unterscheidung nach Groß-/Kleinschreibung ist für die Unterstützung von XPath 1.0/Level 1 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="95b11-146">Case-sensitivity is required to support the XPath 1.0/Level 1 standard.</span></span> <span data-ttu-id="95b11-147">Um WMI-Daten über WinRM zu erhalten, bedeutet die Unterscheidung nach Groß-/Kleinschreibung, dass die Namen von WMI-Klassen,-Eigenschaften und-Methoden mit der Groß-/Kleinschreibung des im WMI-Repository gefundenen namens</span><span class="sxs-lookup"><span data-stu-id="95b11-147">To get WMI data through WinRM, case-sensitivity means that the names of WMI classes, properties, and methods must match the case of the name found in the WMI repository.</span></span>

<span data-ttu-id="95b11-148">Weitere Informationen finden Sie unter [XPath-Syntax](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="95b11-148">For more information, see [XPath Syntax](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).</span></span>

## <a name="case-sensitivity-examples"></a><span data-ttu-id="95b11-149">Beispiele für die groß-</span><span class="sxs-lookup"><span data-stu-id="95b11-149">Case Sensitivity Examples</span></span>

<span data-ttu-id="95b11-150">Beispielsweise kann ein Skript, das die **\_ sicherheitsbeschreibungenschaft** aus einer Instanz der WMI- [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Klasse abruft, keine Großbuchstaben für die Namen im Fragmentpfad verwenden, sondern nur den URI.</span><span class="sxs-lookup"><span data-stu-id="95b11-150">For example, a script that obtains the **SECURITY\_DESCRIPTOR** property from an instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class cannot use upper-case for the names in the fragment path, only the URI.</span></span> <span data-ttu-id="95b11-151">Das WinRM- [*WMI-Plug-in*](windows-remote-management-glossary.md) gibt für das folgende VBScript-Beispiel einen Fehler zurück, da die für den **fragmentpath** angegebene XPath-XML-Datei nicht die richtige Groß-/Kleinschreibung verwendet.</span><span class="sxs-lookup"><span data-stu-id="95b11-151">The WinRM [*WMI plug-in*](windows-remote-management-glossary.md) returns an error for the following VBScript example because the XPath XML supplied for the **FragmentPath** does not use the correct case.</span></span> <span data-ttu-id="95b11-152">Im WMI-Repository ist die Klasse "Win32- \_ Dienst".</span><span class="sxs-lookup"><span data-stu-id="95b11-152">In the WMI repository, the class is spelled "Win32\_Service".</span></span>


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



<span data-ttu-id="95b11-153">Die folgende Version desselben Beispiels zeigt die korrekte Verwendung von Case für die Win32- [**\_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Klasse und die **Sicherheits \_ deskriptoreigenschaft** .</span><span class="sxs-lookup"><span data-stu-id="95b11-153">The following version of the same example shows the correct use of case for the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class and **SECURITY\_DESCRIPTOR** property.</span></span>


```VB
ResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_Service/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



## <a name="related-topics"></a><span data-ttu-id="95b11-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95b11-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95b11-155">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="95b11-155">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="95b11-156">Remote Hardware Verwaltung</span><span class="sxs-lookup"><span data-stu-id="95b11-156">Remote Hardware Management</span></span>](remote-hardware-management.md)
</dt> <dt>

[<span data-ttu-id="95b11-157">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="95b11-157">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 