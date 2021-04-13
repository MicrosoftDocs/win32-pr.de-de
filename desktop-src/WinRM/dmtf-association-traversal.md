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
# <a name="dmtf-profile-discovery-through-association-traversal"></a>Ermittlung von DMTF-Profilen durch Zuordnungs Durchlauf

Eine Schlüsselkomponente der WMI-Infrastruktur (Windows-Verwaltungsinstrumentation) ist ein objektorientiertes Modell der verwaltbaren Entitäten in einem System. Das Modell entspricht einem Standard, der vom Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) verwaltet wird, und wird als Common Information Model (CIM) bezeichnet. Einige Klassen im Modell, z. b. [CIM \_ DataFile](../cimwin32prov/cim-datafile.md) oder [Win32 \_ Process](../cimwin32prov/win32-process.md), entsprechen direkt verwaltbaren Entitäten. Andere Klassen im Modell, z. b. [Win32- \_ Systemdienste](../cimwin32prov/win32-systemservices.md), stellen Beziehungen zwischen verwaltbaren Entitäten dar. Diese Beziehungs Modellierungs Klassen werden als Zuordnungs Klassen bezeichnet.

Mithilfe der WMI-spezifischen Abfragesprache (WQL) können Sie Instanzen von Klassen abrufen, die verwaltbare Entitäten oder Instanzen von Zuordnungs Klassen darstellen. WQL ist jedoch Implementierungs spezifisch. Dies funktioniert nur mit der Windows-Implementierung des DMTF-Standards (WMI). Außerdem ist die WQL-Syntax zum Abrufen von Zuordnungs Klassen recht kompliziert.

Die Windows-Remoteverwaltung-Infrastruktur (WinRM) bietet eine hervorragende Möglichkeit, die Funktionalität von WMI zu nutzen. In frühen Versionen von WinRM mussten WQL zum Abrufen von Instanzen von Zuordnungs Klassen verwendet werden. WinRM 2,0 umfasst ein neues Feature, das als DMTF-Profil Ermittlung über Association Traversal bezeichnet wird. Der Zuordnungs Durchlauf ermöglicht einem Benutzer von WinRM das Abrufen von Instanzen von Zuordnungs Klassen mithilfe eines Standardfilter Mechanismus, dem associationfilter-Dialekt, der in der DMTF-CIM-Bindungs Spezifikation definiert ist. Weitere Informationen zu Association Traversal finden Sie in der WS-Management CIM-Bindungs Spezifikation ( [https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man) ).

Das WinRM-Hilfsprogramm bietet einen einfachen Mechanismus zum Durchlaufen der entsprechenden Zuordnung und zum Abrufen eines Geräte Profils.

## <a name="configuration-implementation-details"></a>Details zur Konfigurations Implementierung

Das WinRM-Hilfsprogramm unterstützt jetzt einen Dialekt für die Zuordnungs Anforderung. Entweder der URI oder der Alias kann mit dem WinRM-Hilfsprogramm angegeben werden.



| Alias       | URI                                                               |
|-------------|-------------------------------------------------------------------|
| Korrelation | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a>Abrufen von Instanzen einer Association-Klasse mithilfe des associationfilter-Dialekts

Das WinRM-Hilfsprogramm kann WMI-Zuordnungs Klassen Instanzen einer bestimmten Quell Instanz abrufen. Der folgende Befehl veranschaulicht, wie das WinRM-Hilfsprogramm verwendet wird, um Instanzen von [Win32- \_ Dienst](../cimwin32prov/win32-service.md) Zuordnungs Klassen abzurufen. Der Switch "-Zuordnungen" muss verwendet werden, um Zuordnungs Klassen zurückzugeben.

**WinRM auflisten wmicimv2/ \* -Dialekt: Association-Zuordnungen-Filter: {Object = Win32 \_ Service? Name = WinRM; resultclassname = Win32 \_ dependentservice; Role = Dependent}**

Der folgende textbasierte Code Ausschnitt ist die Ausgabe des obigen Befehls:

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

## <a name="retrieving-instances-of-an-associated-class-by-using-the-associationfilter-dialect"></a>Abrufen von Instanzen einer zugeordneten Klasse mithilfe des associationfilter-Dialekts

Mit dem WinRM-Hilfsprogramm können WMI-Klassen Instanzen abgerufen werden, die einer bestimmten Quell Instanz zugeordnet sind. Der folgende Befehl veranschaulicht, wie das WinRM-Hilfsprogramm verwendet wird, um Instanzen von zugeordneten [Win32- \_ Dienst](../cimwin32prov/win32-service.md) Klassen abzurufen.

**WinRM auflisten wmicimv2/ \* -Dialekt: Association-Filter: {Object = Win32 \_ Service? Name = WinRM; associationclassname = Win32 \_ dependentservice; resultclassname = Win32 \_ Service; RESULTROLE = Vorgänger; Role = Dependent}**

Der folgende textbasierte Code Ausschnitt ist die Ausgabe des obigen Befehls:

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

 

 