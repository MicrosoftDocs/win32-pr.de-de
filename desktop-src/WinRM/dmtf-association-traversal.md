---
title: DMTF-Profilermittlung durch Zuordnungsdurchlauf
description: Eine wichtige Komponente der WMI-Infrastruktur (Windows Management Instrumentation) ist ein objektorientiertes Modell der verwaltbaren Entitäten in einem System.
ms.assetid: 21e03d78-bce1-471e-a826-e676d32990ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f49d1433d8263dff2c1d50007f9aa0daf1573c09ebc8d7a513eda658c51997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643150"
---
# <a name="dmtf-profile-discovery-through-association-traversal"></a>DMTF-Profilermittlung durch Zuordnungsdurchlauf

Eine wichtige Komponente der WMI-Infrastruktur (Windows Management Instrumentation) ist ein objektorientiertes Modell der verwaltbaren Entitäten in einem System. Das Modell entspricht einem Standard, der von der Desktop Management Task Force[(DMTF)](https://www.dmtf.org/standards/wsman)verwaltet wird und als Common Information Model (CIM) bekannt ist. Einige Klassen im Modell, z. B. [CIM \_ DataFile](../cimwin32prov/cim-datafile.md) oder [Win32 \_ Process,](../cimwin32prov/win32-process.md)entsprechen direkt verwaltbaren Entitäten. Andere Klassen im Modell, z. B. [Win32 \_ SystemServices,](../cimwin32prov/win32-systemservices.md)stellen Beziehungen zwischen verwaltbaren Entitäten dar. Diese Beziehungsmodellierungsklassen werden als Zuordnungsklassen bezeichnet.

Mithilfe der WMI-spezifischen Abfragesprache WQL können Sie Instanzen von Klassen abrufen, die verwaltbare Entitäten oder Instanzen von Association-Klassen darstellen. WQL ist jedoch implementierungsspezifisch. Er funktioniert nur mit der Windows-Implementierung des DMTF-Standards (WMI). Darüber hinaus ist die WQL-Syntax zum Abrufen von Association-Klassen recht kompliziert.

Die Windows-Infrastruktur der Remoteverwaltung (WinRM) bietet eine hervorragende Möglichkeit, die Funktionalität von WMI zu nutzen. Frühe Versionen von WinRM mussten WQL verwenden, um Instanzen von Association-Klassen abzurufen. WinRM 2.0 enthält ein neues Feature, das als DMTF-Profilermittlung durch Zuordnungsdurchlauf bezeichnet wird. Der Zuordnungsdurchlauf ermöglicht einem Benutzer von WinRM das Abrufen von Instanzen von Association-Klassen mithilfe eines Standardfiltermechanismus, des AssociationFilter-Dialekts, der in der DMTF CIM-Bindungsspezifikation definiert ist. Weitere Informationen zum Zuordnungsdurchlauf finden Sie in der WS-Management CIM-Bindungsspezifikation ( [https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man) ).

Das Hilfsprogramm winrm bietet einen einfachen Mechanismus, um die entsprechende Zuordnung zu durchlaufen und ein Geräteprofil abzurufen.

## <a name="configuration-implementation-details"></a>Details zur Konfigurationsimplementierung

Das Hilfsprogramm winrm unterstützt jetzt einen Dialekt für die Zuordnungsanforderung. Entweder der URI oder der Alias kann mit dem Hilfsprogramm winrm angegeben werden.



| Alias       | URI                                                               |
|-------------|-------------------------------------------------------------------|
| Korrelation | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a>Abrufen von Instanzen einer Zuordnungsklasse mithilfe des AssociationFilter-Dialekts

Das Hilfsprogramm winrm kann WMI-Zuordnungsklasseninstanzen einer bestimmten Quellinstanz abrufen. Der folgende Befehl veranschaulicht die Verwendung des Hilfsprogramms winrm zum Abrufen von Instanzen von [ \_ Win32-Dienst-Zuordnungsklassen.](../cimwin32prov/win32-service.md) Der Schalter "-associations" muss zum Zurückgeben von Zuordnungsklassen verwendet werden.

**winrm enumerate wmicimv2/ \* -dialect:association -associations -filter:{object=win32 \_ service?name=winrm;resultclassname=win32 \_ dependentservice;role=dependent}**

Der folgende textbasierte Codeausschnitt ist die Ausgabe des obigen Befehls:

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

## <a name="retrieving-instances-of-an-associated-class-by-using-the-associationfilter-dialect"></a>Abrufen von Instanzen einer zugeordneten Klasse mithilfe des AssociationFilter-Dialekts

Das Hilfsprogramm winrm kann WMI-Klasseninstanzen abrufen, die einer bestimmten Quellinstanz zugeordnet sind. Der folgende Befehl veranschaulicht die Verwendung des Hilfsprogramms winrm zum Abrufen von Instanzen der zugeordneten Klassen des [Win32-Diensts. \_ ](../cimwin32prov/win32-service.md)

**winrm enumerate wmicimv2/ \* -dialect:association -filter:{object=win32 \_ service?name=winrm;associationclassname=win32 \_ dependentservice;resultclassname=win32 \_ service;resultrole=antecedent;role=dependent}**

Der folgende textbasierte Codeausschnitt ist die Ausgabe des obigen Befehls:

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

 

 