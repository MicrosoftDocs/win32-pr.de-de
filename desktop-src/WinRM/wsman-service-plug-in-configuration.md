---
title: Konfiguration des WinRM-Dienst-Plug-ins
description: Ein Windows-Remoteverwaltung-Plug-in (WinRM) muss im WinRM-Katalog registriert sein, damit die Infrastruktur den Satz der verfügbaren Plug-ins und die von Ihnen unterstützten Ressourcen-URIs dynamisch ermitteln kann.
ms.assetid: d71cd244-3f10-40e3-a756-36cdf41b9cad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60bf618d71e55c6afd28de918198725895088559
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104316736"
---
# <a name="winrm-service-plug-in-configuration"></a><span data-ttu-id="8ae38-103">Konfiguration des WinRM-Dienst-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="8ae38-103">WinRM Service Plug-in Configuration</span></span>

<span data-ttu-id="8ae38-104">Ein Windows-Remoteverwaltung-Plug-in (WinRM) muss im WinRM-Katalog registriert sein, damit die Infrastruktur den Satz der verfügbaren Plug-ins und die von Ihnen unterstützten [*Ressourcen-URIs*](windows-remote-management-glossary.md) dynamisch ermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="8ae38-104">A Windows Remote Management (WinRM) plug-in must be registered in the WinRM catalog to enable the infrastructure to dynamically determine the set of available plug-ins and the [*resource URIs*](windows-remote-management-glossary.md) that they support.</span></span> <span data-ttu-id="8ae38-105">Alle [*Ressourcen-URIs*](windows-remote-management-glossary.md) für WinRM-Plug-Ins müssen dem Format entsprechen, das in RFC 3986 ( [https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt) ) definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8ae38-105">All [*resource URIs*](windows-remote-management-glossary.md) for WinRM plug-ins should conform to the format that is defined in RFC 3986 ([https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt)).</span></span> <span data-ttu-id="8ae38-106">Die Konfiguration erfolgt über den WinRM-Hauptdienst.</span><span class="sxs-lookup"><span data-stu-id="8ae38-106">Configuration is done through the main WinRM service.</span></span>

<span data-ttu-id="8ae38-107">Der folgende Befehl registriert eine Plug-in-Konfiguration beim WinRM-Dienst:</span><span class="sxs-lookup"><span data-stu-id="8ae38-107">The following command registers a plug-in configuration with the WinRM service:</span></span>

```console
winrm create http://schemas.microsoft.com/wbem/wsman/1/config/plugin?name=MyPlugIn -file:myplugin.xml
```

> [!NOTE]
> <span data-ttu-id="8ae38-108">Der WinRM-Dienst muss neu gestartet werden, um die neu registrierten Plug-Ins verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="8ae38-108">The WinRM service needs to be restarted to expose the newly registered plug-ins.</span></span>

<span data-ttu-id="8ae38-109">Die Plug-in-Konfiguration ist in XML angegeben.</span><span class="sxs-lookup"><span data-stu-id="8ae38-109">Plug-in configuration is specified in XML.</span></span> <span data-ttu-id="8ae38-110">Im Folgenden finden Sie ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="8ae38-110">The following is an example.</span></span>

```XML
<PlugInConfiguration xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
                     Name="MyPlugIn"
                     Filename="%systemroot%\system32\myplugin.dll" 
                     SDKVersion="1"
                     XmlRenderingType="text"
                     Architecture="64"
                     Enabled="true">

 <InitializationParameters>
  <Param Name="myParam1" Value="myValue1"/>
  <Param Name="myParam2" Value="myValue2"/>
 </InitializationParameters>

 <Resources>
  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri1" SupportsOptions="true" ExactMatch="false">
   <Capability Type="Get" SupportsFragment="true"/>
   <Capability Type="Put" SupportsFragment="true"/>
   <Capability Type="Create"/>
   <Capability Type="Delete"/>
   <Capability Type="Invoke"/>
   <Capability Type="Enumerate" SupportsFiltering="true"/>
  </Resource>

  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri2" SupportsOptions="false" ExactMatch="true">
   <Security Uri="https://schemas.MyCompany.com/MyUri2" Sddl="O:NSG:BAD:P(A;;GA;;;BA)"/>
   <Security Uri="https://schemas.MyCompany.com/MyUri2/MoreSpecific" Sddl="O:NSG:BAD:P(A;;GR;;;BA)" ExactMatch="true"/>
   <Capability Type="Shell"/>
  </Resource>
 </Resources>
</PlugInConfiguration>
```



