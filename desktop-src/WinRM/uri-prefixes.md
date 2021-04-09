---
title: URI-Präfixe
description: Das Ressourcen-URI-Präfix ist abhängig vom XML-Schema, das die Ressource beschreibt, unterschiedlich.
ms.assetid: 47c32da6-98c9-4f66-82ac-647976127cb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e73de4d6d1762e87aa05e72b6cb6b3fbb228b80d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "103858538"
---
# <a name="uri-prefixes"></a><span data-ttu-id="f311d-103">URI-Präfixe</span><span class="sxs-lookup"><span data-stu-id="f311d-103">URI prefixes</span></span>

<span data-ttu-id="f311d-104">Das [*Ressourcen-URI*](windows-remote-management-glossary.md) -Präfix ist abhängig vom XML-Schema, das die Ressource beschreibt, unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="f311d-104">The [*resource URI*](windows-remote-management-glossary.md) prefix is different depending on which XML schema describes the resource.</span></span>

## <a name="prefixes"></a><span data-ttu-id="f311d-105">Präfixe</span><span class="sxs-lookup"><span data-stu-id="f311d-105">Prefixes</span></span>

<span data-ttu-id="f311d-106">Wenn Sie auf eine [*CIM*](windows-remote-management-glossary.md) 2,1-Klasse (z. b. [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile)) zugreifen, unterscheidet sich das Präfix des URI vom Präfix für eine CIM 2,9-Klasse, z. b. **CIM \_ admindomain**.</span><span class="sxs-lookup"><span data-stu-id="f311d-106">If you access a [*CIM*](windows-remote-management-glossary.md) 2.1 class, such as [**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), the prefix of the URI differs from the prefix for a CIM 2.9 class, such as **CIM\_AdminDomain**.</span></span> <span data-ttu-id="f311d-107">CIM 2,1-Klassen sind im Abschnitt [CIM-Klassen](/windows/desktop/WmiSdk/cimclas) von Windows-Verwaltungsinstrumentation (WMI) dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="f311d-107">CIM 2.1 classes are documented in the [CIM Classes](/windows/desktop/WmiSdk/cimclas) section of Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="f311d-108">Die meisten [WMI-Klassen](/windows/desktop/WmiSdk/wmi-classes) befinden sich im Stamm- **\\ CIMV2** -WMI-Namespace.</span><span class="sxs-lookup"><span data-stu-id="f311d-108">Most [WMI classes](/windows/desktop/WmiSdk/wmi-classes) are in the **root\\cimv2** WMI namespace.</span></span> <span data-ttu-id="f311d-109">Die Klassen für den Microsoft Intelligent Platform Management Interface ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider))-Anbieter befinden sich in der Stamm **\\ Hardware**.</span><span class="sxs-lookup"><span data-stu-id="f311d-109">Classes for the Microsoft Intelligent Platform Management Interface ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)) provider are in **root\\hardware**.</span></span>

<span data-ttu-id="f311d-110">Die folgende Liste enthält die Ressourcen-URI-Präfixe für diese Schemas:</span><span class="sxs-lookup"><span data-stu-id="f311d-110">The following list contains the resource URI prefixes for these schemas:</span></span>

-   <span data-ttu-id="f311d-111">WMI-oder CIM 2,1-Klassen im **root \\ CIMV2** -Namespace</span><span class="sxs-lookup"><span data-stu-id="f311d-111">WMI or CIM 2.1 classes in the **root\\cimv2** namespace</span></span>

    <span data-ttu-id="f311d-112">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"</span><span class="sxs-lookup"><span data-stu-id="f311d-112">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"</span></span>

-   <span data-ttu-id="f311d-113">CIM 2,9-Klassen oder IPMI-Klassen</span><span class="sxs-lookup"><span data-stu-id="f311d-113">CIM 2.9 classes or IPMI classes</span></span>

    <span data-ttu-id="f311d-114">"https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"</span><span class="sxs-lookup"><span data-stu-id="f311d-114">"https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"</span></span>

-   <span data-ttu-id="f311d-115">Alternative Methode für den Zugriff auf IPMI-Anbieter Klassen</span><span class="sxs-lookup"><span data-stu-id="f311d-115">Alternate way to access IPMI provider classes</span></span>

    <span data-ttu-id="f311d-116">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"</span><span class="sxs-lookup"><span data-stu-id="f311d-116">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"</span></span>

