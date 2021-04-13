---
title: Ermittlung von DMTF-Profilen durch Zuordnungs Durchlauf
description: Eine Schlüsselkomponente der WMI-Infrastruktur (Windows-Verwaltungsinstrumentation) ist ein objektorientiertes Modell der verwaltbaren Entitäten in einem System.
ms.assetid: 21e03d78-bce1-471e-a826-e676d32990ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776b3f5883075ddf549330c422efec558195c8fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104391122"
---
# <a name="dmtf-profile-discovery-through-association-traversal"></a><span data-ttu-id="6b264-103">Ermittlung von DMTF-Profilen durch Zuordnungs Durchlauf</span><span class="sxs-lookup"><span data-stu-id="6b264-103">DMTF Profile Discovery Through Association Traversal</span></span>

<span data-ttu-id="6b264-104">Eine Schlüsselkomponente der WMI-Infrastruktur (Windows-Verwaltungsinstrumentation) ist ein objektorientiertes Modell der verwaltbaren Entitäten in einem System.</span><span class="sxs-lookup"><span data-stu-id="6b264-104">A key component of the Windows Management Instrumentation (WMI) infrastructure is an object-oriented model of the manageable entities in a system.</span></span> <span data-ttu-id="6b264-105">Das Modell entspricht einem Standard, der vom Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) verwaltet wird, und wird als Common Information Model (CIM) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6b264-105">The model conforms to a standard maintained by the Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) and is known as the Common Information Model (CIM).</span></span> <span data-ttu-id="6b264-106">Einige Klassen im Modell, z. b. [CIM \_ DataFile](../cimwin32prov/cim-datafile.md) oder [Win32 \_ Process](../cimwin32prov/win32-process.md), entsprechen direkt verwaltbaren Entitäten.</span><span class="sxs-lookup"><span data-stu-id="6b264-106">Some classes in the model, such as [CIM\_DataFile](../cimwin32prov/cim-datafile.md) or [Win32\_Process](../cimwin32prov/win32-process.md), correspond directly to manageable entities.</span></span> <span data-ttu-id="6b264-107">Andere Klassen im Modell, z. b. [Win32- \_ Systemdienste](../cimwin32prov/win32-systemservices.md), stellen Beziehungen zwischen verwaltbaren Entitäten dar.</span><span class="sxs-lookup"><span data-stu-id="6b264-107">Other classes in the model, such as [Win32\_SystemServices](../cimwin32prov/win32-systemservices.md), represent relationships between manageable entities.</span></span> <span data-ttu-id="6b264-108">Diese Beziehungs Modellierungs Klassen werden als Zuordnungs Klassen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6b264-108">These relationship-modeling classes are known as Association classes.</span></span>

<span data-ttu-id="6b264-109">Mithilfe der WMI-spezifischen Abfragesprache (WQL) können Sie Instanzen von Klassen abrufen, die verwaltbare Entitäten oder Instanzen von Zuordnungs Klassen darstellen.</span><span class="sxs-lookup"><span data-stu-id="6b264-109">Using the WMI-specific query language, WQL, you can retrieve instances of classes that represent manageable entities or instances of Association classes.</span></span> <span data-ttu-id="6b264-110">WQL ist jedoch Implementierungs spezifisch.</span><span class="sxs-lookup"><span data-stu-id="6b264-110">But WQL is implementation specific.</span></span> <span data-ttu-id="6b264-111">Dies funktioniert nur mit der Windows-Implementierung des DMTF-Standards (WMI).</span><span class="sxs-lookup"><span data-stu-id="6b264-111">It works only with the Windows implementation of the DMTF standard (WMI).</span></span> <span data-ttu-id="6b264-112">Außerdem ist die WQL-Syntax zum Abrufen von Zuordnungs Klassen recht kompliziert.</span><span class="sxs-lookup"><span data-stu-id="6b264-112">In addition, the WQL syntax for retrieving Association classes is rather complicated.</span></span>