<span data-ttu-id="8ae38-111">In der folgenden Liste werden die XML-Elemente ausführlicher beschrieben, und es folgt das als XSD angegebene Konfigurations Schema.</span><span class="sxs-lookup"><span data-stu-id="8ae38-111">The following list describes the XML elements in more detail and is followed by the configuration schema specified as an XSD.</span></span>

<dl> <dt>

<span data-ttu-id="8ae38-112"><span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**Pluginconfiguration** / **Operationsconfiguration**</span><span class="sxs-lookup"><span data-stu-id="8ae38-112"><span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration**/**OperationsConfiguration**</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-113">Gibt den Dateinamen des Vorgangs-Plug-ins an.</span><span class="sxs-lookup"><span data-stu-id="8ae38-113">Specifies the file name of the operations plug-in.</span></span> <span data-ttu-id="8ae38-114">Alle Umgebungsvariablen, die in diesen Eintrag eingefügt werden, werden im Kontext des Benutzers erweitert, wenn eine Anforderung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="8ae38-114">Any environment variables that are put in this entry will be expanded in the users' context when a request comes in.</span></span> <span data-ttu-id="8ae38-115">Jeder Benutzer kann über eine andere Version derselben Umgebungsvariablen verfügen, sodass jeder Benutzer ein anderes Plug-in haben könnte.</span><span class="sxs-lookup"><span data-stu-id="8ae38-115">Each user could have a different version of the same environment variable, so each user could end up with a different plug-in.</span></span> <span data-ttu-id="8ae38-116">Dieser Eintrag darf nicht leer sein und muss auf ein gültiges Plug-in zeigen.</span><span class="sxs-lookup"><span data-stu-id="8ae38-116">This entry cannot be blank and must point to a valid plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="8ae38-117"><span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**Pluginconfiguration** / **Name**</span><span class="sxs-lookup"><span data-stu-id="8ae38-117"><span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration**/**Name**</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-118">Gibt den anzeigen Amen an, der für das Plug-in verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ae38-118">Specifies the display name to use for the plug-in.</span></span> <span data-ttu-id="8ae38-119">Wenn vom Plug-in ein Fehler zurückgegeben wird, wird dieser Name in die Fehler-XML-Datei eingefügt, die an die Client Anwendung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8ae38-119">If an error is returned from the plug-in, this name will be put into the error XML that is returned to the client application.</span></span> <span data-ttu-id="8ae38-120">Der Name gilt für kein bestimmtes Gebietsschema.</span><span class="sxs-lookup"><span data-stu-id="8ae38-120">The name is not locale specific.</span></span>

</dd> <dt>