<span data-ttu-id="f311d-117">Weitere Informationen finden Sie unter [Ressourcen-URIs](resource-uris.md) und [URLPrefix](/windows/desktop/Http/urlprefix-strings)-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="f311d-117">For more information, see [Resource URIs](resource-uris.md) and [UrlPrefix Strings](/windows/desktop/Http/urlprefix-strings).</span></span> <span data-ttu-id="f311d-118">Weitere Informationen zum Erstellen eines URI für eine WMI-Klasse oder-Methode finden Sie unter [Windows-Remoteverwaltung und WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f311d-118">For more information about generating a URI for a WMI class or method, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

## <a name="prefix-aliases"></a><span data-ttu-id="f311d-119">Präfix Aliase</span><span class="sxs-lookup"><span data-stu-id="f311d-119">Prefix Aliases</span></span>

<span data-ttu-id="f311d-120">Ein Präfix-Alias ist eine Verknüpfung, die das lange Ressourcen-URI-Präfix darstellt.</span><span class="sxs-lookup"><span data-stu-id="f311d-120">A prefix alias is a shortcut that represents the long resource URI prefix.</span></span> <span data-ttu-id="f311d-121">Sie können auch Aliase in der **WinRM** -Befehlszeile verwenden.</span><span class="sxs-lookup"><span data-stu-id="f311d-121">You can also use aliases in the **Winrm** command-line.</span></span> <span data-ttu-id="f311d-122">Geben Sie **WinRM-Hilfe Aliase** ein, um eine Liste der verfügbaren Aliase anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f311d-122">To view a list of available aliases, type **Winrm help aliases**.</span></span>

<span data-ttu-id="f311d-123">Beachten Sie, dass ein Alias nicht innerhalb eines Endpunkt Verweises (EPR) verwendet werden kann, wenn ein Ressourcen-URI angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f311d-123">Be aware that an alias cannot be used inside an endpoint reference (EPR) when specifying a resource URI.</span></span> <span data-ttu-id="f311d-124">Windows-Remoteverwaltung kann den Alias nicht erweitern, wenn er in XML eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="f311d-124">Windows Remote Management is unable to expand the alias when it is embedded in XML.</span></span>

<span data-ttu-id="f311d-125">Im folgenden Codebeispiel wird der WinRM-Alias in einem EPR anstelle des gesamten Ressourcen-URI verwendet, der ist `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` .</span><span class="sxs-lookup"><span data-stu-id="f311d-125">In the following code example, the winrm alias is used in an EPR instead of the complete resource URI, which is `http://schemas.microsoft.com/wbem/wsman/1/config/Listener`.</span></span> <span data-ttu-id="f311d-126">In diesem Fall gibt WinRM einen Fehler zurück, der angibt, dass der Dienst die Anforderung nicht verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="f311d-126">In this case, WinRM returns an error that indicates the service cannot process the request.</span></span>


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



<span data-ttu-id="f311d-127">In der folgenden Liste sind die definierten Aliase und Ressourcen-URIs aufgeführt, deren Ersatz Sie ersetzen.</span><span class="sxs-lookup"><span data-stu-id="f311d-127">The following lists defined aliases and resource URIs for which they substitute.</span></span>

<dl> <dt>

<span data-ttu-id="f311d-128"><span id="wmi"></span><span id="WMI"></span>WMI</span><span class="sxs-lookup"><span data-stu-id="f311d-128"><span id="wmi"></span><span id="WMI"></span>wmi</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi`

</dd> <dt>

<span data-ttu-id="f311d-129"><span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2</span><span class="sxs-lookup"><span data-stu-id="f311d-129"><span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2`

</dd> <dt>

<span data-ttu-id="f311d-130"><span id="cimv2"></span><span id="CIMV2"></span>CIMV2</span><span class="sxs-lookup"><span data-stu-id="f311d-130"><span id="cimv2"></span><span id="CIMV2"></span>cimv2</span></span>
</dt> <dd>

`https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2`

</dd> <dt>

<span data-ttu-id="f311d-131"><span id="winrm"></span><span id="WINRM"></span>WinRM</span><span class="sxs-lookup"><span data-stu-id="f311d-131"><span id="winrm"></span><span id="WINRM"></span>winrm</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span data-ttu-id="f311d-132"><span id="wsman"></span><span id="WSMAN"></span>WSMAN</span><span class="sxs-lookup"><span data-stu-id="f311d-132"><span id="wsman"></span><span id="WSMAN"></span>wsman</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span data-ttu-id="f311d-133"><span id="shell"></span><span id="SHELL"></span>schel</span><span class="sxs-lookup"><span data-stu-id="f311d-133"><span id="shell"></span><span id="SHELL"></span>shell</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="f311d-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f311d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f311d-135">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="f311d-135">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="f311d-136">Windows-Remoteverwaltung und WMI</span><span class="sxs-lookup"><span data-stu-id="f311d-136">Windows Remote Management and WMI</span></span>](windows-remote-management-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="f311d-137">Ressourcen-URIs</span><span class="sxs-lookup"><span data-stu-id="f311d-137">Resource URIs</span></span>](resource-uris.md)
</dt> </dl>