<span data-ttu-id="6b264-113">Die Windows-Remoteverwaltung-Infrastruktur (WinRM) bietet eine hervorragende Möglichkeit, die Funktionalität von WMI zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="6b264-113">The Windows Remote Management (WinRM) infrastructure provides an excellent way to leverage the functionality of WMI.</span></span> <span data-ttu-id="6b264-114">In frühen Versionen von WinRM mussten WQL zum Abrufen von Instanzen von Zuordnungs Klassen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b264-114">Early versions of WinRM had to use WQL to retrieve instances of Association classes.</span></span> <span data-ttu-id="6b264-115">WinRM 2,0 umfasst ein neues Feature, das als DMTF-Profil Ermittlung über Association Traversal bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="6b264-115">WinRM 2.0 includes a new feature known as DMTF profile discovery through association traversal.</span></span> <span data-ttu-id="6b264-116">Der Zuordnungs Durchlauf ermöglicht einem Benutzer von WinRM das Abrufen von Instanzen von Zuordnungs Klassen mithilfe eines Standardfilter Mechanismus, dem associationfilter-Dialekt, der in der DMTF-CIM-Bindungs Spezifikation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="6b264-116">Association traversal enables a user of WinRM to retrieve instances of Association classes by using a standard filtering mechanism, the AssociationFilter dialect, defined in the DMTF CIM binding specification.</span></span> <span data-ttu-id="6b264-117">Weitere Informationen zu Association Traversal finden Sie in der WS-Management CIM-Bindungs Spezifikation ( [https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man) ).</span><span class="sxs-lookup"><span data-stu-id="6b264-117">For more information on association traversal, see the WS-Management CIM Binding specification ([https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man)).</span></span>

<span data-ttu-id="6b264-118">Das WinRM-Hilfsprogramm bietet einen einfachen Mechanismus zum Durchlaufen der entsprechenden Zuordnung und zum Abrufen eines Geräte Profils.</span><span class="sxs-lookup"><span data-stu-id="6b264-118">The winrm utility provides a simple mechanism to traverse through the appropriate association and retrieve a device profile.</span></span>

## <a name="configuration-implementation-details"></a><span data-ttu-id="6b264-119">Details zur Konfigurations Implementierung</span><span class="sxs-lookup"><span data-stu-id="6b264-119">Configuration Implementation Details</span></span>

<span data-ttu-id="6b264-120">Das WinRM-Hilfsprogramm unterstützt jetzt einen Dialekt für die Zuordnungs Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6b264-120">The winrm utility now supports a dialect for the association request.</span></span> <span data-ttu-id="6b264-121">Entweder der URI oder der Alias kann mit dem WinRM-Hilfsprogramm angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6b264-121">Either the URI or the alias can be specified using the winrm utility.</span></span>



| <span data-ttu-id="6b264-122">Alias</span><span class="sxs-lookup"><span data-stu-id="6b264-122">Alias</span></span>       | <span data-ttu-id="6b264-123">URI</span><span class="sxs-lookup"><span data-stu-id="6b264-123">URI</span></span>                                                               |
|-------------|-------------------------------------------------------------------|
| <span data-ttu-id="6b264-124">Korrelation</span><span class="sxs-lookup"><span data-stu-id="6b264-124">association</span></span> | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a><span data-ttu-id="6b264-125">Abrufen von Instanzen einer Association-Klasse mithilfe des associationfilter-Dialekts</span><span class="sxs-lookup"><span data-stu-id="6b264-125">Retrieving Instances of an Association Class by Using the AssociationFilter Dialect</span></span>

<span data-ttu-id="6b264-126">Das WinRM-Hilfsprogramm kann WMI-Zuordnungs Klassen Instanzen einer bestimmten Quell Instanz abrufen.</span><span class="sxs-lookup"><span data-stu-id="6b264-126">The winrm utility can retrieve WMI association class instances of a particular source instance.</span></span> <span data-ttu-id="6b264-127">Der folgende Befehl veranschaulicht, wie das WinRM-Hilfsprogramm verwendet wird, um Instanzen von [Win32- \_ Dienst](../cimwin32prov/win32-service.md) Zuordnungs Klassen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6b264-127">The following command demonstrates how to use the winrm utility to retrieve instances of [Win32\_Service](../cimwin32prov/win32-service.md) association classes.</span></span> <span data-ttu-id="6b264-128">Der Switch "-Zuordnungen" muss verwendet werden, um Zuordnungs Klassen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="6b264-128">The switch "-associations" must be used to return association classes.</span></span>