<span data-ttu-id="8ae38-121"><span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**Pluginconfiguration** / **Architektur**</span><span class="sxs-lookup"><span data-stu-id="8ae38-121"><span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration**/**Architecture**</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-122">Gibt an, ob das Operations-Plug-in 32-Bit oder 64-Bit ist.</span><span class="sxs-lookup"><span data-stu-id="8ae38-122">Specifies whether the operations plug-in is 32-bit or 64-bit.</span></span> <span data-ttu-id="8ae38-123">Wenn dieses Element nicht angegeben ist, wird der Wert standardmäßig auf x86-Systemen auf "32" und auf 64-Bit-Systemen auf "64" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-123">If this element is not specified, the value will default to "32" on x86 systems and to "64" on 64-bit systems.</span></span> <span data-ttu-id="8ae38-124">Für x86-Systeme ist der einzige gültige Wert "32".</span><span class="sxs-lookup"><span data-stu-id="8ae38-124">For x86 systems, the only valid value is "32".</span></span> <span data-ttu-id="8ae38-125">Wenn der Wert "32" auf einem 64-Bit-System ist, muss die WOW64-Umleitung beim Eingeben der **Dateiname** -Informationen berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-125">If the value is "32" on an 64-bit system, wow64 redirection needs to be taken into account when entering the **Filename** information.</span></span> <span data-ttu-id="8ae38-126">Das zugrunde liegende Dateisystem verwendet die WOW64-Umleitung zum Übersetzen von system32 in syswow64.</span><span class="sxs-lookup"><span data-stu-id="8ae38-126">The underlying file system will use wow64 redirection to translate system32 to syswow64.</span></span> <span data-ttu-id="8ae38-127">Wenn der **Dateiname** z. b. "% windir% \\ system32 \\myplugin.dll" und die **Architektur** den Wert "32" hat, befindet sich die tatsächliche Plug-in-Datei unter "% windir% \\ syswow64 \\myplugin.dll".</span><span class="sxs-lookup"><span data-stu-id="8ae38-127">For example, if **Filename** is "%windir%\\system32\\myplugin.dll" and **Architecture** is "32", the actual plug-in file is located at "%windir%\\syswow64\\myplugin.dll".</span></span>

</dd> <dt>

<span data-ttu-id="8ae38-128"><span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**Pluginconfiguration** / **Xmlrenderingtype**</span><span class="sxs-lookup"><span data-stu-id="8ae38-128"><span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration**/**XmlRenderingType**</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-129">Konfiguriert das Format, in dem XML an Plug-ins über das [**WSMAN- \_ Daten**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) Objekt übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="8ae38-129">Configures the format in which XML is passed to plug-ins through the [**WSMAN\_DATA**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) object.</span></span> <span data-ttu-id="8ae38-130">Folgende Dateitypen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="8ae38-130">The following types are available:</span></span>

<dl> <dt>

<span data-ttu-id="8ae38-131"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span><span class="sxs-lookup"><span data-stu-id="8ae38-131"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-132">Eingehende XML-Daten sind in der Text Struktur eines WSMAN- \_ \_ Datentyps enthalten \_ , der den XML-Code als **pcwstr** -Arbeitsspeicher Puffer darstellt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-132">Incoming XML data is contained in a WSMAN\_DATA\_TYPE\_TEXT structure, which represents the XML as a **PCWSTR** memory buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8ae38-133"><span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>XmlReader</span><span class="sxs-lookup"><span data-stu-id="8ae38-133"><span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>XMLReader</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-134">Eingehende XML-Daten sind in \_ der WS XML Reader-Struktur eines WSMAN- \_ Datentyps enthalten \_ , der \_ den XML-Code \_ als **XmlReader** -Objekt darstellt, das in der Header Datei "Webservices. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8ae38-134">Incoming XML data is contained in a WSMAN\_DATA\_TYPE\_WS\_XML\_READER structure, which represents the XML as an **XmlReader** object, which is defined in the WebServices.h header file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8ae38-135"><span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**Pluginconfiguration** / **Initializationxml**</span><span class="sxs-lookup"><span data-stu-id="8ae38-135"><span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration**/**InitializationXml**</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-136">Dieser Knoten ist optional und ermöglicht einem Plug-in das Konfigurieren zusätzlicher XML-Daten, die an die [**wsmanpluginstartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)-Methode übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-136">This node is optional and allows a plug-in to configure extra XML that will be passed in to the [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)method.</span></span> <span data-ttu-id="8ae38-137">Die meisten Plug-Ins benötigen diese zusätzlichen Informationen nicht. Wenn jedoch ein Plug-in in mehr als einem Szenario verwendet werden muss, das eine andere Lauf Zeit Semantik erfordert, gibt dieser XML-Code dem Plug-in die Flexibilität.</span><span class="sxs-lookup"><span data-stu-id="8ae38-137">Most plug-ins will not need this extra information, but if a plug-in needs to be used under more than one scenario that requires different run-time semantics, this XML will give the plug-in the flexibility to do this.</span></span>

</dd> <dt>

<span data-ttu-id="8ae38-138"><span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**Pluginconfiguration** / **Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="8ae38-138"><span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration**/**Resources**</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-139">Gibt eine Liste von [*Ressourcen-URIs*](windows-remote-management-glossary.md)an, die dieses Plug-in unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-139">Specifies a list of [*resource URIs*](windows-remote-management-glossary.md)that this plug-in supports.</span></span> <span data-ttu-id="8ae38-140">Mindestens ein **resourceUri**-Eintrag muss angegeben werden. Andernfalls wird der XML-Code zurückgewiesen.</span><span class="sxs-lookup"><span data-stu-id="8ae38-140">At least one **ResourceUri** entry must be specified; otherwise, the XML will be rejected.</span></span>

</dd> <dt>

<span data-ttu-id="8ae38-141"><span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**Pluginconfiguration** / **Ressourcen** / **Ressource**</span><span class="sxs-lookup"><span data-stu-id="8ae38-141"><span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration**/**Resources**/**Resource**</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-142">Stellt eine einzelne [*Ressourcen-URI*](windows-remote-management-glossary.md)-Konfiguration dar.</span><span class="sxs-lookup"><span data-stu-id="8ae38-142">Represents a single [*resource URI*](windows-remote-management-glossary.md)configuration.</span></span>

> [!Note]  
> <span data-ttu-id="8ae38-143">Das **supportsoptions**-Attribut kann auf "false" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-143">The **SupportsOptions** attribute can be set to false.</span></span> <span data-ttu-id="8ae38-144">Wenn **supportsoptions** auf false festgelegt ist, wird dieses Attribut nicht aufgelistet, wenn die Ressource aufgezählt wird.</span><span class="sxs-lookup"><span data-stu-id="8ae38-144">If **SupportsOptions** is set to false, this attribute is not listed when the resource is enumerated.</span></span>

 

</dd> <dt>

<span data-ttu-id="8ae38-145"><span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**Pluginconfiguration** / **Ressourcen** / **Ressource** / **ResourceUri**</span><span class="sxs-lookup"><span data-stu-id="8ae38-145"><span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration**/**Resources**/**Resource**/**ResourceUri**</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-146">Gibt einen einzelnen [*Ressourcen-URI*](windows-remote-management-glossary.md) entweder vollständig oder als partielle Vergleichs Zeichenfolge basierend auf dem **exactMatch** -Attribut an.</span><span class="sxs-lookup"><span data-stu-id="8ae38-146">Specifies a single [*resource URI*](windows-remote-management-glossary.md) either in full or as a partial match string based on the **ExactMatch** attribute.</span></span> <span data-ttu-id="8ae38-147">Wenn " **exactMatch** " nicht vorhanden ist, wird standardmäßig " **false**" verwendet. Dies bedeutet, dass der WinRM-SOAP-Prozessor eine partielle Entsprechung zum Anfang des *Ressourcen-URI* findet und eine Entsprechung an das Plug-in übergibt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-147">If **ExactMatch** is not present, it defaults to **False**, which means the WinRM SOAP processor will do a partial match to the start of the *resource URI* and, if there is a match, pass it to the plug-in.</span></span> <span data-ttu-id="8ae38-148">Das **supportsoptions** -Attribut kann angegeben werden, wenn für diesen *Ressourcen-URI* alle Optionen übermittelt werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="8ae38-148">The **SupportsOptions** attribute can be specified if this *resource URI* is allowed to have any options passed in.</span></span> <span data-ttu-id="8ae38-149">Standardmäßig werden keine Optionen unterstützt, und wenn in der Client Anforderung eine vorhanden ist, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ae38-149">By default, no options are supported, and if any are present in the client request, an error will be returned.</span></span> <span data-ttu-id="8ae38-150">Wenn Optionen vom Plug-in unterstützt werden, ist es wichtig, dass das Plug-in den korrekten Fehler zurückgibt, wenn eine Option vorhanden ist, die das Plug-in nicht versteht, wenn das **MustUnderstand** -Flag auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8ae38-150">If options are supported by the plug-in, it is important that the plug-in returns the correct error if an option is present that the plug-in does not understand when the **mustUnderstand** flag is set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="8ae38-151"><span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**Pluginconfiguration** / **Ressourcen** / **Ressource** / **Funktion**</span><span class="sxs-lookup"><span data-stu-id="8ae38-151"><span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration**/**Resources**/**Resource**/**Capability**</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-152">Gibt eine Funktion an, die für diesen [*Ressourcen-URI*](windows-remote-management-glossary.md)verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8ae38-152">Specifies a capability that is available on this [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="8ae38-153">Es gibt einen Eintrag für jeden Vorgangstyp, den er unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-153">There will be one entry for each type of operation that it supports.</span></span> <span data-ttu-id="8ae38-154">Die folgenden Optionen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="8ae38-154">The following options are available:</span></span>

<dl> <dt>

<span data-ttu-id="8ae38-155"><span id="Get"></span><span id="get"></span><span id="GET"></span>Erhalten</span><span class="sxs-lookup"><span data-stu-id="8ae38-155"><span id="Get"></span><span id="get"></span><span id="GET"></span>Get</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-156">Get-Vorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-156">Get operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="8ae38-157">Das **supportfragment** -Attribut wird verwendet, wenn der Get-Vorgang das Konzept unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-157">The **SupportFragment** attribute is used if the get operation supports the concept.</span></span> <span data-ttu-id="8ae38-158">Das **supportfiltering** -Attribut ist ungültig und sollte auf false festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-158">The **SupportFiltering** attribute is not valid and should be set to false.</span></span> <span data-ttu-id="8ae38-159">Diese Funktion ist für einen Ressourcen- *URI* ungültig, wenn Shellvorgänge ebenfalls unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-159">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="8ae38-160"><span id="Put"></span><span id="put"></span><span id="PUT"></span>Stellte</span><span class="sxs-lookup"><span data-stu-id="8ae38-160"><span id="Put"></span><span id="put"></span><span id="PUT"></span>Put</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-161">Put-Vorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-161">Put operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="8ae38-162">Das **supportfragment**-Attribut wird verwendet, wenn der Put-Vorgang das Konzept unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-162">The **SupportFragment** attribute is used if the put operation supports the concept.</span></span> <span data-ttu-id="8ae38-163">Das **supportfiltering** -Attribut ist ungültig und sollte auf **false** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-163">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="8ae38-164">Diese Funktion ist für einen Ressourcen- *URI* ungültig, wenn Shellvorgänge ebenfalls unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-164">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="8ae38-165"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>Stelle</span><span class="sxs-lookup"><span data-stu-id="8ae38-165"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>Create</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-166">Erstellungs Vorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-166">Create operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="8ae38-167">Das **supportfragment** -Attribut wird verwendet, wenn der Create-Vorgang das Konzept unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-167">The **SupportFragment** attribute is used if the create operation supports the concept.</span></span> <span data-ttu-id="8ae38-168">Das **supportfiltering** -Attribut ist ungültig und sollte auf **false** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-168">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="8ae38-169">Diese Funktion ist für einen Ressourcen- *URI* ungültig, wenn Shellvorgänge ebenfalls unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-169">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="8ae38-170"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Lösch</span><span class="sxs-lookup"><span data-stu-id="8ae38-170"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Delete</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-171">Löschvorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-171">Delete operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="8ae38-172">Das **supportfragment** -Attribut wird verwendet, wenn der DELETE-Vorgang das Konzept unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-172">The **SupportFragment** attribute is used if the delete operation supports the concept.</span></span> <span data-ttu-id="8ae38-173">Das **supportfiltering** -Attribut ist ungültig und sollte auf **false** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-173">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="8ae38-174">Diese Funktion ist für einen Ressourcen- *URI* ungültig, wenn Shellvorgänge ebenfalls unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-174">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="8ae38-175"><span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Blaze</span><span class="sxs-lookup"><span data-stu-id="8ae38-175"><span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Invoke</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-176">Startvorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-176">Invoke operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="8ae38-177">Das **supportfragment** -Attribut wird für Aufruf Vorgänge nicht unterstützt und sollte auf false festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-177">The **SupportFragment** attribute is not supported for invoke operations and should be set to false.</span></span> <span data-ttu-id="8ae38-178">Das **supportfiltering** -Attribut ist ungültig und sollte auf **false** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-178">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="8ae38-179">Diese Funktion ist für einen Ressourcen- *URI* ungültig, wenn Shellvorgänge ebenfalls unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-179">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="8ae38-180"><span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Auflisten</span><span class="sxs-lookup"><span data-stu-id="8ae38-180"><span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Enumerate</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-181">Enumeringvorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-181">Enumerate operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="8ae38-182">Das **supportfragment** -Attribut wird für auflisten-Vorgänge nicht unterstützt und sollte auf **false** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-182">The **SupportFragment** attribute is not supported for enumerate operations and should be set to **False**.</span></span> <span data-ttu-id="8ae38-183">Das **supportfiltering** -Attribut ist gültig, und wenn das Plug-in das Filtern unterstützt, sollte dieses Attribut auf " **true**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-183">The **SupportFiltering** attribute is valid, and if the plug-in supports filtering this attribute should be set to **True**.</span></span> <span data-ttu-id="8ae38-184">Diese Funktion ist für einen Ressourcen- *URI* ungültig, wenn Shellvorgänge ebenfalls unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-184">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="8ae38-185"><span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Abonnieren</span><span class="sxs-lookup"><span data-stu-id="8ae38-185"><span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Subscribe</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-186">Abonnement Vorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-186">Subscribe operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="8ae38-187">Das **supportfragment** -Attribut wird für abonnieren-Vorgänge nicht unterstützt und sollte auf **false** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-187">The **SupportFragment** attribute is not supported for subscribe operations and should be set to **False**.</span></span> <span data-ttu-id="8ae38-188">Das **supportfiltering** -Attribut ist ungültig und sollte auf **false** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-188">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="8ae38-189">Diese Funktion ist für einen Ressourcen- *URI* ungültig, wenn Shellvorgänge ebenfalls unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-189">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="8ae38-190"><span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Schel</span><span class="sxs-lookup"><span data-stu-id="8ae38-190"><span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Shell</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-191">Shellvorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-191">Shell operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="8ae38-192">Das **supportfragment** -Attribut wird für Shellvorgänge nicht unterstützt und sollte auf **false** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-192">The **SupportFragment** attribute is not supported for shell operations and should be set to **False**.</span></span> <span data-ttu-id="8ae38-193">Das **supportfiltering** -Attribut ist ungültig und sollte auf **false** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae38-193">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="8ae38-194">Diese Funktion ist für einen Ressourcen- *URI* nicht gültig, wenn eine andere Vorgangs Funktion ebenfalls unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8ae38-194">This capability is not valid for a *resource URI* if any other operation capability is also supported.</span></span> <span data-ttu-id="8ae38-195">Wenn eine shellvorgangsaktionen für einen *Ressourcen-URI* konfiguriert ist, werden Get-, Put-, CREATE-, DELETE-, Aufruf-und auflisten-Vorgänge intern im WinRM-Dienst verarbeitet, um Shells zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="8ae38-195">If a shell operation capability is configured for a *resource URI*, then get, put, create, delete, invoke, and enumerate operations are processed internally within the WinRm service to manage shells.</span></span> <span data-ttu-id="8ae38-196">Folglich kann das Plug-in nicht mit den Vorgängen selbst umgehen.</span><span class="sxs-lookup"><span data-stu-id="8ae38-196">As a result, the plug-in cannot deal with the operations itself.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8ae38-197"><span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**Pluginconfiguration** / **Ressourcen** / **Ressource** / **Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="8ae38-197"><span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration**/**Resources**/**Resource**/**Security**</span></span>
</dt> <dd>