<span data-ttu-id="6b264-129">**WinRM auflisten wmicimv2/ \* -Dialekt: Association-Zuordnungen-Filter: {Object = Win32 \_ Service? Name = WinRM; resultclassname = Win32 \_ dependentservice; Role = Dependent}**</span><span class="sxs-lookup"><span data-stu-id="6b264-129">**winrm enumerate wmicimv2/\* -dialect:association -associations -filter:{object=win32\_service?name=winrm;resultclassname=win32\_dependentservice;role=dependent}**</span></span>

<span data-ttu-id="6b264-130">Der folgende textbasierte Code Ausschnitt ist die Ausgabe des obigen Befehls:</span><span class="sxs-lookup"><span data-stu-id="6b264-130">The following text-based snippet is the output of the above command:</span></span>

``` syntax
Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = RpcSs
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null

Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_SystemDriver
            SelectorSet
                Selector: Name = HTTP
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null
```

## <a name="retrieving-instances-of-an-associated-class-by-using-the-associationfilter-dialect"></a><span data-ttu-id="6b264-131">Abrufen von Instanzen einer zugeordneten Klasse mithilfe des associationfilter-Dialekts</span><span class="sxs-lookup"><span data-stu-id="6b264-131">Retrieving Instances of an Associated Class by Using the AssociationFilter Dialect</span></span>

<span data-ttu-id="6b264-132">Mit dem WinRM-Hilfsprogramm können WMI-Klassen Instanzen abgerufen werden, die einer bestimmten Quell Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6b264-132">The winrm utility can retrieve WMI class instances that are associated with a particular source instance.</span></span> <span data-ttu-id="6b264-133">Der folgende Befehl veranschaulicht, wie das WinRM-Hilfsprogramm verwendet wird, um Instanzen von zugeordneten [Win32- \_ Dienst](../cimwin32prov/win32-service.md) Klassen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6b264-133">The following command demonstrates how to use the winrm utility to retrieve instances of [Win32\_Service](../cimwin32prov/win32-service.md) associated classes.</span></span>

<span data-ttu-id="6b264-134">**WinRM auflisten wmicimv2/ \* -Dialekt: Association-Filter: {Object = Win32 \_ Service? Name = WinRM; associationclassname = Win32 \_ dependentservice; resultclassname = Win32 \_ Service; RESULTROLE = Vorgänger; Role = Dependent}**</span><span class="sxs-lookup"><span data-stu-id="6b264-134">**winrm enumerate wmicimv2/\* -dialect:association -filter:{object=win32\_service?name=winrm;associationclassname=win32\_dependentservice;resultclassname=win32\_service;resultrole=antecedent;role=dependent}**</span></span>

<span data-ttu-id="6b264-135">Der folgende textbasierte Code Ausschnitt ist die Ausgabe des obigen Befehls:</span><span class="sxs-lookup"><span data-stu-id="6b264-135">The following text-based snippet is the output of the above command:</span></span>

``` syntax
Win32_Service
    AcceptPause = false
    AcceptStop = false
    Caption = Remote Procedure Call (RPC)
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = The RPCSS service is the Service Control Manager for COM and DCOM servers. It performs object activations requests, object exporter resolutions and distributed garbage collection for COM and DCOM servers. If this service is stopped or disabled, programs using COM or DCOM will not function properly. It is strongly recommended that you have the RPCSS service running DesktopInteract = false
    DisplayName = Remote Procedure Call (RPC)
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = RpcSs
    PathName = C:\Windows\system32\svchost.exe -k rpcss
    ProcessId = 716
    ServiceSpecificExitCode = 0
    ServiceType = Share Process
    Started = true
    StartMode = Auto
    StartName = NT AUTHORITY\NetworkService
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = myComputer
    TagId = 0
    WaitHint = 0
```

 

 