<span data-ttu-id="8ae38-198">Dieses Element definiert die Sicherheits Beschreibung (über das **SDDL** -Attribut), die angewendet werden soll, um den Zugriff auf einen bestimmten [*Ressourcen-URI*](windows-remote-management-glossary.md) zu bestimmen (über das **URI** -Attribut).</span><span class="sxs-lookup"><span data-stu-id="8ae38-198">This element defines the security descriptor (via the **Sddl** attribute) that should be applied to determine access to a particular [*resource URI*](windows-remote-management-glossary.md) (via the **Uri** attribute).</span></span> <span data-ttu-id="8ae38-199">Wenn **exactMatch** nicht vorhanden ist, wird das **Sicherheits** Element standardmäßig auf **false** festgelegt. Dies bedeutet, dass die **SDDL** für alle *Ressourcen-URIs* gilt, die **URI** als Präfix freigeben.</span><span class="sxs-lookup"><span data-stu-id="8ae38-199">If **ExactMatch** is not present, the **Security** element defaults to **False**, which means that the **Sddl** applies to all *resource URIs* that share **Uri** as a prefix.</span></span> <span data-ttu-id="8ae38-200">Wenn **exactMatch** auf true festgelegt ist, gilt die **SDDL** nur für den angegebenen **URI** .</span><span class="sxs-lookup"><span data-stu-id="8ae38-200">If **ExactMatch** is set to true, the **Sddl** applies only to the exact **Uri** specified.</span></span> <span data-ttu-id="8ae38-201">Wenn mehrere **Sicherheits** Einträge vorhanden sind, die auf einen bestimmten *Ressourcen-URIs* angewendet werden können, wird der entsprechende **SDDL** mit der längsten Präfix Übereinstimmung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-201">If there are multiple **Security** entries that could apply to a particular *resource URIs*, the longest-prefix match is used to determine the appropriate **Sddl**.</span></span> <span data-ttu-id="8ae38-202">Wenn ein **URI** -Eintrag mit dem längsten Präfix vorhanden ist, wird er immer als entsprechendes Sicherheitselement ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="8ae38-202">As a result of the longest-prefix match, if an exact-match **Uri** entry exists, it will always be chosen as the appropriate Security element.</span></span>

</dd> </dl>

<span data-ttu-id="8ae38-203">Im folgenden wird das Plug-in-Konfigurations Schema als XSD angegeben.</span><span class="sxs-lookup"><span data-stu-id="8ae38-203">The following is the plug-in configuration schema specified as an XSD.</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<xs:schema attributeFormDefault="unqualified" 
           elementFormDefault="qualified" 
           targetNamespace="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns:xs="https://www.w3.org/2001/XMLSchema">
 <xs:element name="PlugInConfiguration">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="InitializationParameters" minOccurs="0" maxOccurs="1">
     <xs:complexType>
      <xs:sequence>
       <xs:element name="Param">
        <xs:complexType>
         <xs:sequence></xs:sequence>
         <xs:attribute name="Name" type="xs:string"/>
         <xs:attribute name="Value" type="xs:string"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
    <xs:element name="Resources">
     <xs:complexType>
      <xs:sequence>
       <xs:element minOccurs="1" maxOccurs="unbounded" name="Resource">
        <xs:complexType>
         <xs:sequence>
          <xs:element name="Capability" minOccurs="1" maxOccurs="unbounded">
           <xs:complexType>
            <xs:simpleContent>
             <xs:extension base="ResourceCapabilityType">
              <xs:attribute name="SupportsFragment" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="SupportsFiltering" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="Type" type="ResourceCapabilityType"/>
             </xs:extension>
            </xs:simpleContent>
           </xs:complexType>
          </xs:element>
          <xs:element name="Security" minOccurs="0" maxOccurs="unbounded">
           <xs:complexType>
            <xs:sequence></xs:sequence>
            <xs:attribute name="Uri" type="xs:string"/>
            <xs:attribute name="Sddl" type="xs:string"/>
            <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
           </xs:complexType>
          </xs:element>
         </xs:sequence>
         <xs:attribute name="ResourceUri" type="xs:string"/>
         <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
         <xs:attribute name="SupportOptions" type="xs:boolean" use="optional" default="false"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
   </xs:sequence>
   <xs:attribute name="Filename" type="xs:token"/>
   <xs:attribute name="SDKVersion" type="xs:unsignedInt"/>
   <xs:attribute name="Name" type="xs:string"/>
   <xs:attribute name="XmlRenderingType" type="XmlRenderingTypeType" use="optional" default="text"/>
   <!--Architecture will default to 32 on x86 systems; 64 on 64-bit systems.-->
   <xs:attribute name="Architecture" type="ArchitectureType" use="optional" default="32"/>
  </xs:complexType>
 </xs:element>
 <xs:simpleType name="ResourceCapabilityType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="Get"/>
   <xs:enumeration value="Put"/>
   <xs:enumeration value="Create"/>
   <xs:enumeration value="Delete"/>
   <xs:enumeration value="Invoke"/>
   <xs:enumeration value="Enumerate"/>
   <xs:enumeration value="Subscribe"/>
   <xs:enumeration value="Shell"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="XmlRenderingTypeType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="text"/>
   <xs:enumeration value="XmlReader"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="ArchitectureType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="32"/>
   <xs:enumeration value="64"/>
  </xs:restriction>
 </xs:simpleType>
</xs:schema>
```

 

 




